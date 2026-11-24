# Dashboard Executivo Financeiro — Veloce Logística & E-commerce S.A.

Aplicação de **Business Intelligence (BI)** desenvolvida em arquivo único (`HTML5`, `CSS3` e `JavaScript` com **Chart.js**) para acompanhamento executivo de resultados financeiros, mix de categorias e SLA logístico da empresa fictícia **Veloce Logística & E-commerce S.A.** (varejo digital de eletrônicos no Brasil) referente ao **1º Semestre de 2026 (Jan–Jun)**.

---

## 1. Estrutura e Funcionalidades do Painel

O dashboard foi organizado em **4 blocos visuais** para leitura executiva rápida:

1. **Cabeçalho & Filtros Dinâmicos**
   - Seletor de **Período** (`Todos os meses (Jan–Jun)` ou mês específico de `Janeiro/2026` a `Junho/2026`).
   - Seletor de **Região** (`Todas as Regiões`, `Sudeste`, `Sul`, `Nordeste`, `Centro-Oeste`, `Norte`).
   - Botão **Limpar Filtros** para retorno imediato à visão consolidada.

2. **KPIs Principais (Topo)**
   - **Receita Total** (com exibição do CMV correspondente).
   - **Lucro Líquido** (`Receita - CMV - Despesas` no consolidado nacional, com exibição das Despesas Operacionais).
   - **Margem Líquida (%)** (com comparativo em relação à meta corporativa de `≥ 12,0%`).
   - **Ticket Médio** (`Receita / Pedidos`, com volume total de pedidos).
   - Todos os cards exibem variação em relação ao mês anterior (ou `Jun vs. Mai` na visão consolidada do semestre).

3. **Área Central (Gráficos com Chart.js)**
   - **Gráfico Combinado (Barras + Linha):** Evolução mensal de **Receita Bruta** (barras) vs. **Lucro Líquido** (linha), com destaque visual quando um mês específico é filtrado e tooltip com margem líquida calculada.
   - **Gráfico de Rosca (Doughnut):** Participação da receita por categoria de produto, recalculada em reais (`R$`) conforme os filtros aplicados.

4. **Detalhamento & Alertas por Região (Base)**
   - Tabela interativa por região com ordenação por coluna (clicando nos cabeçalhos) e filtro cruzado (clicando em uma linha para filtrar todo o dashboard).
   - **Indicadores visuais (badges):**
     - 🟢 **Verde (Saudável):** Prazo `≤ 3,5 dias` e Margem `≥ 14,0%` (`Sudeste`, `Sul`).
     - 🟡 **Amarelo (Atenção):** Prazo `> 3,5 dias` ou Margem `< 14,0%` (`Centro-Oeste`).
     - 🔴 **Vermelho (Crítico):** Prazo `> 4,0 dias` ou Margem `< 12,0%` (`Nordeste`, `Norte`).

---

## 2. Base de Dados Embutida (1º Semestre de 2026)

### Desempenho Mensal Consolidado

| Mês | Receita Bruta | CMV | Despesas Op. | Lucro Líquido | Margem Líq. | Pedidos | Ticket Médio |
| :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Janeiro | R$ 420.000,00 | R$ 231.000,00 | R$ 110.000,00 | R$ 79.000,00 | 18,81% | 1.400 | R$ 300,00 |
| Fevereiro | R$ 390.000,00 | R$ 214.500,00 | R$ 108.000,00 | R$ 67.500,00 | 17,31% | 1.300 | R$ 300,00 |
| Março | R$ 465.000,00 | R$ 251.100,00 | R$ 115.000,00 | R$ 98.900,00 | 21,27% | 1.500 | R$ 310,00 |
| Abril | R$ 510.000,00 | R$ 275.400,00 | R$ 120.000,00 | R$ 114.600,00 | 22,47% | 1.645 | R$ 310,03 |
| Maio | R$ 540.000,00 | R$ 286.200,00 | R$ 124.000,00 | R$ 129.800,00 | 24,04% | 1.740 | R$ 310,34 |
| Junho | R$ 615.000,00 | R$ 325.950,00 | R$ 130.000,00 | R$ 159.050,00 | 25,86% | 1.980 | R$ 310,61 |
| **Total Semestre** | **R$ 2.940.000,00** | **R$ 1.584.150,00** | **R$ 707.000,00** | **R$ 648.850,00** | **22,07%** | **9.565** | **R$ 307,37** |

### Distribuição por Categoria e Região
- **Categorias:** Smartphones (`42%`), Notebooks & Periféricos (`31%`), Áudio & Wearables (`17%`) e Casa Inteligente (`10%`).
- **Regiões:** Sudeste (`54%` | Margem `16,2%` | `2,1 dias`), Sul (`22%` | Margem `15,8%` | `2,8 dias`), Nordeste (`14%` | Margem `11,4%` | `4,9 dias`), Centro-Oeste (`7%` | Margem `13,5%` | `3,6 dias`) e Norte (`3%` | Margem `9,1%` | `6,8 dias`).

---

## 3. Tecnologias Utilizadas

- **HTML5 & CSS3:** Layout responsivo com CSS Grid, Flexbox, tema corporativo claro (`#F8FAFC`), cards brancos e paleta em azul-marinho e verde-esmeralda.
- **JavaScript (ES6+):** Cálculos dinâmicos, filtros reativos, ordenação de tabela e formatação monetária via `Intl.NumberFormat('pt-BR')`.
- **Chart.js v4.4.4:** Carregado via CDN (`cdn.jsdelivr.net`) para renderização dos gráficos combinado e doughnut.

---

## 4. Como Executar

1. Faça o download ou clone dos arquivos do projeto.
2. Abra o arquivo `index.html` diretamente em qualquer navegador moderno (Chrome, Edge, Firefox) com acesso à internet para carregamento do **Chart.js** via CDN.

---

## 5. Etapa 3 – Engenharia de Prompt (Registro do Processo)

Este projeto foi desenvolvido com o auxílio do **Antigravity**, aplicando evolução iterativa de prompts para sair de uma ideia genérica até um painel executivo com regras de negócio precisas:

### 5.1. Descrição Inicial do Projeto (Prompt 1)
- **Instrução utilizada:** *"olá, Crie um dashboard financeiro de um empresa ficticia"*
- **Resultado:** Como o pedido inicial era aberto, a IA criou um primeiro protótipo exploratório (`dashboard_financeiro.html`) para uma empresa SaaS fictícia (*Vértice Tech S.A.*), com múltiplas abas (Visão Executiva, DRE, Fluxo de Caixa e Simulador).

### 5.2. Orientação Estruturada e Refinamento (Prompt 2)
Para atender aos requisitos específicos de negócio e visual desejados, o segundo prompt foi estruturado com técnicas de Engenharia de Prompt:
- **Definição de Persona:** Atuação como *Analista de Dados Sênior e Engenheiro de Front-end*.
- **Contexto e Base Numérica Fechada:** Definição da empresa *Veloce Logística & E-commerce S.A.* e fornecimento dos valores exatos de Janeiro a Junho/2026, categorias e regiões.
- **Especificação da Arquitetura Visual:** Organização em 4 blocos para leitura em até 10 segundos, tema claro (`#F8FAFC`), paleta azul-marinho e verde-esmeralda, e obrigatoriedade de arquivo único usando **Chart.js** com formatação brasileira (`R$`).
- **Regras de Negócio e Alertas:** Inclusão de filtros interativos e badges de status na tabela regional para sinalizar prazo de entrega `> 4 dias` ou margem `< 12%`.

### 5.3. Tratamento de Casos de Borda e Consistência Matemática
Durante a construção de `index.html`, foram aplicados cuidados específicos para manter os indicadores coerentes:
- **Consistência entre Visão Consolidada e Visão Regional:** No consolidado nacional (`Todas as Regiões`), o Lucro Líquido reflete exatamente `Receita - CMV - Despesas`. Ao filtrar uma região específica, o painel aplica a participação de receita e a margem líquida daquela região para manter os KPIs alinhados à tabela regional.
- **Primeiro mês da série (`Janeiro/2026`):** Como não há dados de Dezembro/2025 na base fornecida, o indicador de variação exibe `"1º mês da série"` em vez de inventar um percentual fictício.
- **Diferenciação de severidade nos alertas:** Além do estado crítico (`> 4,0 dias` ou `< 12,0%`, em vermelho) e saudável (verde), foi definida uma faixa intermediária de atenção em amarelo (`> 3,5 dias` ou `< 14,0%`) para destacar regiões próximas ao limite de SLA, como o **Centro-Oeste** (`3,6 dias` e `13,5%`).
