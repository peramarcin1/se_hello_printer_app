Simple Flask App
================

Aplikacja Dydaktyczna wyświetlająca imię i wiadomość w różnych formatach dla zajęć 
o Continuous Integration, Continuous Delivery i Continuous Deployment.

- Rozpocząnając pracę z projektem (wykorzystując virtualenv). Hermetyczne środowisko dla pojedyńczej aplikacji w python-ie:

  ::

    # centos, add to ~/.bashrc
    source /usr/bin/virtualenvwrapper.sh
    
    # ubuntu, add to ~/.bashrc
    source /usr/local/bin/virtualenvwrapper.sh

    mkvirtualenv wsb-simple-flask-app
    pip install -r requirements.txt
    pip install -r test_requirements.txt

- Uruchamianie applikacji:

  :: 

    # jako zwykły program
    python main.py

    # albo:
    PYTHONPATH=. FLASK_APP=hello_world flask run

- Uruchamianie testów (see: http://doc.pytest.org/en/latest/capture.html):

  ::

    PYTHONPATH=. py.test
    PYTHONPATH=. py.test  --verbose -s

- Kontynuując pracę z projektem, aktywowanie hermetycznego środowiska dla aplikacji py:

  ::

    source /usr/bin/virtualenvwrapper.sh # nie trzeba, jeśli już w .bashrc
    workon wsb-simple-flask-app


- Integracja z TravisCI:

  ::

    ...


Pomocnicze
==========

Ubuntu
------

- Instalacja python virtualenv i virtualenvwrapper:

  ::

    sudo su
    pip install virtualenv
    pip install virtualenvwrapper

Centos
------

- Instalacja python virtualenv i virtualenvwrapper:

  ::

    yum install -y python-pip
    pip install -U pip
    pip install virtualenv
    pip install virtualenvwrapper
  
- Instalacja docker-a:

  :: 

    yum remove docker \
        docker-common \
        container-selinux \
        docker-selinux \
        docker-engine

    yum install -y yum-utils

    yum-config-manager \
      --add-repo \
      https://download.docker.com/linux/centos/docker-ce.repo

    yum makecache fast
    yum install -y docker-ce
    systemctl start docker

Materiały
=========

- https://virtualenvwrapper.readthedocs.io/en/latest/


Odpalenie
=========

   source /usr/local/bin/virtualenvwrapper.sh

   mkvirtualenv wsb-simple-flask-app

   przejscie do katalogu se_hello_printer_app

   komenda make deps


Badge TracisCI
========

.. image:: https://travis-ci.org/travis-ci/travis-web.svg?branch=master
    :target: https://travis-ci.org/travis-ci/travis-web

Badge StatusCake
=======

.. image:: https://app.statuscake.com/button/index.php?Track=B8VQbl7Xgs&Days=1&Design=2
    :target: https://app.statuscake.com/UptimeStatus.php?tid=3976146


