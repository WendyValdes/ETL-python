# 🚀 ETL com Python | Santander Dev Week 2023 (Adaptado)

## 📌 Sobre o Projeto

Este projeto implementa um pipeline completo de **ETL (Extract, Transform, Load)** utilizando Python.

A proposta original utilizava uma API que atualmente está indisponível. Como alternativa, foi utilizado um dataset real do Banco Mundial via KaggleHub, garantindo a continuidade do fluxo de dados com uma fonte confiável.

---

## 🎯 Objetivo

Demonstrar na prática:

- Extração de dados de fonte externa
- Transformação e enriquecimento dos dados
- Geração de mensagens personalizadas (simulação de IA)
- Carregamento e persistência dos dados processados

---

## 🧱 Arquitetura do Pipeline

KaggleHub Dataset  
        ↓  
     Extract  
        ↓  
    Transform  
        ↓  
       Load  
        ↓  
   CSV Final  

---

## 🔄 Etapas do ETL

### 🟢 Extract

- Download do dataset via KaggleHub
- Leitura de dados com Pandas

```python
path = kagglehub.dataset_download("nilaychauhan/world-bank-datasets")
df = pd.read_csv(full_path, header=2)
```

### 🟡 Transform
Estruturação dos dados no formato esperado
Simulação de IA para geração de mensagens personalizadas
Enriquecimento dos dados com insights
``` def generate_ai_news(user):
    return f"{user['name']}, investir é essencial para crescimento econômico."
```

### 🔵 Load
Conversão dos dados para formato tabular
Exportação para arquivo .csv
```
final_df.to_csv('resultado_worldbank_etl.csv', index=False)
```

## 📊 Tecnologias Utilizadas
Python
Pandas
KaggleHub
Google Colab
📁 Estrutura de Saída

O pipeline gera um arquivo final contendo:
ID do usuário
Nome
Informação associada
Mensagem personalizada

##💡 Diferenciais do Projeto
Uso de dados reais do Banco Mundial 🌍
Adaptação do desafio original (resolução de problema real)
Pipeline ETL completo em uma única execução
Código simples, reutilizável e escalável

## 🚀 Possíveis Melhorias
Integração com API da OpenAI para geração real de texto
Armazenamento em banco de dados como MongoDB
Criação de dashboard no Power BI
Deploy como pipeline automatizado

🏁 Conclusão
Este projeto demonstra, de forma prática, a aplicação do fluxo ETL utilizando Python, reforçando conceitos essenciais de engenharia e ciência de dados, mesmo diante de limitações externas como indisponibilidade de APIs.
