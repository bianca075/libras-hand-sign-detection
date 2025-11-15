# LIBRAS Hand Sign Detection

Sistema de detecção de sinais manuais (letras do alfabeto em LIBRAS) utilizando visão computacional e técnicas de aprendizado de máquina, com captura em tempo real via webcam.

#

## 1. Descrição Geral

Este projeto tem como objetivo a detecção de sinais manuais, com foco na representação de letras do alfabeto, utilizando técnicas de visão computacional e aprendizado de máquina.

A aplicação utiliza imagens capturadas por webcam para treinar um modelo de reconhecimento e realizar a inferência de letras da linguagem de sinais. Tem o objetivo de desenvolver um sistema capaz de identificar letras representadas com as mãos, utilizando modelos treinados com imagens reais.

As tecnologias utilizadas foram:

- Python 3.10.11
- OpenCV
- TensorFlow / Keras
- NumPy
- cvzone (módulo para rastreamento de mão)
- MediaPipe (biblioteca auxiliar utilizada pelo cvzone)

#

## 2. Objetivos do Projeto

- Capturar imagens de sinais manuais (letras do alfabeto) por meio de webcam.
- Treinar um modelo de machine learning para reconhecer letras da linguagem de sinais.
- Realizar inferência em tempo real, identificando a letra correspondente ao sinal exibido pela mão.
- Utilizar validação cruzada e ajuste automático de hiperparâmetros para melhorar o desempenho do modelo.

Espera-se que, ao mostrar um sinal de mão correspondente a uma das letras treinadas, o sistema consiga identificar corretamente qual letra está sendo representada, com um nível adequado de acurácia.

#

## 3. Funcionalidades Principais

- Captura de imagens de mão via webcam.
- Pré-processamento das imagens para uso no treinamento.
- Treinamento de um modelo de classificação de letras.
- Validação cruzada com re-treinamento utilizando diferentes divisões de treino e teste.
- Ajuste automático de hiperparâmetros, como taxa de aprendizado e número de épocas.
- Inferência em tempo real com exibição da letra reconhecida na tela.

#

## 4. Tecnologias e Dependências

- Python 3.10.11
- OpenCV
- TensorFlow / Keras
- NumPy
- cvzone
- MediaPipe

Todas as dependências necessárias estão listadas no arquivo:

- `requirements.txt`

#

## 5. Estrutura do Projeto

Ajuste esta seção conforme a estrutura real do repositório. Exemplo:

- `libras_classifier.py` – script responsável pelo treinamento do modelo, validação cruzada e ajuste de hiperparâmetros.
- `test.py` – script responsável pela inferência em tempo real com uso da webcam.
- `requirements.txt` – arquivo com a lista de dependências do projeto.
- `models/` – diretório opcional para armazenamento de modelos treinados.
- `data/` – diretório opcional para armazenamento do conjunto de dados (imagens) utilizado no treinamento.

#

## 6. Pré-requisitos

Antes de executar o projeto, recomenda-se utilizar a versão Python 3.10.11, devido à compatibilidade com TensorFlow e demais bibliotecas empregadas.

O Python 3.10.11 pode ser obtido no site oficial:

https://www.python.org/downloads/release/python-31011/

#

## 7. Instalação e Configuração do Ambiente

### 7.1 Clonar o Repositório

```bash
git clone https://github.com/bianca075/libras-hand-sign-detection.git
cd libras-hand-sign-detection
```

### 7.2 Criar e Ativar o Ambiente Virtual

Windows:

```bash
python -m venv venv
venv\Scriptsctivate
```

Linux / macOS:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 7.3 Instalar as Dependências

Com o ambiente virtual ativado, execute:

```bash
pip install -r requirements.txt
```

#

## 8. Execução do Projeto

### 8.1 Treinamento e Validação do Modelo

É possível realizar uma validação cruzada com re-treinamento, em que o conjunto de dados é dividido em várias partes. O modelo é treinado e testado várias vezes, cada vez com uma combinação diferente de dados de treino e teste.

Essa etapa é executada com o comando:

```bash
python libras_classifier.py
```

Nessa fase, também são ajustados automaticamente alguns hiperparâmetros, como:

- taxa de aprendizado (learning rate);
- número de épocas (epochs).

O objetivo é encontrar a configuração que produz os melhores resultados de desempenho para o modelo.

### 8.2 Inferência em Tempo Real com Webcam

Com o modelo treinado, é possível testar a detecção dos sinais em tempo real utilizando a webcam:

```bash
python test.py
```

Ao executar esse comando:

- a webcam será ativada;
- o modelo tentará reconhecer, em tempo real, a letra correspondente ao sinal capturado pela mão;
- a letra detectada será exibida na tela.

#

## 9. Resultados Esperados

- Reconhecimento das letras do alfabeto utilizadas no conjunto de treinamento.
- Bom desempenho de classificação em cenários controlados (iluminação adequada e enquadramento correto da mão).
- Capacidade de generalização para novas imagens que sigam o mesmo padrão de captura.

#

## 10. Possíveis Melhorias Futuras

- Ampliação do conjunto de letras, inclusão de números ou sinais completos.
- Expansão e diversificação do conjunto de dados de imagens.
- Otimização da arquitetura do modelo para maior desempenho e menor tempo de inferência.
- Desenvolvimento de uma interface gráfica (GUI) para facilitar o uso por usuários não técnicos.
- Empacotamento da aplicação para distribuição em diferentes plataformas.
