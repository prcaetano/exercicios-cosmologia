# Exercícios cosmologia
Este diretório contêm os exercícios teóricos e computacionais do curso de Cosmologia do Prof. Saulo.

## Instalação e configuração

### Usando pip

Os exercícios computacionais foram feitos utilizando o Jupyter. Para rodá-los é necessário instalar algumas dependências.
Usando pip, basta fazer

```
pip install -r requirements.txt
```

neste diretório, e, uma vez instaladas as dependências, rodar

```
jupyter notebook
```

Um jeito prático de instalar as dependências sem correr o risco de quebrar o sistema é utilizando o [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/). Neste caso basta fazer


```
mkvirtualenv curso-cosmologia
workon curso-cosmologia
pip install -r requirements.txt
jupyter notebook
```

Para fechar o jupyter, basta dar Ctrl-C no terminal e sair do ambiente usando

```
deactivate
```

### Usando conda

Com conda, crie um novo ambiente conda e, dentro dele, um ambiente pip. Siga então as instruções da seção anterior.

```
conda create --name curso-cosmologia
conda install -n curso-cosmologia pip
source activate curso-cosmologia
pip install -r requirements.txt
```

### Instalação do CLASS

Não é possível instalar CLASS 2.6.3 usando apenas o pip. Uma possibilidade é clonar o [repositório git do CLASS](https://github.com/lesgourg/class_public), compilá-lo e, uma vez no ambiente virtual criado, instalar o wrapper python.

```
git clone https://github.com/lesgourg/class_public.git
git checkout tags/v2.6.3
cd class_public
make clean
make
workon curso-cosmologia
python setup.py install
python -c 'from classy import Class'
```

Se a última etapa procedeu sem erros está tudo certo.

