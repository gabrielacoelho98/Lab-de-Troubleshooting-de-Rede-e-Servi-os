# 🌐 Lab de Troubleshooting de Rede e Serviços

Projeto prático de troubleshooting voltado à simulação de falhas comuns em ambientes de suporte técnico, abordando diagnóstico e resolução de problemas relacionados a conectividade de rede, serviços web, DNS e firewall em sistemas Windows e Linux.


---

## 🎯 Objetivo

Simular cenários reais de falhas operacionais encontradas em rotinas de suporte técnico e infraestrutura, aplicando procedimentos de diagnóstico e correção de problemas em serviços e conectividade.

---

## 🛠️ Tecnologias Utilizadas

- Oracle VirtualBox  
- Windows  
- Ubuntu Linux  
- Apache2  
- UFW Firewall  
- Ferramentas nativas de diagnóstico de rede  

---

## 🌐 Estrutura do Ambiente

O laboratório foi desenvolvido com duas máquinas virtuais interligadas por rede interna para simulação de comunicação cliente-servidor.

- **Cliente:** Windows  
- **Servidor:** Ubuntu Linux  
- **Rede Virtual:** `lab-network`  
- **Serviço Web:** Apache2  

---

## ⚙️ Configuração do Ambiente

### Rede Virtual no VirtualBox
- Adaptador 1: NAT  
- Adaptador 2: Rede Interna (`lab-network`)  

![Rede Linux](img/02-print-rede-virtualbox-linux.png)

![Rede Windows](img/01-print-rede-virtualbox-win.png)

---

### Configuração do Servidor Linux
![IP Linux](img/03-print-ip-linux.png)

---

### Configuração do Cliente Windows
![IP Windows](img/04-print-ip-windows.png)

---

### Teste Inicial de Conectividade
![Ping Inicial](img/05-print-ping-ok.png)

---

## 🔎 Cenários de Troubleshooting

### 🖥️ Cenário 1 — Serviço Web Inativo

Simulação de falha do serviço Apache para análise de indisponibilidade de aplicação.

#### Serviço em Execução
![Apache Rodando](img/06-print-apache-rodando.png)

#### Aplicação Disponível
![Site Online](img/07-print-site-ok.png)

#### Falha Simulada
![Apache Parado](img/08-print-apache-parado.png)

#### Aplicação Indisponível
![Site Offline](img/09-print-site-down.png)

#### Validação de Conectividade
![Ping Serviço Off](img/10-print-ping-ok-servico-off.png)

#### Diagnóstico de Porta
![Porta 80 Fechada](img/13-print-porta-80-fechada.png)

#### Status do Serviço
![Apache Inativo](img/14-print-apache-inativo.png)

**Diagnóstico:**  
A conectividade com o servidor permanecia funcional, porém o serviço Apache encontrava-se inativo, impedindo a entrega da aplicação web.

#### Resultado Após Correção
![Site Restaurado](img/15-print-site-restaurado.png)

---

### 🌐 Cenário 2 — Falha de DNS

Simulação de erro de resolução de nomes causado por configuração incorreta de DNS.

#### DNS Incorreto
![DNS Errado](img/16-print-dns-errado.png)

#### Falha de Resolução
![Ping Google Falha](img/17-print-ping-google-falha.png)

#### Teste via IP
![Ping IP OK](img/18-print-ping-ip-ok.png)

**Diagnóstico:**  
A conectividade com a internet permanecia operacional, porém a resolução de nomes falhava devido à configuração incorreta do servidor DNS.

#### Resultado Após Correção
![DNS Corrigido](img/19-print-dns-corrigido.png)

---

### 🔥 Cenário 3 — Firewall Bloqueando Serviço

Simulação de indisponibilidade causada por regra de firewall bloqueando porta de serviço.

#### Bloqueio Configurado
![Firewall Bloqueio](img/20-print-firewall-bloqueio.png)

#### Ping Funcional
![Ping Firewall](img/21-print-ping-ok-firewall.png)

**Diagnóstico:**  
O servidor permanecia acessível via rede, porém o firewall bloqueava a porta 80, impedindo acesso ao serviço web.

#### Resultado Após Correção
![Firewall Corrigido](img/22-print-firewall-corrigido.png)

---

## 📚 Conhecimentos Aplicados

- Troubleshooting de Serviços  
- Diagnóstico de DNS  
- Gerenciamento de Firewall  
- Análise de Portas e Serviços  
- Troubleshooting de Infraestrutura  
- Diagnóstico de Rede Cliente/Servidor  

---

## 🚀 Resultado

Ao final do laboratório foi possível identificar, diagnosticar e corrigir múltiplos cenários de falha relacionados a serviços, DNS, firewall e conectividade, reforçando conhecimentos práticos aplicáveis em rotinas de suporte técnico, help desk e infraestrutura de TI.
