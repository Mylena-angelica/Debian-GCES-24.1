# Apresentação final- Ana Luíza Rodrigues
Resumo das contribuições do Debian para a disciplina de GCES.

## **Resumo geral por Sprint**
|Sprint|Issues|PR/MR aceitos|
|------|------|-------------|
|1     |2     |0            |
|2     |2     |0            |
|3     |2     |0            |
|4     |2     |0            |
|5     |1     |0            |

## **Listagem de Commits e Issues**

|          |Commits|Issues|PR/MR realizados|PR/MR aceitos|
|----------|-------|------|----------------|-------------|
|Individual|25     |09    | 03             | 0           |

## Sprint 1 

|Nome do pacote     | Descrição| Issues|
|-------------------|---------| ---------|
|Pacote aionotify   | Biblioteca inotify simples, baseada em asyncio    | Atualização do Upstream    | 
|Pacote jqp        | TUI playground para experimentar o jq (programa)    | Atualização do Upstream    | 

## Sprint 2 

|Nome do pacote     | Descrição| Issues|
|-------------------|---------| ---------|
|Pacote aionotify   | Biblioteca inotify simples, baseada em asyncio    | Correção pedidas na revisão    |
|Pacote jqp        | TUI playground para experimentar o jq (programa)    | Correção pedidas na revisão    |

No pacote aionotify, além de fazer as correções atualizei a versão Standards seguindo o Debian Policy.

Na correção do pacote jqp segui as orientações do revisor. Posteriormente durante a reunião do Debian foi avaliada a complexidade envolvida devido à necessidade de atualização da biblioteca bubbletea e a orientação foi abandonar o pacote.

## Sprint 3 

|Nome do pacote     | Descrição| Issues|
|-------------------|---------| --------|
|Pacote aionotify   | Biblioteca inotify simples, baseada em asyncio    | Correção pedidas na revisão    | 
|Pacote python-gflanguages        | API para avaliar o suporte a idiomas na coleção Google Fonts    | Atualização do Upstream    | 

Foi necessário refazer alguns commits feitos anteriormente no pacote aionotify para seguir o padrão do Debian.

Depois da atualização do upstream do pacote python-gflanguages enfrentei um erro ao tentar fazer o build. Não obtive resposta sobre o erro no grupo e na reunião do Debian.

## Sprint 4 

|Nome do pacote     | Descrição| Issues|
|-------------------|---------| --------|
|Pacote crudini   | Utilitário para manipular arquivos ini    | Atualização do Upstream    | 
|-        |   -  | Documentação de erros comuns no git pages    | 

Depois da atualização do upstream enfrentei um erro na hora de fazer o build que é comum, então adicionei na documentação do gitpages sobre como resolvê-lo.

## Sprint 5 - Clean Code

- **Projeto:** SIGE

Para a etapa de clean code analisei o SIGE Frontend e a utilizei a ferramenta SonarQube para fazer a análise do código. Identifiquei uma área de melhoria e após a correção analisei o código novamente com o SonarQube para constatar que o problema tinha sido resolvido.