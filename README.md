# dashboard-vendas-powerbi
# 📊 Dashboard de Vendas com Power BI utilizando Star Schema

Projeto prático desenvolvido para consolidar os conceitos de modelagem dimensional e modelagem de dados utilizando o **Power BI Desktop**, estruturando um ambiente analítico otimizado no formato **Star Schema** (Modelo em Estrela).

## 🚀 Sobre o Desafio
O objetivo principal deste projeto é transformar dados relacionais em um modelo dimensional eficiente, garantindo alta performance em consultas, clareza nas análises e facilidade na criação de medidas DAX e relatórios visuais.

## 🗄️ Estrutura do Modelo de Dados (Star Schema)
O modelo foi construído separando as informações de negócio entre tabelas dimensionais (contexto e características) e tabelas fato (métricas e chaves de relacionamento):

* **Tabela Fato (`Fato_Professor`):** 
  * Contém as chaves estrangeiras de ligação (`idProfessor`, `idDepartamento`, `idCurso`, `idDisciplina`) e as métricas/valores de negócio (como a `CargaHoraria`).
  * Inclui a coluna de data para cruzar os eventos na linha do tempo.

* **Tabelas de Dimensão:**
  * **`Dim_Professor`**: Armazena as informações descritivas dos professores.
  * **`Dim_Departamento`**: Detalha os departamentos e respectivos campi.
  * **`Dim_Curso`**: Especifica os cursos oferecidos.
  * **`Dim_Disciplina`**: Detalha as disciplinas associadas.
  * **`Calendario`**: Tabela dimensão de tempo gerada via DAX (`CALENDAR`) para habilitar análises temporais e inteligência de tempo (`Time Intelligence`).

## 🔗 Relacionamentos
* Todas as dimensões estão conectadas à tabela fato (`Fato_Professor`) através de relacionamentos de **Um para Muitos (1:*)**, com a propagação de filtros fluindo das dimensões para a tabela fato, garantindo integridade e consistência analítica.
* A tabela `Calendario` foi relacionada à tabela fato pela respetiva coluna de data utilizando cardinalidade **Muitos para Um (*:1)**.

## 🛠️ Ferramentas Utilizadas
* **Power BI Desktop** (Modelagem de dados, Power Query e DAX)
* **GitHub** (Versionamento e portfólio de projetos)
