# 📦 Previsão de Tempo de Entrega com Machine Learning

Este projeto utiliza técnicas de aprendizado de máquina para prever o tempo de entrega (em minutos) com base em variáveis como tipo de transporte, tráfego, região e distância percorrida.

## 📊 Objetivo

Criar um modelo preditivo capaz de estimar o tempo de entrega de um pedido com base em dados históricos. Isso pode ajudar empresas logísticas a otimizarem rotas, preverem atrasos e tomarem decisões mais estratégicas.

---

## 📁 Dados Utilizados

O dataset inclui os seguintes campos:

- **Distancia (km)**: distância total da entrega.
- **Tipo de Transporte**: bicicleta, caminhão, moto ou van.
- **Tráfego**: intensidade do tráfego (leve, moderado ou pesado).
- **Região**: região de entrega (centro, subúrbio ou zona rural).
- **Tempo de Entrega (min)**: valor real do tempo da entrega.

---

## ⚙️ Técnicas Utilizadas

- 📦 **Pandas** e **NumPy** para manipulação de dados.
- 📊 **Matplotlib** para visualização.
- ⚙️ **LabelEncoder** para transformar variáveis categóricas em numéricas.
- 🤖 **Linear Regression (Regressão Linear)** para criar o modelo preditivo.
- 🧪 **Train/Test Split** para avaliar o desempenho do modelo.
- 📈 **Métricas**: MSE (Erro Quadrático Médio) e R² (Coeficiente de Determinação).

---

## 🔍 Exemplo de Previsão

Você pode fazer previsões informando os seguintes dados (exemplo no código):

```python
# Tipo de Transporte | Tráfego | Região | Distância (km)
# BICICLETA = 0 | CAMINHÃO = 1 | MOTO = 2 | VAN = 3
# LEVE = 0 | MODERADO = 1 | PESADO = 2
# CENTRO = 0 | SUBÚRBIO = 1 | ZONA RURAL = 2

dados_novos = pd.DataFrame([[1, 2, 0, 50]], columns=['Tipo de Transporte', 'Trafego', 'Regiao', 'Distancia (km)'])
previsao = modelo.predict(dados_novos)
print(f"Tempo estimado de entrega: {previsao[0]:.2f} minutos")
