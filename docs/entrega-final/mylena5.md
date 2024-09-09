# Apresentação final- Mylena Angélica
Resumo das contribuições do Debian para a disciplina de GCES.

## **Resumo geral por Sprint**
|Sprint|Issues|PR/MR aceitos|
|------|------|-------------|
|1     |3     |3            |
|2     |2     |1            |
|3     |1     |0            |
|4     |2     |1            |
|5     |1     |0            |

## **Listagem de Commits e Issues**

|          |Commits|Issues|PR/MR realizados|PR/MR aceitos|
|----------|-------|------|----------------|-------------|
|Individual|23     |10    | 9              | 5           |

## Empacotamento por Sprint
### Sprint 1
#### Package Ruby-airbrussh
  Foi realizada uma atualização upstream. O PR foi aceito e o pacote migrou para testing.
#### Package python-shodan
Foi realizada uma atualização upstream. O PR foi aceito e o pacote migrou para testing.
#### Package hiera
Foi realizada uma atualização upstream. O PR foi aceito e o pacote migrou para testing.

--- 

### Sprint 2
#### Package ruby-web-console
Foi realizada uma atualização upstream. O PR foi aceito e o pacote migrou para testing.
#### Package golang-github-vjeantet-grok
Foi realizada uma atualização upstream. Como é um pacote orfã, depende de muito trabalho de QA. Então a atualização upstream foi feita mas não foi criado o PR pois ações ficaram pendentes.

--- 

### Sprint 3
#### Package python-smoke-zephyr
Foi adicionado patches, que já tinham sido criadoa nova versão upstream. PR não foi aceito, pois segundo os revisores, as alterações não afetavam o pacote, logo não foi necessário. Mas ficou pentende para quando tiver uma nova atualização upstream.

--- 

### Sprint 4
#### Package ruby-view-component
Foi realizada uma atualização upstream. O PR ainda está em fase de revisão.
#### Package ruby-unleash
Foi realizada uma atualização upstream e a criação de um patch. O PR ainda está em fase de revisão.

--- 

### Sprint 5
Essa foi a Sprint de Clean Code, na qual foi realizada um sugestão de refatoração no projeto MEC-Energia-API.

--- 
## Relato das Decisões Organizacionais
- Durante o desenvolvimento do projeto, as decisões organizacionais foram baseadas em reuniões que ocorreram durante as aulas ou virtuais. Além da participação de reunião semanais com a equipe Debian.
- Somente houve 1 sprint com pareamento, para que os membros pudessem auxiliar na configuração do ambiente. Após, cada pacote foi feito de forma individual.

## Relato das Dificuldades
- *Falta de documentação*: Muitas atividades relacionadas ao empacotamento no Debian não possuem tutoriais ou guias detalhados, o que gerou dificuldades ao realizar tarefas variadas. A reunião com o grupo do Debian Brasília ocorria apenas uma vez por semana, com duração de 1 hora, para atender a todos os membros. Esse tempo limitado tornava o processo de aprendizado e a solução de dúvidas mais desafiadores.

- *Sprints curtas*: Algumas sprints tinham prazos apertados, o que impactava o andamento do trabalho, especialmente quando era necessário esperar até uma semana para obter suporte mais detalhado da comunidade Debian. Embora o grupo fosse bastante ativo no Telegram, certas questões exigiam um suporte mais personalizado e aprofundado.


## Insigths
|Tipo                |Quantidade|
|--------------------|----------|
|Upstream            |       7  |
|Add patches         |       2  |
|Criar patches       |       1  |
|Outras contribuiçõe |    3     |

### Outras contribuições
- Criação da GitHub Pages e deploy de todas as sprints e apresentação final;
- Elaboração de um tutorial para utilização e deploy da aplicação;
- Contribuições na página da Wiki do Debian.

### Linguagens Utilizadas nos Pacotes
- **Linguagens**: Ruby, Python, Golang

### GitHub Pages (08/09/24)
- **Commits**: 20 commits
- **Linhas de Código**: 81.762

