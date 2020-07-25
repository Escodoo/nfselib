nfselib Python library
======================

TODO

Como Usar
=========
virtualenv .
source bin/activate
hg clone https://bitbucket.org/kmee/generateds --branch=odoo-plugin
git clone git@github.com:erpbrasil/erpbrasil.edoc.gen.git

cd generateds
pip install .

cd ..

cd erpbrasil.edoc.gen
pip install .

wget https://www.notacontrol.com.br/download/manuais.zip
unzip manuais.zip

cd Manuais/
unzip Schemas.zip
cd ..
mkdir issnet-teste
cd issnet-teste/
mkdir -p issnet/v1_0
mv ../Manuais/Schemas/* issnet/v1_0/

erpbrasil-edoc-gen-generate-python -n issnet -v v1.0 -s . -d .

ls issnetlib/v1_0/
