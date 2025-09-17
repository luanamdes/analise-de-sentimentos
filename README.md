### Análise de Sentimentos — Avaliações do Spotify na App Store

Oiiii!! Este projeto tem como objetivo aplicar os conhecimentos de Azure Language Studio para realizar uma análise de sentimentos sobre as **três primeiras avaliações** que aparecem na página do aplicativo Spotify na **Apple App Store**, documentando os processos, resultados, dificuldades e aprendizados.

### Mais detalhes

- Ferramenta de análise: **Azure Language Studio**
- Aplicativo: **Spotify: música e podcasts**
- Plataforma: Apple App Store  
- Avaliações: as três primeiras avaliações públicas que aparecem atualmente na página do aplicativo.
- Data da coleta: 16/09/2025
- Idioma das avaliações: Português e Inglês
<img width="1002" height="358" alt="image" src="https://github.com/user-attachments/assets/62235532-4db6-4e23-b8be-ead3cc036de4" />
<img width="1009" height="318" alt="image" src="https://github.com/user-attachments/assets/4c44015e-5e2c-493c-9739-0013b8accd4a" />

### Processo

#### 1. Pré-processamento
Antes de enviar o texto para análise de sentimentos, foi realizada de forma manual:
- Extração dos textos das três avaliações. 
- Remoção de emojis, para limpeza de texto.
- Identificação de idioma, para configurar o modelo certo de análise.

#### 2. Ferramenta
Através do Azure Language Studio (versão 2023-04-01), foi utilizado o serviço de **Sentiment Analysis and Opinion Mining**.
Para essa análise, definimos as seguintes configurações:
- Ativação do Opinion Mining.
- Definição do idioma para cada texto (Português ou Inglês).

#### 3. Análise 

Resultado da análise da Avaliação 1:

<img width="577" height="496" alt="image" src="https://github.com/user-attachments/assets/3c8d9572-6a42-4783-9852-9987347259e6" />


Resultado da análise da Avaliação 2:

<img width="700" height="507" alt="image" src="https://github.com/user-attachments/assets/8c9f9cdf-0a97-418d-b835-e2e933794456" />
<img width="684" height="335" alt="image" src="https://github.com/user-attachments/assets/76ba3e3a-c513-4d32-b3aa-41d3cdaa9851" />


Resultado da análise da Avaliação 3:

<img width="775" height="507" alt="image" src="https://github.com/user-attachments/assets/f3a4e2fd-8725-4a34-9d92-359c85c76357" />
<img width="766" height="307" alt="image" src="https://github.com/user-attachments/assets/2aba80db-1c9b-4016-9ccb-2616375ae497" />
<img width="789" height="529" alt="image" src="https://github.com/user-attachments/assets/8deb8626-6a1d-43ba-91fc-186731492409" />


### Resultados

Comparando os resultados das análises de sentimento de cada texto, é possível retirar de cada avaliação:
- Avaliação 1: 100.00% Positive - 0.00% Neutral - 0.00% Negative
- Avaliação 2: 39.00% Positive - 0.00% Neutral - 61.00% Negative
- Avaliação 3: 0.00% Positive - 0.00% Neutral - 100.00% Negative

### Aprendizados

- É possível perceber que nem sempre o sentimento analisado no texto de avaliação corresponde à nota atribuida ao aplicativo pelo usuário. Na avaliação 2, onde a análise revela uma avaliação 39% positiva e 61% negativa, o usuário atribuiu ao aplicativo uma nota 5 de 5 estrelas, enquanto na Avaliação 3, onde a análise revela uma avaliação 0% positiva e 100% negativa, o usuário atribuiu ao aplicativo 2 de 5 estrelas. 
- Também é possível observar na Avaliação 3 que não temos o resultado do Opinion Mining em algumas frases, pois a ferramenta não localiza o alvo das avaliações. 

### Dificuldades 

- Realização do pré-processamento de forma manual, reduzindo a velocidade do processo.
- Algumas avaliações estavam em inglês e outras em português, exigindo a alteração manual do idioma no Azure Language Studio ao inserir cada texto.  
- O Opinion Mining não conseguiu identificar o alvo em certas frases, limitando a análise mais detalhada.  

### Conclusão

- A prática demonstrou como ferramentas de Inteligência Artificial podem auxiliar na análise de feedback de usuários.  
- Foi possível identificar sentimentos gerais e opiniões específicas, além de observar inconsistências entre as notas atribuídas e o sentimento detectado.  
- Esse tipo de solução pode ser aplicado por empresas para entender melhor seus clientes, detectar insatisfações e mapear pontos fortes e fracos do produto.  
