# 🛒 Dashboard de Vendas — Hashtag Eletro | Power BI

**Stack:** Power BI (Modelo de Dados Relacional, DAX, Relatório Interativo)
**Base de dados:** 8 arquivos Excel relacionados — vendas 2020-2022, produtos, lojas, clientes, localidades e devoluções
**Objetivo:** Monitorar performance de vendas de uma rede de eletrônicos por marca, produto, loja e período — com análise de margem, crescimento anual e devoluções

---

## 📖 O Contexto

Este projeto analisa 3 anos de vendas da **Hashtag Eletro**, uma rede fictícia de eletrônicos com **306 lojas**, **18.150 clientes** e **293 produtos**. A base foi estruturada em 8 tabelas relacionadas importadas no Power BI — simulando um modelo de dados real com tabelas fato (vendas e devoluções) e dimensões (produtos, lojas, clientes e localidades).

---

## 🗂️ Estrutura dos Dados

| Arquivo | Conteúdo |
|---|---|
| `Base_Vendas_2020/2021/2022.xlsx` | 56.046 registros de vendas (3 anos) |
| `Cadastro_Produtos.xlsx` | 293 produtos com SKU, marca, tipo, preço e custo |
| `Cadastro_Lojas.xlsx` | 306 lojas com tipo (física/online), gerente e localidade |
| `Cadastro_Clientes.xlsx` | 18.150 clientes cadastrados |
| `Cadastro_Localidades.xlsx` | Regiões e países das lojas |
| `Base_Devoluções.xlsx` | 1.809 registros de devolução com motivo |
| `Imagens.xlsx` | Links de imagens dos produtos para o relatório |

---

## 📊 Principais KPIs

### 💰 Visão Geral (2020-2022)

| Indicador | Valor |
|---|---|
| Total de vendas | 56.046 transações |
| Faturamento total | R$ 15.226.080,56 |
| Custo total | R$ 3.860.844,90 |
| Lucro total | R$ 11.365.235,66 |
| **Margem geral** | **74,6%** |
| Clientes únicos | 18.150 |
| Produtos no catálogo | 293 |
| Lojas ativas | 306 |

---

### 📅 Crescimento Anual

| Ano | Faturamento | Crescimento |
|---|---|---|
| 2020 | R$ 2.183.760,41 | — |
| 2021 | R$ 5.982.860,68 | +173,9% |
| 2022 | R$ 7.059.459,47 | +18,0% |

**Insight:** O salto de **+173,9%** de 2020 para 2021 é expressivo — pode refletir expansão da base de clientes, novas lojas online ou aumento do ticket médio. O crescimento de 2022 (+18%) indica estabilização em patamar mais alto.

---

### 🏆 Top 5 Marcas por Faturamento

| Marca | Faturamento | Participação |
|---|---|---|
| Apple | R$ 4.449.787,00 | 29,2% |
| Asus | R$ 1.444.505,42 | 9,5% |
| LG | R$ 1.421.291,05 | 9,3% |
| Samsung | R$ 1.346.653,64 | 8,8% |
| Dell | R$ 1.316.404,13 | 8,6% |

**Insight:** **Apple sozinha representa 29,2%** de todo o faturamento — quase um terço da receita dependente de uma única marca. Isso é risco de concentração: qualquer problema de fornecimento ou precificação da Apple impacta diretamente o resultado.

---

### 📦 Faturamento por Tipo de Produto

| Tipo | Faturamento | Participação |
|---|---|---|
| Notebook | R$ 7.469.356,74 | 49,1% |
| Celular | R$ 4.429.261,00 | 29,1% |
| Monitor | R$ 1.705.621,95 | 11,2% |
| Teclado | R$ 758.816,58 | 5,0% |
| Mouse | R$ 427.425,79 | 2,8% |
| Casaco | R$ 288.666,00 | 1,9% |
| Camisa | R$ 146.932,50 | 1,0% |

**Insight:** Notebook + Celular concentram **78,2%** do faturamento. A presença de Casaco e Camisa no catálogo é incomum para uma rede de eletrônicos — pode indicar expansão de categoria ou dados de teste no dataset.

---

### 🏪 Top 5 Lojas por Faturamento

| Loja | Tipo | Faturamento |
|---|---|---|
| Loja Catalog | Física | R$ 1.053.605,04 |
| Loja North America Online | Online | R$ 854.544,57 |
| Loja Europe Online | Online | R$ 827.454,52 |
| Loja Asia Online | Online | R$ 817.054,34 |
| Loja North America Reseller | Física | R$ 677.311,44 |

**Insight:** 3 das 5 maiores lojas são **canais online** — mesmo com 306 lojas físicas na rede, o digital domina o Top 5. A Loja Catalog lidera sozinha (catálogo de vendas diretas), padrão comum em distribuidores de eletrônicos.

---

### ↩️ Análise de Devoluções

| Indicador | Valor |
|---|---|
| Total de registros | 1.809 |
| Total de itens devolvidos | 1.828 |

| Motivo | Ocorrências | % |
|---|---|---|
| Produto com defeito | 1.600 | 88,4% |
| Arrependimento | 104 | 5,7% |
| Troca Indisponível | 54 | 3,0% |
| Não informado | 51 | 2,8% |

**Insight:** **88,4% das devoluções são por defeito** — proporção altíssima. Em condições normais, esse indicador ficaria abaixo de 50-60%. Vale investigar se é concentrado em alguma marca, produto ou período específico.

---

## 🧠 Sobre as Habilidades Aplicadas

Nível: **intermediário em Excel e Power BI** — construção de modelo de dados relacional com 8 tabelas (fato + dimensão), relacionamentos por chave (SKU, ID Loja, ID Cliente), medidas DAX para faturamento, margem, crescimento anual e taxa de devolução, e visualização interativa com filtros por marca, produto, loja e período.

---

## 🎥 Demonstração

![Dashboard em funcionamento](dashboard.gif)

---

## 📁 Estrutura do Projeto

```
Dashboard-Vendas-Eletro-PowerBI/
├── Hashtag_Eletro.pbix              # Arquivo Power BI
├── Base_Vendas_-_2020.xlsx          # 2.630 vendas
├── Base_Vendas_-_2021.xlsx          # vendas 2021
├── Base_Vendas_-_2022.xlsx          # vendas 2022
├── Base_Devoluções.xlsx             # 1.809 devoluções
├── Cadastro_Produtos.xlsx           # 293 produtos
├── Cadastro_Lojas.xlsx              # 306 lojas
├── Cadastro_Clientes.xlsx           # 18.150 clientes
├── Cadastro_Localidades.xlsx        # regiões e países
├── Imagens.xlsx                     # links de imagens
├── dashboard.gif                    # demonstração interativa
└── README.md                        # este arquivo
```

---

## 🚀 Como Reproduzir

1. Baixe todos os arquivos `.xlsx`
2. Abra o `Hashtag_Eletro.pbix` no Power BI Desktop
3. Atualize o caminho das fontes de dados (Transformar Dados → Configurações da Fonte)
4. Os relacionamentos entre tabelas já estão configurados no modelo

---

📫 **Contato:** [LinkedIn](https://www.linkedin.com/in/simaosantana-a744372a7) · simaojoaosantana@gmail.com
