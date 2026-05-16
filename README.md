# Gerenciamento de Instâncias EC2 na AWS - Lab Ocean/DIO

Este repositório contém minhas anotações, insights e a documentação prática sobre o gerenciamento de instâncias Amazon EC2 (Elastic Compute Cloud) na AWS, desenvolvido durante o bootcamp na DIO.

## 🎯 Objetivos do Aprendizado
* Compreender o conceito de computação em nuvem com AWS EC2.
* Aprender a provisionar, configurar e conectar-se a uma instância virtual.
* Entender o ciclo de vida de uma instância e as boas práticas de segurança.

---

## 📑 Principais Conceitos Aprendidos

### 1. O que é o Amazon EC2?
O EC2 é um serviço da AWS que fornece capacidade de computação escalável na nuvem. Ele elimina a necessidade de investir em hardware inicial, permitindo lançar servidores virtuais conforme a demanda.

### 2. Ciclo de Vida da Instância
Durante o laboratório, ficou clara a diferença entre os estados da instância:
* **Start:** Liga a máquina virtual (inicia a cobrança de computação).
* **Stop:** Desliga a máquina. Os dados no volume EBS continuam salvos, mas você para de pagar pelo processamento.
* **Terminate:** Exclui a instância permanentemente. O volume associado geralmente é deletado junto.

### 3. Segurança (Security Groups)
Os Security Groups atuam como um firewall virtual para a instância. Aprendi a configurar as regras de entrada (Inbound Rules) para permitir acessos específicos, como:
* Portas comuns: SSH (22), HTTP (80) e HTTPS (443).

---

## 🛠️ Passo a Passo da Prática (Resumo)
1. **Configuração Inicial:** Escolha da AMI (Amazon Linux 2 / Ubuntu) e do tipo de instância (foco na elegível para o nível gratuito, ex: `t2.micro`).
2. **Chaves de Acesso:** Criação e download do par de chaves (`.pem`) para conexão segura via SSH.
3. **Lançamento:** Execução da instância e acompanhamento do status do sistema.
4. **Conexão:** Utilização do terminal (ou EC2 Instance Connect) para acessar a máquina remotamente.

---

## 💡 Insights e Aprendizados
* **Atenção aos Custos:** É fundamental dar `Stop` ou `Terminate` em instâncias de teste para evitar cobranças surpresa na AWS, mesmo usando o nível gratuito.
* **Segurança em Primeiro Lugar:** Nunca se deve liberar o acesso SSH (porta 22) para qualquer IP (`0.0.0.0/0`) em ambientes de produção. O ideal é restringir para o seu IP atual.

---

## 🔗 Links Úteis
* [Documentação Oficial do Amazon EC2](https://docs.aws.amazon.com/ec2/)
* [Meu perfil na DIO](SEU_LINK_DO_PERFIL_DA_DIO_AQUI)
