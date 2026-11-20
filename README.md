# 🛡️ Simulação de Ataques de Força Bruta com Kali Linux e Medusa

Este repositório documenta a realização do desafio prático da **DIO**, cujo objetivo é explorar conceitos de segurança ofensiva em ambiente controlado, simulando cenários de testes de intrusão (Pentest) para compreender vulnerabilidades de autenticação e suas respectivas formas de mitigação.


## 🛠️ 1. Configuração do Ambiente de Laboratório

Para a execução segura e controlada dos testes, o ambiente foi isolado utilizando o **Oracle VM VirtualBox** com duas máquinas virtuais conectadas através de uma rede interna (Host-Only):

* **Atacante (Attacker):** Kali Linux 
* **Alvo (Target):** Metasploitable 2 192.168.56.102
  * *O Metasploitable 2 já possui diversos serviços desatualizados e intencionalmente vulneráveis (como FTP,SMB e aplicações web como o DVWA).*




### Fase 1: Uso do Ping
primeiro pinguei metasploitable no kali linux se esta funcionado
![ping](imagens/configurando%20o%20ambiente%20virtual/ping-teste.png)
## Configurando o Ambiente Virtual

Veja abaixo como realizar o teste de conexão:
aqui no inet 19.168.56.102 é o ip que vamos usar para o teste
![mataplot](imagens/configurando%20o%20ambiente%20virtual/conferindo%20o%20ip%20no%20metaplot%202.png)

Reconhecimento (Nmap)
Antes de iniciar os ataques, realizamos um escaneamento de portas para identificar quais serviços estavam ativos no alvo:
usando o comando para saber quais portas estão abertas 
![Nmap](imagens/nmap/executando%20nmap.png)
## 🔍 2. Fases dos Testes e Execução
ftp primeiro vamos usar o comando ftp mais o ip 
![comando ftp](imagens/ftp/caminho%20para%20o%20ftp.png)


aqui esta o ftp mas não conseguimos entra pois não sabemos ainda login para o acessalo

![dentrodoftp](imagens/ftp/ftp.png)


agora criaremos usuarios e senhas para ftp

![criando usuarios](imagens/ftp/criando%20usuarios%20para%20ftp.png)

![criando senha](imagens/ftp/criando%20as%20senhas%20de%20usuarios%20para%20ftp.png)

agora com o usuarios e senhas criado vamos usar o medusa

![medusa](imagens/ftp/rodando%20o%20medusa.png)
