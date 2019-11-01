# Eventex

Sistema de Eventos encomendado pela Morena.
[![Build Status](https://travis-ci.org/dressacl/Python.svg?branch=master)](https://travis-ci.org/dressacl/Python)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/267f1b717f92466eb54816d720e1f0c9)](https://www.codacy.com/manual/dressacl/Python?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dressacl/Python&amp;utm_campaign=Badge_Grade)

# Como desenvolver?

1. Clone o repositório.
2. Crie um vitualenv com Python 3.5
3. Ative o virtualenv.
4. Instale as dependências.
5. Configure a instância com o .env
6. Execute os testes.

```
git clone https://github.com/dressacl/Python.git
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements-dev.txt
cp contrib/env-sample .env
python manage.py test
``` 

##Como fazer o deploy?

1. Crie uma instância no heroku.
2. Envie as configurações para o heroku.
3. Define uma SECRET_KEY segura para instância.
4. Defina DEBUG=False
5. Configure o serviço de email.
6. Envie o código para o heroku

```console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
# configuro o email
git push heroku master --force

```