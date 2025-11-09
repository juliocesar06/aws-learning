# EC2(Elastic Compute Cloud)
## O QUE É
EC2 significa **Elastic Compute Cloud**, o serviço de máquinas virtuais na nuvem da AWS. Ele permite criar, configurar e rodar *servidores virtuais* (chamados **instâncias**) com controle total sobre o sistema operacional, memória, CPU, rede e armazenamento

## PRA QUE SERVE?
- hospedar aplicações
- sites
- bancos de dados
- sistemas interno
- bots
- APIs
- jogos

## COMO FUNCIONA

1. Escolhe um tipo de instância
2. um sistema operacional
3. configura segurança
4. armazenamento


## BASICO NECESSARIO PARA SABER 💡

- 🔹 Instância = sua máquina virtual.
- 🔹 AMI (Amazon Machine Image) = imagem do sistema operacional + apps.
- 🔹 Tipo de instância = define CPU, RAM, rede (ex: t3.micro, m5.large).
- 🔹 Key Pair = chave de acesso para conectar.
- 🔹 Security Group = regras de firewall.
- 🔹 EBS (Elastic Block Store) = armazenamento persistente.
- 🔹 Região / Zona de disponibilidade = local onde o servidor roda.
- 🔹 Elastic IP = IP fixo público opcional.
- 🔹 Auto Scaling = adiciona/remove instâncias conforme demanda.
- 🔹 Load Balancer = distribui o tráfego entre instâncias.

## 🧠 Tipos de instâncias

| Tipo | Uso principal | Exemplos |
|------|----------------|-----------|
| 💼 **Uso geral** | Equilíbrio entre CPU e memória | Web apps, repositórios |
| ⚙️ **Otimizada p/ computação** | Tarefas intensivas em CPU | Servidores de jogos, ML |
| 🧮 **Otimizada p/ memória** | Processamento de dados em RAM | Bancos de dados em memória |
| 🎨 **Computação acelerada (GPU)** | Gráficos, IA, simulações | ML, renderização 3D |
| 💾 **Otimizada p/ armazenamento** | Acesso rápido a dados locais | Big data, logs |
# INSTÂNCIANDO
  ### Console
  
  * Esse é o método direto via terminal (PowerShell, CMD ou bash)

  
## 🔸 1. Pelo Console AWS (modo gráfico)

  1. Acesse o painel [AWS Management Console](https://aws.amazon.com/console/)
  
  2. Vá em **EC2 → Launch Instance**
  
  3. Escolha:
  
    - **Nome** da instância
    - **AMI** (Ubuntu, Amazon Linux, etc.)
    - **Tipo de instância** (ex: `t3.micro`)
    - **Key Pair** (crie ou selecione uma existente)
    - **Security Group**
    - **Armazenamento**
  
  4. Clique em **Launch Instance**

  ![Instânciando](https://github.com/juliocesar06/aws-learning/blob/main/modulos/img/aws_instanciando.gif?raw=True)

  Obs: uso de 0.0.0.0/0 apenas por exemplo
  
  ## 🔸 2. Por CLI 

  ### Pré-requisito
  *  ter AWS CLI instalado.
  *  aws configure com suas chaves de acesso (Access Key e Secret Key)

- info importante

| Parametro           | Significado|
| --------------------|---------------------------------------|
|--image-id           |	ID da AMI (Ubuntu, Amazon Linux, etc.)|
|--instance-type	    |Tipo da instância
|--key-name	          |Nome da chave SSH
|--security-group-ids	|Firewall associado
|--subnet-id	        |Sub-rede VPC
|--region	            |Região AWS
|--tag-specifications	|Nomeia automaticamente a instância

* Comando de Exemplo:

```bash
aws ec2 run-instances \
  --image-id ami-0abcd1234efgh5678 \
  --instance-type t3.micro \
  --key-name minha-chave \
  --security-group-ids sg-0123456789abcdef \
  --subnet-id subnet-0abcdef123456789 \
  --region us-east-1 \
  --tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=MinhaInstanciaCLI}]'
  ```

  ## 🔸 3. Pelo SDK (Boto3 - Python)

  ```python
  import boto3

ec2 = boto3.resource('ec2')

instance = ec2.create_instances(
    ImageId='ami-0abcd1234efgh5678',
    InstanceType='t3.micro',
    KeyName='minha-chave',
    MinCount=1,
    MaxCount=1,
    TagSpecifications=[
        {
            'ResourceType': 'instance',
            'Tags': [{'Key': 'Name', 'Value': 'Instancia-SDK'}]
        }
    ]
)
print(f"Instância criada: {instance[0].id}")




