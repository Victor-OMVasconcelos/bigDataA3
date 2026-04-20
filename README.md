# Análise de Dados e Big Data - A3

________________________________________
# 1. Caso de estudo
1.1 Descrição do problema
Durante abordagens policiais de trânsito, situações inicialmente rotineiras podem evoluir para cenários de risco devido ao comportamento do infrator. Essa escalada pode resultar em confrontos, necessidade de uso da força ou até prisões.
Atualmente, não há um sistema estruturado que permita analisar dados históricos dessas abordagens para identificar padrões comportamentais que indiquem risco de escalada.
Dessa forma, surge a necessidade de um sistema capaz de analisar dados de ocorrências, identificar padrões e fornecer suporte à tomada de decisão dos agentes de segurança.
________________________________________
**1.2 Hipóteses**
 
 •	H1: Existem padrões comportamentais recorrentes em infratores que levam à escalada de abordagens. 
 
 •	H2: A análise de dados históricos pode ajudar a prever situações de risco. 
 
 •	H3: A identificação desses padrões pode melhorar a tomada de decisão dos policiais em campo. 
 
 •	H4: O uso de visualizações gráficas facilita a interpretação dos dados e a identificação de correlações. 
 
________________________________________
 **1.3 Requisitos Funcionais (RF)**
 
•	RF01: O sistema deve importar conjuntos de dados nos formatos CSV, JSON e RDS. 

•	RF02: O sistema deve organizar os dados em estruturas tabulares. 

•	RF03: O sistema deve permitir a filtragem de dados com base em colunas e valores definidos pelo usuário. 

•	RF04: O sistema deve identificar padrões e correlações entre os dados. 

•	RF05: O sistema deve apresentar os dados por meio de visualizações gráficas (gráficos e tabelas). 

•	RF06: O sistema deve permitir exportar resultados das análises. 

________________________________________
**1.4 Requisitos Não Funcionais (RNF)**

•	RNF01: O sistema deve possuir interface intuitiva e de fácil utilização. 

•	RNF02: O sistema deve processar conjuntos de dados de médio porte (até X registros) em tempo aceitável. 

•	RNF03: O sistema deve garantir a segurança e privacidade dos dados analisados. 

•	RNF04: O sistema deve ser compatível com os principais sistemas operacionais (Windows/Linux). 

•	RNF05: O sistema deve manter desempenho estável durante análises simultâneas. 

•	RNF06: O sistema deve permitir fácil manutenção e evolução. 

________________________________________
 **1.5 Backlog Inicial**
 
| ID   | Item              | Descrição                                   | Prioridade |
|------|-------------------|---------------------------------------------|------------|
| B01  | Importação de dados | Implementar leitura de CSV, JSON e RDS      | Alta       |
| B02  | Estruturação de dados | Organizar dados em tabelas                   | Alta       |
| B03  | Filtros           | Criar sistema de filtragem dinâmica          | Alta       |
| B04  | Análise de padrões | Implementar correlação e análise estatística | Alta       |
| B05  | Visualização      | Criar gráficos e dashboards                   | Alta       |
| B06  | Exportação        | Exportar relatórios e dados                   | Média      |
| B07  | Interface         | Desenvolver UI amigável                        | Média      |
| B08  | Segurança         | Implementar controle de acesso e proteção de dados | Alta       |

________________________________________
# 2. Mapeamento de Dados e Coleta e Armazenamento

**2.1 Identificação das fontes de dados (APIs, bancos, datasets públicos)**

Fontes potenciais identificadas para coleta de dados incluem:

* Dados históricos de ocorrências policiais de trânsito (CSV, JSON, RDS).
* Datasets públicos relacionados a abordagens policiais e comportamento de infratores.
* APIs de bases governamentais ou de segurança pública (a definir).
* Exemplo de datasets públicos: Stanford Open Policing Project (dados de paradas policiais nos EUA), bases do Data.gov, Bureau of Justice Statistics.
* Para o mapa de fonte de dados, foi acessado os sites Stanford Open Policing Project, Traffic Stop Data NCSL, mas o que realmente foi utilizado foi o dataset disponível em: ( [https://www.kaggle.com/datasets/stanford-open-policing/stanford-open-policing-project-bundle-1?select=CT.csv](url) ).
  
Entrega: Mapa de fontes de dados.
________________________________________
**2.2 Implementação da coleta de dados**

* O sistema deve importar conjuntos de dados nos formatos CSV, JSON e RDS (RF01).

* A coleta deve contemplar a importação automatizada e manual desses arquivos para alimentar a base de dados.

* Deve ser possível integrar dados de múltiplas fontes, organizando-os para análise posterior.

* Para o processamento desses dados foi utilizado o programa Python e Jupyter para análise do arquivo CSV, executado no VS Code utilizando extensões de Python e Jupyter, com os seguintes comandos para configuração do ambiente:

  ________________________________________
```**Código para visualização dos dados no VS Code**
# Criar ambiente virtual
python -m venv myenv

# Ativar ambiente (no cmd)
myenv\Scripts\activate

# Instalar pandas e notebook
pip install pandas
python -m pip install notebook

# Executar Jupyter Notebook
jupyter notebook

# Instalar kernel
python -m pip install ipykernel
```
Entrega: Base de dados inicial.
________________________________________

**2.3 Definição de estrutura de armazenamento**
* Os dados devem ser organizados em estruturas tabulares (RF02), facilitando filtragem e análise.

* A estrutura deve suportar a manipulação de dados de médio porte com desempenho aceitável (RNF02).

* Deve garantir segurança e privacidade dos dados armazenados (RNF03).

* A estrutura deve ser compatível com sistemas operacionais Windows e Linux (RNF04).

* Deve permitir fácil manutenção e evolução do sistema (RNF06).

* **Obs: A definição da estrutura de armazenamento ainda não foi pensada, portanto não há alterações para essa etapa no momento.**

Entrega: Base de dados inicial estruturada.
