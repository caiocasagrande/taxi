<p align="center">
  <img src="https://github.com/caiocasagrande/taxi/blob/main/images/portugal_map.png" alt="image">
</p>

# Previsão de pontos finais de trajetórias de táxi
Projeto de previsões de pontos de chegada em corridas de táxi na cidade do Porto, Portugal.

## Problema de Negócio
### Sobre o Negócio:
- Com as novas tecnologias atuais, a indústria de táxis precisou se reinventar para não ficar para trás em relação aos seus novos concorrentes;
- Um dos desafios é a adaptação ao novo sistema eletrônico de despacho em tempo real, instalados nos veículos.

### Sobre o Problema:
- O sistema conta com um problema: a falta de informação sobre o destino final das corridas, pois os motoristas não indicam o destino;
- Com as mensagens unicast (1:1) os despachantes precisam identificar corretamente qual táxi enviar para uma localização de coleta, o que se torna difícil quando não se sabe o destino final dos táxis em serviço;
Em razão desse problema, a proposta é desenvolver um modelo preditivo que seja capaz de inferir o destino final de corridas de táxi com base em suas localizações de coleta.

### Benefícios da solução:
Assim, é possível melhorar a eficiência do sistema de despacho eletrônico de taxistas, permitindo uma identificação ágil de qual motorista encaminhar para cada solicitação de corrida, especialmente durante períodos de alta demanda.

## Objetivos
- Entender o problema de negócio
- Análise de dados
- Modelo de previsão
- PowerPoint descrevendo o problema e conclusões
- Enviar notebook (.ipynb) e apresentação (.pdf)

## Dataset
...

## Análise Exploratória 

**Qual a distribução das viagens por dia?**
![image](https://github.com/caiocasagrande/taxi/blob/main/images/corridas_por_dia.png)
- É possível ver que as corridas acontecem em ondas pequenas de frequência;
- Agosto é um período com menos corridas por dia, provavelmente em razão do verão e pela cidade do Porto não ser um dos principais destinos nessa estação como o Algarve é.

**Qual o dia da semana com mais corridas? Qual dia se percorre as maiores distâncias?**
![image](https://github.com/caiocasagrande/taxi/blob/main/images/analise_semanal.png)
- O dia em que acontece mais viagens é a sexta-feira, seguida pelo sábado e pela quinta-feira;
- Por outro lado, os dias com menos corridas são domingo e segunda-feira;
- Interessantemente, domingo é de longe o dia em que se percorre as maiores distâncias médias;
- Os outros dias não apresentam muita diferência nas distâncias médias, mas a segunda-feira está em segundo lugar enquanto a terça-feira é o dia com menores distâncias percorridas;
- Este resultado vai de encontro com as "pequenas ondas" vistas no ponto 6 (corridas por dia), onde os dias com mais corridas estão no final da semana.

  **Qual o comportamento das distâncias percorridas por hora do dia?**
![image](https://github.com/caiocasagrande/taxi/blob/main/images/analise_diaria.png)
- O maior volume de corridas acontece entre às 8h e às 10h da manhã, com uma diminuição no horário de almoço e retomada de um forte volume das 13h às 15h;
- A menor quantidade de corridas é realizada na madrugada, entre às 0h e às 6h;
- Por outro lado, as maiores distâncias médias percorridas estão nessa faixa de horário, mais precisamente das 3h às 6h;
- No resto do dia, as distâncias médias não oscilam tanto.

## Machine Learning
...

# Performances

## Performance do Modelo
- O modelo performou bem e com resultados satisfatórios. Contudo, a base utilizada para a modelagem foi apenas uma fração do total em razão de limites computacionais;
- Acredita-se que utilizando a base inteira, o modelo **LightGBM** possa prever com mais exatidão os pontos de destino;
- Ademais, incrementar o **GridSearchCV** com mais parâmetros também pode resultar em modelos mais precisos;
- Ainda assim, **o modelo resultou em bons resultados para a base de treino e resultados ainda melhores para o dataset de teste (erros menores).**

## Business Performance

Realizar a previsão do destino final de corridas de táxi com base em pontos iniciais pode trazer diversos benefícios financeiros à empresa, como:

**1. Minimização de quilometragem vazia:**
- Quilometragem vazia se refere aos quilômetros rodados por um táxi sem passageiros. Assim, prever o destino final com maior eficiência ajuda os motoristas a minimizarem essa quilometragem, enviando táxis para áreas onde provavelmente irão pegar novos passageiros após deixar os atuais. Esta prática também reduz o consumo de combustível e o desgaste dos veículos, gerando economia de custos.

**2. Maior satisfação do cliente:**
- A previsão otimizada de destinos pode levar a tempos de resposta mais rápidos, resultando em tempos de espera reduzidos para os clientes. Assim, a capacidade de resposta mais rápida contribui para uma maior satisfação do cliente e maior fidelidade.

**3. Otimização de recursos:**
- Saber o destino final permite que os táxis estejam disponíveis em áreas de alta demanda durante os horários de pico. Com o passar do tempo, a prática resulta em melhor utilização de recursos e aumento da receita.

**4. Mais viagens em menos tempo:**
- Com a otimização do serviço e dos tempos de espera, os táxis podem completar mais viagens em um menor período de tempo. O aumento no volume de viagens também contribui para uma maior geração de receita para a empresa.

**5. Planejamento operacional:**
- Com a análise de dados históricos e o constante melhoramento na previsão de futuras trajetórias, é possívelse programar melhor e gerenciar a frota de táxis conforme a demanda e os dias.

**6. Vantagem competitiva:**
- A capacidade de prever com precisão os destinos dos táxis e fornecer um serviço eficiente pode dar à empresa uma vantagem competitiva no mercado em relação aos seus concorrentes. Isso pode atrair mais clientes e ajudar a reter os existentes.
