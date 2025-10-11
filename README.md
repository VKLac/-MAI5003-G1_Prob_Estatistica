# MAI5003 – Probabilidade e Estatística (G1)

Repositório do projeto da disciplina de **Probabilidade e Estatística** do Mestrado Profissional em Estatística, Computação e Matemática da USP.  

## 🖥️ Projeto
**Tema:** Limpeza e Pré-Processamento de Dados  
**Objetivo:** realizar a leitura, análise inicial e limpeza de um dataset de datacenter (720 linhas × 12 colunas).  

---

## 📂 Metadados do Dataset

| Coluna                  | Tipo            | Descrição                          |
|--------------------------|-----------------|------------------------------------|
| timestamp                | datetime64[ns] | Ano, mês e dia do evento           |
| hora_dia                 | int64          | Hora do evento                     |
| dia_semana               | int64          | Dia da semana                      |
| reqs                     | int64          | Número de requisições via app      |
| trafego_MBps             | int64          | Tráfego de dados (MBps)            |
| usuarios_ativos          | int64          | Quantidade de usuários ativos      |
| temp_ambiente_C          | float64        | Temperatura ambiente (°C)          |
| uso_cpu_%                | float64        | Percentual de uso da CPU           |
| uso_ram_%                | float64        | Percentual de uso da RAM           |
| demanda_energia_KW       | float64        | Demanda energética estimada        |
| pressao_resfriamento_bar | float64        | Pressão de resfriamento (bar)      |
| consumo_agua_m3          | float64        | Consumo de água (m³)               |

---

## 🛠️ Metodologia

1. **Análise inicial**
   - Verificação da tipagem dos dados  
   - Identificação de valores ausentes, duplicados ou inconsistentes  

2. **Tratamento de nulos**
   - Heatmap com *missingno*  
   - Correlação de Spearman aplicada a variáveis de ausência  

3. **Ajustes temporais**
   - Reconstrução da sequência contínua de `timestamp`  
   - Criação de variáveis derivadas: `hora_dia` e `dia_semana`  

4. **Interpolação**
   - Definição de `timestamp` como índice temporal  
   - Interpolação baseada em tempo para colunas com nulo