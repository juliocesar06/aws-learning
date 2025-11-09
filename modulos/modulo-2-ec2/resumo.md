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

## TIPOS DE INSTÂNCIAS
- Instâncias de uso geral 
  - Equilibrio recursos de computaçao.
    - várias workloads 
    - serviços da web
    - repositórios de código

- Instâncias otimizadas para computação.
  -  Ideais para tarefas de computação intensiva.
     - computação intensiva
     - servidores de jogos
     - computação de alto desempenho
     - machine learning
     - modelagem científica.

- Instâncias otimizadas para memória
   - boas para tarefas que consomem muita memória
     - desempenho rápido para grande processamento de dados.
- cálculos de números de ponto flutuante
      

- instâncias de computação acelerada
  - cálculos de números de ponto flutuante
  - processamento gráfico
  - correspondência de padrões de dados

- instâncias otimizadas para armazenamento
  -  alto desempenho para dados armazenados localmente.

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




  

  ### Pré-requisito
  *  ter AWS CLI instalado.
  *  aws configure com suas chaves de acesso (Access Key e Secret Key)










  <table>
    <tr>
      <th>Parâmetro </th>
      <th>Significado </th>
    </tr>
    <tr>
      <th>--image-id</th>
      <th>ID da AMI (ex: Ubuntu, Amazon Linux, etc.)</th>
    </tr>
     <tr>
      <th>--instance-type</th>
      <th>Tipo da instância (t2.micro, t3.small, etc.)</th>
    </tr>
     <tr>
      <th>--key-name</th>
      <th>Nome do par de chaves SSH</th>
    </tr>
     <tr>
      <th>--security-group-ids</th>
      <th>ID do Security Group</th>
    </tr>
     <tr>
      <th>--subnet-id</th>
      <th>Sub-rede na VPC</th>
    </tr>
     <tr>
      <th>--region</th>
      <th>Região AWS</th>
    </tr>
     <tr>
      <th>--tag-specifications</th>
      <th>Nomeia a instância automaticamente</th>
    </tr>
  </table>

<h3>cli</h3>
  -
<h3>sdk</h3>



