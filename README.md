# Criando-Ransomware-e-Keylogger-teste-aula-Ciberseguranca-
Desenvolver, documentar e compartilhar um projeto em Python que simule malwares em ambiente seguro, incluindo ransomware com criptografia e descriptografia de arquivos, mensagem de resgate e keylogger simulado, além de apresentar medidas de prevenção e defesa contra ameaças digitais.

# Simulando um Malware de Captura de Dados Simples em Python e Aprendendo a se Proteger

Projeto prático desenvolvido no contexto de cibersegurança defensiva com o objetivo de compreender, simular e documentar o funcionamento de ameaças digitais comuns (**Ransomware** e **Keylogger**), analisando técnicas de ataque em ambiente controlado para aprimorar mecanismos de defesa, mitigação e conscientização.

---

## 📋 Sumário
1. [Sobre o Desafio](#-sobre-o-desafio)
2. [Arquitetura e Módulos do Projeto](#-arquitetura-e-módulos-do-projeto)
3. [Módulo 1: Ransomware Simulado](#-módulo-1-ransomware-simulado)
4. [Módulo 2: Keylogger Simulado com Envio por E-mail](#-módulo-2-keylogger-simulado-com-envio-por-e-mail)
5. [Como Executar o Projeto](#-como-executar-o-projeto)
6. [Medidas de Defesa e Mitigação](#-medidas-de-defesa-e-mitigação)
7. [Aviso Legal](#-aviso-legal)

---

## 🎯 Sobre o Desafio
Este repositório documenta os estudos práticos sobre o comportamento de malwares utilizando a linguagem **Python**. O foco principal é a **cibersegurança defensiva**: entender como atacantes operam para saber como proteger sistemas corporativos e pessoais de forma eficiente.

O projeto abrange:
* **Ransomware Simulado:** Criação de arquivos de teste, implementação de scripts de criptografia/descriptografia simétrica e geração de nota de resgate[cite: 8].
* **Keylogger Simulado:** Captura de eventos de teclado, manipulação de arquivos de log e automação de envio remoto via protocolo SMTP[cite: 8].
* **Análise Defensiva:** Documentação de boas práticas, prevenção, sandboxing e detecção de ameaças[cite: 8].

---

## 🛠️ Arquitetura e Módulos do Projeto

A estrutura de diretórios do projeto está organizada da seguinte forma:

```text
malware/
│
├── test_files/              # Pasta isolada contendo arquivos de teste
│   ├── dados_confidenciais
│   └── senhas.txt
│
├── ramsoware.py             # Script de criptografia (simulação de Ransomware)
├── descriptografar.py       # Script de reversão/descriptografia
├── keylogger_email.py       # Script de captura de teclas e envio por e-mail
├── chave.key                # Chave simétrica gerada para criptografia
└── LEIA ISSO.txt            # Nota de resgate simulada
