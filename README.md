## Work - Fenômenos de Transporte

### Objetivos

- Extração automática de dados a partir do site da [ONS](https://dados.ons.org.br/dataset/).
- EDA a partir de dados de séries temporais de vazões (m³/s).
- Interpretabilidade de fatores impactantes, como: sazonalidade, autocorrelação, séries residuais, tendênciasi e etc.
- Uso/criação de modelos de ML/DL, realizando uma comparação entre eles (visual e numérica, usando métricas como: RMSE, MAE) para previsão de vazões baseados em dados mensais de vazões no passado.
- Modelos utilizados nessa análise: baseados em redes neurais (LSTM), baseados em arvores (XGBOOST), tradicionais (SARIMA, ARIMA, PROPHET).

### Fonte dos dados
Origem (open-source): Operador Nacional do Sistema Elétrico - ONS

### Conclusões

Apesar da tarefa de times series forecasting ser algo dificil ou de dificil otimização, sendo bem recorrente no mundo de ciência de dados, conseguimos atingir bons resultados durante nossos testes e com pouco esforço computacional (apesar de não monitorado através de gráficos e números, foi notado empericamente o baixo consumo de RAM e uso da GPU, tanto que em nenhum momento do código eu uso técnicas de processamento paralelo ou uso da gpu - até mesmo para a LSTM). Com uma salva exceção para o modelo XGBOOST que, apesar de não ser baseado em redes neurais demonstrou maiores robustez até mesmo que a LSTM. A seguir, acompanhe algumas previsões de vazõe em 12 meses futuros usando diferentes modelos para o reservatório **ITAPEBI**:

## LSTM
![](results\lstm_ITAPEBI.png) 

## XGBOOST
![](results\XGBOOST_ITAPEBI.png) 

## ARIMA
![](results\ARIMA_ITAPEBI.png) 

## SARIMA
![](results\SARIMA_ITAPEBI.png) 

## PROPHET
![](results\PROPHET_ITAPEBI.png) 