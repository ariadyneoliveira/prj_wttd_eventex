# prj_wttd_eventex
Sistema de eventos


## Como desenvolver?
  
 1. Clone o repositório
 2. Crie um virtualenv com Python 3.5
 3. Ative o virtualenv
 4. Instale as dependencias
 5. Configure a instancia com o .env
 6. Execute os seguintes passos.
 
 ```console
 git clone git@github.com:ariadyneoliveira/prj_wttd_eventex.git wttd
 cd wttd
 python -m venv .wttd
 source .wttd/bin/activate
 pip install -r requirements.txt
 cp contrib/env-sample .env
 python manage.py test
 ```
## Como fazer o deploy?
 1. Crie uma instancia no heroku
 2. Envie as configurações para o heroku
 3. Define uma SECRET_KEY segura
 4. Defina DEBUG=False
 5. Configure o serviço de email
 6. Envie o código para o heroku
 
 ```console
 heroku create minhainstancia
 heroku config:push
 heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
 heroku config:set DEGUB=False
 #configuro o email
 git push heroku master --force  
 ```
