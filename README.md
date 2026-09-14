# Pipeline Preditivo MNIST

Disclaimer: README criado com IA e revisado por um humano ao fim do projeto, erros são possíveis e justificáveis, haha.

## Vídeo de apresentação

🎥 [Assista aqui](https://drive.google.com/file/d/1JGVFxnc57ZuwTVOMqT3mrQGqm7fZNkyX/view?usp=drive_link)

## Sobre o projeto

Este projeto implementa um pipeline de Ciência de Dados ponta a ponta para classificação de dígitos manuscritos (0 a 9), utilizando o dataset MNIST. Além de treinar e comparar modelos, o projeto testa a robustez e a capacidade de generalização diante de cenários fora do padrão de treino, incluindo classes nunca vistas e imagens manuscritas reais produzidas pelo autor.

## Tecnologias e técnicas utilizadas

- Python, executado em Google Colab
- scikit-learn (fetch_openml, KNN, Random Forest, MLP, MinMaxScaler, métricas de classificação)
- pandas e numpy para manipulação de dados
- matplotlib e seaborn para visualização
- PIL (Pillow) para pré-processamento de imagens manuscritas
- Photopea para criação das imagens manuscritas próprias (28x28, fundo preto, traço branco)

## Estrutura do projeto

- **Fase 1:** Carregamento do dataset e Análise Exploratória (EDA)
- **Fase 2:** Divisão estratificada treino/teste (80/20) e normalização via MinMaxScaler
- **Fase 3:** Treinamento de 3 modelos (KNN, Random Forest e MLP) com ajuste de hiperparâmetros
- **Fase 4:** Avaliação comparativa de desempenho (matrizes de confusão e métricas). Modelo recomendado: Random Forest
- **Fase 5.1 e 5.2:** Teste de robustez com mascaramento de classes (dígitos 4 e 7 ocultados do treino) e avaliação do comportamento em inferência fora da distribuição (OOD)
- **Fase 5.3:** Inferência com imagens manuscritas próprias, incluindo pré-processamento (escala de cinza, centralização por bounding box, normalização) e visualização das probabilidades preditas

## Como executar

1. Abra o notebook `NeyPeres_MiniProjeto.ipynb` no Google Colab.
2. Execute as células em ordem, de cima para baixo (Ambiente de execução > Executar tudo).
3. Na Fase 5.3, quando solicitado, faça upload das suas próprias imagens de dígitos manuscritos (28x28 pixels, fundo preto e traço branco).
4. As saídas (gráficos, métricas e previsões) são geradas automaticamente ao longo da execução.

## Possíveis melhorias

- Utilizar uma rede neural convolucional (CNN), naturalmente mais robusta a pequenas variações de posição e traço.
- Salvar os modelos treinados (via joblib/pickle) para evitar retreinamento a cada execução.
- Ampliar o conjunto de imagens manuscritas próprias para uma avaliação estatisticamente mais robusta.

## Autor

Ney Peres
