# Aprendendo a fazer um projeto em Django
primeiro ver o setup django.md para fazer os comando necessarios para o django

- Dentro do .env
>SECRET_KEY = sua secret key

- Em settings.py
>from pathlib import Path, os<br>
>from dotenv import load_dotenv<br>
>load_dotenv()

- Agora na secret key
>str(os.getenv('SECRET_KEY'))

## Criar um .gitignore
[Templates .gitignore](gitignore.io.)

## Iniciar o Projeto
>django-admin startproject setup .

o arquivo "manage.py", que acabou de ser criado. Ele é responsável por realizar a maioria dos comandos que utilizaremos para o desenvolvimento de aplicações Django e também por subir servidores.
>python mange.py runserver

## Criar uma pasta
>python manage.py startapp \<nome da pasta>

 - ex: python manage.py startapp galeria<br>
  (chamado de galeria porque ele vai esta ligado com tudo que tive de imagens no projeto)

  - Adicionar galeria como app no projeto
  > \>setup\>settings.py

  - Vamos rolar a página até encontrar a seção "INSTALLED_APPS" do código. Nela, no final da lista, vamos passar o app que acabamos de criar:
  >ISNTALLED_APPS = [
        'django.contrib.admin',<br>
        'django.contrib.auth',<br>
        'django.contrib.contenttypes',<br>
        'django.contrib.sessions',<br>
        'django.contrib.messages',<br>
        'django.contrib.staticfiles',<br>
        'galeria', <--- AQUI FOI A ADIÇÃO