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


