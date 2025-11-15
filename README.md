Este projeto tem como objetivo a detecção de sinais manuais, com foco na representação de letras do alfabeto, utilizando técnicas de visão computacional e aprendizado de máquina. A aplicação utiliza imagens capturadas por webcam para treinar um modelo de reconhecimento e realizar a inferência de letras da linguagem de sinais. Tem o objtivo de desenvolver um sistema capaz de identificar letras representadas com as mãos, utilizando modelos treinados com imagens reais.
As Tecnologias utilizadas foram o Python 3.x, OpenCV, TensorFlow/Keras, NumPy, cvzone (módulo para rastreamento de mão), MediaPipe (biblioteca auxiliar do cvzone)
Para executar o código são necessárias algumas etapas:
1. Baixar o python 3.10.11, que pode ser baixado no link abaixo
[# HandSignDetection](https://www.python.org)
2. Instalação de Dependências
Execute o seguinte comando no terminal para instalar as dependências do projeto:
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt

Com o modelo treinado, é possível testar a detecção dos sinais com o comando "python test.py", a webcam será ativada, e o modelo tentará reconhecer em tempo real a letra correspondente ao sinal da mão capturado. Também conseguimos realizEa uma validação cruzada com re-treinamento, onde o conjunto de dados é dividido em várias partes. O modelo é treinado e testado várias vezes, cada vez com uma combinação diferente de dados de treino e teste, vemos isso com o comando "python libras_classifier.py"

Nessa etapa, também são ajustados hiperparâmetros automaticamente, como taxa de aprendizado e número de épocas, pra encontrar a configuração que gera os melhores resultados.
Espera-se que, ao mostrar um sinal de mão correspondente a uma das letras treinadas, o sistema consiga identificar corretamente qual letra está sendo representada, com um bom nível de acurácia.
