# Configurando-servidor-DNS

# Primeiramente deve ser criado uma nova VM para ser utilizada como computador de acesso dos sites ifrn.com e ufrn.com
# Logo após deve ser criado novamente todo um diretório para hospedar o site
cd /var/www/
sudo mkdir -p ufrn/public_html
sudo touch index.html
# Após isso é necessário configurar o site
<html><
<head><title>Olá seja bem vindo a UFRN</title>
</head>
<body>
<center>
<h1>Bem vindo ao site da UFRN</h1>
</body>
</html>

# Finalizando a parte de configuração vamos fazer o site entrar no ar
cd /etc/apache2/sites-available/
sudo nano ufrn.conf

# Colocando o site no ar
sudo a2ensite ufrn.conf

# Para finalizar é necessário apenas reiniciar o apache
sudo /etc/init.d/apache2 restart 

# Na máquina onde estão hospedados os outros sites deve se apenas finalizar as configurações para que o site ufrn.com entre no ar.
