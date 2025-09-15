# Ciencia-de-Dados

## Tratamento de Dados

Este notebook tem como objetivo aplicar **técnicas de tratamento e limpeza de dados** em um dataset para torná-lo adequado para análises posteriores.

## 📌 Etapas realizadas

1. **Importação de bibliotecas**  
   - `pandas`, `numpy`, `matplotlib`, `seaborn` para manipulação e visualização de dados.

2. **Carregamento dos dados**  
   - Montagem do Google Drive para acessar os arquivos.  
   - Leitura de um arquivo `.csv` contendo os dados.  
   - Criação de um DataFrame com `pandas`.

3. **Análise inicial do DataFrame**  
   - Visualização das primeiras linhas com `head()`.  
   - Identificação dos tipos de dados das colunas.  

4. **Conversão de tipos incorretos**  
   - Conversão da coluna `Idade` de `float64` → `int64`.  
   - Conversão da coluna `Data_Compra` de `object` → `datetime64`.  
   - Ajuste da coluna `Preço` para formato numérico correto (troca de vírgula por ponto).

5. **Tratamento de valores nulos**  
   - Contagem dos valores ausentes por coluna.  
   - Remoção de registros sem valor na coluna `Preço` (considerando que a compra não foi realizada).  
   - Preenchimento de valores nulos em outras colunas (ex.: `Idade` com mediana, etc.).

6. **Tratamento de duplicatas**  
   - Identificação e remoção de registros duplicados no dataset.

7. **Resultado final**  
   - Obtenção de um DataFrame limpo, com tipos de dados adequados, sem valores inválidos ou duplicados, pronto para análise exploratória ou modelagem.

---

## 🛠️ Tecnologias utilizadas
- [Python](https://www.python.org/)  
- [Pandas](https://pandas.pydata.org/)  
- [NumPy](https://numpy.org/)  
- [Matplotlib](https://matplotlib.org/)  
- [Seaborn](https://seaborn.pydata.org/)  

---

## 📂 Estrutura do notebook
- Importação e configuração  
- Leitura e análise inicial dos dados  
- Conversão de tipos  
- Tratamento de nulos  
- Remoção de duplicatas  
- DataFrame final tratado  

---

## 💻 Exemplos de Código

### Exemplo 1
```python
#Imports utilizados no Código
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### Exemplo 2
```python
# Configurando a conexão com o Google Drive
from google.colab import drive
drive.mount('/content/drive')
path = '/content/drive/MyDrive/Bases de dados/atividade3_dataset.csv'
```

### Exemplo 3
```python
#Criação de um DataFrame baseado em um arquivo .csv
df_csv = pd.read_csv(path)
df_csv
```

### Exemplo 4
```python
#Print dos 5 primeiros valores(Linhas) do DataFrame
df_csv.head()
```

### Exemplo 5
```python
df_csv_types = df_csv.dtypes
df_csv_types
```
