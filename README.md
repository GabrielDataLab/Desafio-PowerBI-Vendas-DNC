# Dashboard de Vendas em Power BI - Desafio DNC

Este projeto foi desenvolvido como o desafio final do módulo de "Introdução a análise de Dados" da Escola DNC (https://www.escoladnc.com.br/), onde recebi nota máxima. O objetivo foi criar um dashboard completo para analisar indicadores de vendas e o perfil dos clientes de uma empresa fictícia.

## 1. Ferramentas Utilizadas
* **Power BI:** Ferramenta principal para a criação do relatório, visuais e cálculos.
* **Power Query:** Utilizado para todo o processo de ETL (Extração, Transformação e Carga dos dados).
* **DAX (Data Analysis Expressions):** Para a criação de medidas personalizadas e cálculos mais robustos.

## 2. Processo de Desenvolvimento
O projeto seguiu um fluxo estruturado de Business Intelligence, dividido em 3 etapas:

### a. Tratamento e Limpeza dos Dados (ETL)
No Power Query, realizei o tratamento inicial dos dados, que incluiu:
- **Correção de Dados Categóricos:** Substituição de valores incorretos como "Mobil" por "Mobile".
- **Remoção de Duplicatas:** Garanti a unicidade dos registros na tabela de clientes para permitir a criação de um modelo relacional correto.
- **Verificação de Tipos de Dados:** Ajuste dos tipos de dados de cada coluna (texto, número, data).

### b. Modelagem de Dados
- Ajustei a propriedade de "Resumo Padrão" da coluna `idcompra` de "Soma" para **"Não resumir"**, corrigindo um problema fundamental que inflava os cálculos de contagem.

### c. Criação dos Visuais e Medidas DAX
- Desenvolvi KPIs para os principais indicadores: Quantidade de Vendas, Valor Total com e sem frete.
- Criei a medida `Quantidade de Vendas = DISTINCTCOUNT('base compra'[idcompra])` para garantir a contagem correta de transações únicas.
- Configurei gráficos de linha com eixos de tempo contínuos e gráficos de coluna para análise por categoria.

## 4. Visualização Final do Dashboard
![Dashboard de Vendas](![RID220310_Desafio01-1](https://github.com/user-attachments/assets/98de2a49-fe8b-4b45-8317-13adb2da8758)
)

---
