import pandas as pd
import matplotlib.pyplot as plt

# Criando um conjunto de dados fictício sobre o impacto do desmatamento
dados = {
    'Ano': [2000, 2005, 2010, 2015, 2020],
    'Área Desmatada (milhões de hectares)': [10, 12, 14, 18, 25],
    'Emissões de CO2 (milhões de toneladas)': [50, 55, 60, 70, 95],
    'Número de Espécies Ameaçadas': [200, 220, 250, 300, 350],
    'Temperatura Média (°C)': [0.4, 0.45, 0.5, 0.55, 0.6]  # Temperatura média global aumentada por causa do desmatamento
}

# Convertendo para um DataFrame
df = pd.DataFrame(dados)

# Exibindo os dados no terminal
print("Dados sobre o impacto do desmatamento:")
print(df)

# Gráfico 1: Área desmatada ao longo do tempo
plt.figure(figsize=(10, 6))
plt.plot(df['Ano'], df['Área Desmatada (milhões de hectares)'], marker='o', color='g', label='Área Desmatada')
plt.title('Área Desmatada ao Longo do Tempo')
plt.xlabel('Ano')
plt.ylabel('Área Desmatada (milhões de hectares)')
plt.grid(True)
plt.legend()
plt.show()

# Gráfico 2: Emissões de CO2 devido ao desmatamento
plt.figure(figsize=(10, 6))
plt.plot(df['Ano'], df['Emissões de CO2 (milhões de toneladas)'], marker='o', color='r', label='Emissões de CO2')
plt.title('Emissões de CO2 ao Longo do Tempo')
plt.xlabel('Ano')
plt.ylabel('Emissões de CO2 (milhões de toneladas)')
plt.grid(True)
plt.legend()
plt.show()

# Gráfico 3: Número de espécies ameaçadas
plt.figure(figsize=(10, 6))
plt.plot(df['Ano'], df['Número de Espécies Ameaçadas'], marker='o', color='b', label='Espécies Ameaçadas')
plt.title('Número de Espécies Ameaçadas ao Longo do Tempo')
plt.xlabel('Ano')
plt.ylabel('Número de Espécies Ameaçadas')
plt.grid(True)
plt.legend()
plt.show()

# Gráfico 4: Aumento da Temperatura Média Global
plt.figure(figsize=(10, 6))
plt.plot(df['Ano'], df['Temperatura Média (°C)'], marker='o', color='orange', label='Temperatura Média Global')
plt.title('Aumento da Temperatura Global devido ao Desmatamento')
plt.xlabel('Ano')
plt.ylabel('Temperatura Média (°C)')
plt.grid(True)
plt.legend()
plt.show()

# Mostrar o impacto do desmatamento em um único gráfico (comparativo)
plt.figure(figsize=(10, 6))
plt.plot(df['Ano'], df['Área Desmatada (milhões de hectares)'], marker='o', color='g', label='Área Desmatada')
plt.plot(df['Ano'], df['Emissões de CO2 (milhões de toneladas)'], marker='o', color='r', label='Emissões de CO2')
plt.plot(df['Ano'], df['Número de Espécies Ameaçadas'], marker='o', color='b', label='Espécies Ameaçadas')
plt.plot(df['Ano'], df['Temperatura Média (°C)'], marker='o', color='orange', label='Temperatura Média Global')
plt.title('Impacto do Desmatamento ao Longo do Tempo')
plt.xlabel('Ano')
plt.ylabel('Valores')
plt.grid(True)
plt.legend()
plt.show()
