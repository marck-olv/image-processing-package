# Projeto: Pacote de Processamento de Imagens
## Autora do Projeto: Karina Kato
### Aula: Projeto de Pacote de Processamento de Imagens em Python- Digital Innovation One
[(clique aqui para ver o meu perfil na plataforma)](https://web.digitalinnovation.one/users/marck_olv)
#### Tecnologia: Python
#### Data: 27/04/2023
-----------------------------------------
### Descri��o
O pacote "image_processing-test" � usado para:

- M�dulo "Processing":
  - Correspond�ncia de histograma;
  - Similaridade estrutural;
  - Redimensionar imagem;

- M�dulo "Utils":
  - Ler imagem;
  - Salvar imagem;
  - Plotar imagem;
  - Resultado do gr�fico;
  - Plotar histograma;
---------------------------------------------
## Passo a passo da configura��o para hospedar um pacote em Python no ambiente de testes Test Pypi

- [x] Instala��o das �ltimas vers�es de "setuptools" e "wheel"

```
py -m pip install --user --upgrade setuptools wheel
```
- [x] Tenha certeza que o diret�rio no terminal seja o mesmo do arquivo "setup.py"

```
C:\User\Marcos\image-processing-package> py setup.py sdist bdist_wheel
```

- [x] Ap�s completar a instala��o, verifique se as pastas abaixo foram adicionadas ao projeto:
  - [x] build;
  - [x] dist;
  - [x] image_processing_test.egg-info.

- [x] Basta subir os arquivos, usando o Twine, para o Test Pypi:

```
py -m twine upload --repository testpypi dist/*
```

- [x] Ap�s rodar o comando acima no terminal, ser� pedido para inserir o usu�rio e senha. Feito isso, o projeto estar� hospedado no Test Pypi.hosped�-lo no Pypi diretamente.

### � interessante em mente que o Test Pypi, como o pr�prio nome diz, � apenas um ambiente de testes. Para que o projeto esteja dispon�vel como um pacote para ser usado publicamente, � necess�rio hosped�-lo no site oficial do Pypi.
----------------------------------------------------
## Instala��o local, ap�s hospedagem no Test Pypi

- [x] Instala��o de depend�ncias
```
pip install -r requirements.txt
```

- [x] Instal��o do Pacote

Use o gerenciador de pacotes ```pip install -i https://test.pypi.org/simple/ image-processing-test ```para instalar image_processing-test

```bash
pip install image-processing-test
```
-------------------------------------------------
## Como usar em qualquer projeto

```python
from image-processing-test.processing import combination
combination.find_difference(image1, image2)
```
<img width="auto" src="https://github.com/henriqueotogami/image-processing-package/blob/master/image-processing-test.png?raw=true">

## Autor (quem hospedou o projeto no Test Pypi)
Marcos Alex Silva de Oliveira

## Licen�a
[MIT](https://choosealicense.com/licenses/mit/)