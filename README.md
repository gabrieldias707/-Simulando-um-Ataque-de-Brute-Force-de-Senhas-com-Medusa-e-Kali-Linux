# 🛡️ Simulação de Ataques de Força Bruta com Kali Linux e Medusa

Este repositório documenta a realização do desafio prático da **DIO**, cujo objetivo é explorar conceitos de segurança ofensiva em ambiente controlado, simulando cenários de testes de intrusão (Pentest) para compreender vulnerabilidades de autenticação e suas respectivas formas de mitigação.

---

## 🛠️ 1. Configuração do Ambiente de Laboratório

Para a execução segura e controlada dos testes, o ambiente foi isolado utilizando o **Oracle VM VirtualBox** com duas máquinas virtuais conectadas através de uma rede interna (Host-Only):

* **Atacante (Attacker):** Kali Linux 
* **Alvo (Target):** Metasploitable 2 192.168.56.102
  * *O Metasploitable 2 já possui diversos serviços desatualizados e intencionalmente vulneráveis (como FTP, SSH, Telnet, SMB e aplicações web como o DVWA).*

---



### Fase 1: Uso do Ping
primeiro pinguei metasploitable no kali linux
![Ping do Teste](Imagens/Captura%20de%20tela%202026-11-14%20183514.png)


Reconhecimento (Nmap)
Antes de iniciar os ataques, realizamos um escaneamento de portas para identificar quais serviços estavam ativos no alvo:

## 🔍 2. Fases dos Testes e Execução
ftp
verifica quais portas estão abertas dos serviços 
<img src="Imagens/Captura%20de%20tela%202026-11-14%20184005.png" alt="Portas vulneráveis escaneadas" width="700">
agora estou acessando ftp:usando o comando ftp 192.168.56.102
# 🛡️ Laboratório de Pentest: Kali Linux & Metasploitable 2 (DVWA)

Documentação da configuração de um ambiente isolado de testes de invasão utilizando o **Oracle VirtualBox**, conectando uma máquina atacante (**Kali Linux**) a um alvo vulnerável (**Metasploitable 2**) em rede interna (*Host-Only*).

---

## 1. Ambiente de Virtualização (VirtualBox)

Visão geral das máquinas virtuais configuradas e em execução no gerenciador do VirtualBox:

![Gerenciador VirtualBox](images/01-virtualbox-gerenciador.png)

---

## 2. Configuração de Rede (*Host-Only*)

Para garantir que o laboratório fique isolado da rede externa, ambas as máquinas foram configuradas com o adaptador em modo **Placa de rede exclusiva de hospedeiro (Host-Only)**[cite: 6, 7]:

* **Configuração de rede do Kali Linux:**
  ![Rede Kali Linux](images/02-rede-kali.png)

* **Configuração de rede do Metasploitable 2:**
  ![Rede Metasploitable](images/03-rede-metasploitable.png)

---

## 3. Inicialização e Identificação de IP (Alvo)

1. Inicialização do sistema **Metasploitable 2**:
   ![Boot Metasploitable](images/04-boot-metasploitable.png)

2. Autenticação no terminal utilizando as credenciais padrão (`msfadmin` / `msfadmin`):
   ![Login Metasploitable](images/05-login-metasploitable.png)

3. Verificação do endereço IP atribuído à interface `eth0` (`192.168.56.102`) através do comando `ip a`:
   ![IP Metasploitable](images/06-ip-metasploitable.png)

---

## 4. Acesso e Teste de Conectividade (Atacante)

1. Ambiente gráfico do **Kali Linux** inicializado:
   ![Desktop Kali Linux](images/07-desktop-kali.png)

2. Abertura do terminal no Kali Linux (`gabriel@kali`):
   ![Terminal Kali Linux](images/08-terminal-kali.png)

3. Teste de conectividade entre o Kali Linux e o Metasploitable 2 utilizando o comando `ping -c 3 192.168.56.102`:
   ![Ping Kali para Metasploitable](images/09-ping-teste.png)

---

## 5. Acesso à Aplicação Web (DVWA)

Com a comunicação estabelecida, foi realizado o acesso via navegador à aplicação **Damn Vulnerable Web App (DVWA)** hospedada no alvo através do endereço `http://192.168.56.102/dvwa/index.php`:

![Acesso ao DVWA](images/10-acesso-dvwa.png)

