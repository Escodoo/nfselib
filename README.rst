nfselib Python library
======================


Como Usar
=========

TODO

Como Converter XSD em Código Python
===================================

Crie um diretório qualquer:

    mkdir laboratorio

    cd laboratorio

Crie um ambiente virtual e ative o mesmo:

    virtualenv .

    source bin/activate

Baixe os fontes necessários:

    hg clone https://bitbucket.org/kmee/generateds --branch=odoo-plugin

    git clone git@github.com:erpbrasil/erpbrasil.edoc.gen.git

Agora faça a instalação de cada um deles:

    cd generateds

    pip install .

    cd ..

    cd erpbrasil.edoc.gen

    pip install .

Baixe e descompacte os arquivos do provedor NFSe:

    wget https://www.notacontrol.com.br/download/manuais.zip

    unzip manuais.zip

    cd Manuais/

    unzip Schemas.zip

    cd ..

    mkdir issnet-teste

    cd issnet-teste/

    mkdir -p issnet/v1_0

    mv ../Manuais/Schemas/* issnet/v1_0/

Agora execute o comando abaixo para gerar os arquivos python:

    erpbrasil-edoc-gen-generate-python -n issnet -v v1.0 -s . -d .

Verifique se os arquivos foram criados:

    ls issnetlib/v1_0/
