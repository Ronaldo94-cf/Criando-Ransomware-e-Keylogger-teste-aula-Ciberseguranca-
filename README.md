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



------------------------------------------------------------------------------------------
🔒 Módulo 1: Ransomware Simulado
O módulo de ransomware utiliza a biblioteca cryptography (baseada no algoritmo simétrico Fernet) para demonstrar a confidencialidade e o sequestro de dados em diretórios específicos.

Geração de Chave (gerar_chave): Cria uma chave criptográfica única e armazena no arquivo chave.key.

Varredura de Arquivos (encontrar_arquivos): Percorre a árvore de diretórios utilizando os.walk focando estritamente na pasta test_files, ignorando scripts e chaves de segurança.

Criptografia e Descriptografia: Lê os dados em formato binário (rb), aplica a cifra e reescreve os dados cifrados (wb).

Nota de Resgate (criar_mensagem_resgate): Gera um arquivo de texto instruindo o usuário sobre o falso sequestro dos dados educacionais.

⌨️ Módulo 2: Keylogger Simulado com Envio por E-mail
O keylogger monitora entradas de teclado em segundo plano de forma controlada, armazenando os caracteres capturados e enviando-os periodicamente por e-mail.

Captura de Eventos (pynput.keyboard): Monitora teclas pressionadas (on_press), formatando espaços, quebras de linha e correções ([<] para backspace).

Envio Automatizado (threading.Timer e smtplib): Utiliza threads para disparar envios automáticos do log acumulado a cada intervalo definido (ex: 60 segundos) através de conexões seguras TLS com servidores SMTP.

🚀 Como Executar o Projeto
Pré-requisitos
Python 3.11 ou superior instalado (com a opção Add Python to PATH ativa).

Gerenciador de pacotes pip.

1. Instalação de Dependências
No terminal do seu editor (como o VS Code), instale a biblioteca de criptografia e a ferramenta de controle de teclado:
**python -m pip install cryptography pynput**


2. Executando o Ransomware de Teste
Crie uma pasta chamada test_files na raiz com alguns arquivos de texto simulados.

Execute o script de criptografia:
**python ramsoware.py**

Para reverter o processo e recuperar os dados, execute o script de restauração:
**python descriptografar.py**

====================================================================
3. Executando o Keylogger
Configure as credenciais de e-mail de teste no script keylogger_email.py.

Execute o monitoramento:

PowerShell
**python keylogger_email.py**

===========================================================================
🛡️ Medidas de Defesa e Mitigação
Para se proteger contra ataques reais de Ransomware e Keyloggers, adote as seguintes práticas de segurança:

Backups Regulares (3-2-1): Mantenha cópias de segurança offline e isoladas da rede corporativa.

Soluções Antivírus e EDR: Utilize ferramentas atualizadas capazes de detectar comportamentos anômalos de leitura/escrita em massa ou capturas de hooks de teclado.

Princípio do Menor Privilégio: Restrinja permissões de execução de scripts e acesso a pastas sensíveis do sistema operacional.

Conscientização de Usuários: Treine equipes para não abrirem anexos suspeitos ou executarem códigos fontes desconhecidos de origens não confiáveis.

⚠️ Aviso Legal
Uso estritamente educacional. Os códigos e conceitos apresentados neste repositório têm como único propósito o aprendizado acadêmico em laboratório controlado de cibersegurança defensiva. O autor não se responsabiliza pelo uso indevido destas ferramentas fora de ambientes de teste autorizados.


