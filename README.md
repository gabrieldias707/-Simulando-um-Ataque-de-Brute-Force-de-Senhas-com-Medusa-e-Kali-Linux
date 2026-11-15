# 🛡️ Simulação de Ataques de Força Bruta com Kali Linux e Medusa

Este repositório documenta a realização do desafio prático da **DIO**, cujo objetivo é explorar conceitos de segurança ofensiva em ambiente controlado, simulando cenários de testes de intrusão (Pentest) para compreender vulnerabilidades de autenticação e suas respectivas formas de mitigação.

---

## 🛠️ 1. Configuração do Ambiente de Laboratório

Para a execução segura e controlada dos testes, o ambiente foi isolado utilizando o **Oracle VM VirtualBox** com duas máquinas virtuais conectadas através de uma rede interna (Host-Only):

* **Atacante (Attacker):** Kali Linux 
* **Alvo (Target):** Metasploitable 2 
  * *O Metasploitable 2 já possui diversos serviços desatualizados e intencionalmente vulneráveis (como FTP, SSH, Telnet, SMB e aplicações web como o DVWA).*

---

## 🔍 2. Fases dos Testes e Execução

### Fase 1: Uso do Ping
![Ping do Teste](Imagens/Captura%20de%20tela%202026-11-14%20183514.png)


Reconhecimento (Nmap)
Antes de iniciar os ataques, realizamos um escaneamento de portas para identificar quais serviços estavam ativos no alvo:

```bash
nmap -sV -p- 192.168.56.102
