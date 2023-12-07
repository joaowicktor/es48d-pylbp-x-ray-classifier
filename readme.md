# PyLBP X-Ray Classifier

O projeto final da disciplina de Processamento de Imagens (ES48D) da Universidade Tecnológica Federal do Paraná (UTFPR) para classificação de imagens de raio-X divididas em duas classes: covid e normal.

## Equipe

- João Wicktor Ortiz de Campos

## Descritor implementado

- [LBP (Local Binary Pattern)](https://pyimagesearch.com/2015/12/07/local-binary-patterns-with-python-opencv/): é um método que compara os valores dos pixels de uma imagem com os seus vizinhos em uma vizinhança circular.

## Repositório do projeto

https://github.com/joaowicktor/es48d-pylbp-x-ray-classifier

## Instruções de uso

> O projeto foi desenvolvido e testado no Windows 11 com Python 3.11.7

1. Clone o projeto e entre no diretório

```bash
git clone https://github.com/joaowicktor/es48d-pylbp-x-ray-classifier
cd es48d-pylbp-x-ray-classifier
```

2. Configure o ambiente virtual (Opcional, mas recomendado)

```bash
python -m venv es48d

# No Linux
source es48d/bin/activate

# No Windows
es48d\Scripts\activate
```

3. Instale as dependências necessárias

```bash
pip install -r requirements.txt
```

4. Faça o download do [dataset](https://www.kaggle.com/datasets/tarandeep97/covid19-normal-posteroanteriorpa-xrays)

5. Descompacte o dataset com as pastas `covid` e `normal` na pasta `images_full`, caso não exista, crie-a na raiz do projeto

```bash
mkdir images_full
```

6. Prepare o dataset executando o script `data_splitting.py`

```bash
python data_splitting.py
```

7. Faça a extração das características das imagens usando LBP executando o script `lbp_feature_extraction.py`

```bash
python lbp_feature_extraction.py
```

8. Execute o script `run_all_classifiers.py` para treinar e testar os classificadores (MLP, SVM e Random Forest) e gerar os resultados finais

```bash
python run_all_classifiers.py
```

## Classificadores e acurácia

### MLP (Multi-Layer Perceptron)

![](https://github.com/joaowicktor/es48d-pylbp-x-ray-classifier/blob/main/results/mlp_classifier-06122023-2132.png?raw=true)

### SVM (Support Vector Machine)

![](https://github.com/joaowicktor/es48d-pylbp-x-ray-classifier/blob/main/results/svm_classifier-06122023-2132.png?raw=true)

### RF (Random Forest)

![](https://github.com/joaowicktor/es48d-pylbp-x-ray-classifier/blob/main/results/rf_classifier-06122023-2132.png?raw=true)

### Comparação de acurácia entre os classificadores

![](https://github.com/joaowicktor/es48d-pylbp-x-ray-classifier/blob/main/results/run_all_classifiers-06122023-2132.png?raw=true)