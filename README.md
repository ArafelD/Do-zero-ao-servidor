# 🌐 Raspberry Pi Web Server Starter  

Transforme seu **Raspberry Pi** em um servidor web funcional e hospede seu primeiro site!  
Este repositório contém instruções, scripts básicos e exemplos de código para você começar.  

---

## 📦 O que você vai precisar  

![Raspberry Pi](https://www.raspberrypi.com/app/uploads/2021/03/raspberry-pi-4-hero-500x333.jpg)  

- Raspberry Pi (3B+, 4 ou 5 recomendado)  
- Cartão microSD (mínimo 16 GB, classe 10)  
- Fonte de alimentação oficial ou equivalente  
- Cabo Ethernet (opcionalmente Wi-Fi)  
- Case (opcional, mas recomendado)  

---

## 💽 Instalação do Sistema Operacional  

1. Baixe o [Raspberry Pi Imager](https://www.raspberrypi.com/software/).  
2. Grave o **Raspberry Pi OS Lite (64-bit)** no cartão microSD.  
3. Configure no Imager:  
   - Hostname: `meuservidor.local`  
   - Ative SSH  
   - Defina usuário e senha fortes  
   - Configure Wi-Fi (se não usar cabo)  

---

## 🔑 Acessando o Raspberry Pi  

![SSH](https://upload.wikimedia.org/wikipedia/commons/6/62/Secure_Shell_logo.png)  

Depois de ligar o Pi:  

bash
ssh seu_usuario@ip_do_seu_pi

⚡ Instalando Nginx (Servidor Web)

No terminal do Raspberry Pi:

sudo apt update && sudo apt upgrade -y
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx


Abra no navegador:

http://ip_do_seu_pi


Você verá a página padrão do Nginx ✅

🖥 Publicando seu primeiro site

Entre na pasta raiz do servidor:

cd /var/www/html
sudo rm index.nginx-debian.html
sudo nano index.html


Adicione um HTML simples:



```<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Meu Site no Raspberry Pi</title>
    <style>
        body { font-family: sans-serif; background-color: #2a2a2a; color: #e0e0e0; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .container { text-align: center; padding: 40px; border-radius: 15px; background-color: #3a3a3a; box-shadow: 0 0 20px rgba(0,0,0,0.5); }
        h1 { color: #00ff9d; }
    </style>
</head>
<body>
    <div class="container">
        <h1>🎉 Meu Site está no Ar! 🎉</h1>
        <p>Hospedado com sucesso em um Raspberry Pi usando Nginx.</p>
    </div>
</body>
</html>

Salve, feche e recarregue no navegador.

👉 Pronto! Seu site está online dentro da sua rede local.
````


🚀 Próximos Passos

Usar domínio dinâmico com DuckDNS

Adicionar HTTPS com Certbot

Instalar PHP + MariaDB para rodar WordPress ou Ghost

Transformar em servidor de arquivos com Samba

Bloquear anúncios em toda a rede com Pi-hole

📂 Estrutura deste repositório

raspberrypi-webserver-starter/

│── site-exemplo/

│   └── index.html

│── scripts/

│   └── setup_nginx.sh

│── README.md


site-exemplo/: contém um HTML pronto para publicar.

scripts/: scripts para automação (instalação rápida do Nginx).

💡 Contribuindo

Pull requests são bem-vindos!
Sugestões de melhorias, novos exemplos de sites e automações são muito bem recebidas.

📜 Licença

Este projeto é open-source sob a licença MIT.
