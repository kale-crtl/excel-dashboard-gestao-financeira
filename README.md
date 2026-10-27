# 📊 Dashboard de Gestão Financeira e Controle de Custos (Excel)

Painel executivo interativo desenvolvido no **Microsoft Excel**, focado na consolidação de transações financeiras, análise de desvios orçamentários (*Budget vs. Actual*) e automação de indicadores para tomada de decisão gerencial.

---

## 🖼️ Prévia do Projeto


![Prévia do Dashboard Financeiro](PROJETO%20EXCEL.png)


---

## 🎯 Objetivo do Negócio
O projeto foi estruturado para resolver um problema comum nas empresas: a descentralização de dados financeiros e a falta de visibilidade rápida sobre os custos. Ele permite:
- Monitorar o fluxo entre valores realizados e orçados por categoria e centro de custo.
- Identificar rapidamente desvios financeiros através de relatórios e gráficos dinâmicos.
- Oferecer uma interface limpa e intuitiva para gestores analisarem a saúde financeira da operação.

---

## 🏗️ Arquitetura da Planilha
A workbook foi dividida em três abas funcionais para garantir boas práticas de modelagem de dados:

1. **`BD_Lancamentos` (Base de Dados)**
   - Tabela estruturada do Excel (`Ctrl + T`) contendo os registros transacionais.
   - Colunas implementadas: `Data`, `Categoria`, `Tipo` (Receita/Despesa), `Centro de Custo`, `Valor Realizado`, `Valor Orçado`, `Status` e a coluna calculada de **`Desvio`**.

2. **`DRE_Resumo` (Tabela de Apoio e Consolidação)**
   - Aba dedicada ao resumo financeiro por categoria.
   - Utilização de fórmulas condicionais avançadas para puxar automaticamente os valores da base bruta.

3. **`Dashboard` (Painel Executivo Visual)**
   - Interface principal do usuário.
   - Design moderno com remoção de linhas de grade para um acabamento corporativo limpo.
   - Gráfico de colunas agrupadas comparando o Realizado versus o Orçado.
   - Segmentação de dados (Slicers) para filtragem interativa e dinâmica.

---

## 🛠️ Tecnologias, Funções e Recursos Aplicados
- **Modelagem e Tabelas Estruturadas:** Conversão de bases brutas em tabelas dinâmicas do Excel com referências estruturadas.
- **Funções de Lógica e Soma Condicional:** 
  - `=SOMASE(BD_Lancamentos[Categoria]; A2; BD_Lancamentos[Valor Realizado])`
- **Operações Matemáticas e Colunas Calculadas:** Cálculo automático de variações financeiras (`[@[Valor Realizado]] - [@[Valor Orçado]]`).
- **Data Visualization & UI/UX:** Gráficos comparativos customizados, formatação monetária padrão e paleta de cores executiva.
- **Interatividade:** Implementação de Filtros / Segmentadores de Dados conectados aos relatórios.

---

## 📂 Estrutura do Repositório
- `Dashboard_Financeiro.xlsx` — Ficheiro completo com toda a estrutura, fórmulas e gráficos.
- `dashboard-financeiro.jpg` — Captura de tela em alta resolução do painel final.
- `README.md` — Documentação técnica do projeto.

---

## 🚀 Como Utilizar
1. Faça o download do ficheiro **`Dashboard_Financeiro.xlsx`**.
2. Abra o ficheiro no Microsoft Excel.
3. Navegue até à aba **`BD_Lancamentos`** para adicionar ou atualizar novos lançamentos financeiros na tabela estruturada.
4. Explore o **`Dashboard`** para interagir com os gráficos e filtros de categoria.
