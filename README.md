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
![Ping do Teste](Imagens/imagens/Captura de tela 2026-11-14 183514.png)


Reconhecimento (Nmap)
Antes de iniciar os ataques, realizamos um escaneamento de portas para identificar quais serviços estavam ativos no alvo:

## 🔍 2. Fases dos Testes e Execução
ftp
