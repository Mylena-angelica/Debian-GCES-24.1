# Igor e Silva Penha

## Empacotamento por Sprint
### Sprint 1
_Sprint_ destinada a configuração do ambiente para empacotamento Debian.

--- 

### Sprint 2
#### Package hcxdumptools
Foi realizada uma atualização _upstream_. O MR realizado, revisado, corrigido e aceito.

--- 

### Sprint 3
#### Package hcxtools
Foi realizada uma atualização _upstream_. O MR realizado e ainda se encontra na etapa de revisão.

--- 

### Sprint 4
#### Package pyenchant
Foi realizada uma atualização _upstream_. O MR ainda está em fase de revisão.
#### Package python-pika
Foi realizada uma atualização _upstream_. Porém por se tratar de uma versão beta foi indicado que seria melhor aguardar.
#### Package python-rosettasciio
Foi realizada uma atualização _upstream_. O MR ainda está em fase de revisão.

--- 

### Sprint 5
Essa foi a _Sprint_ de _Clean Code_, na qual foi realizada um sugestão de refatoração no projeto 
[NINJA-PingU](https://github.com/OWASP/NINJA-PingU) no arquivo `src/listener.c`.

Na Sprint 5, terminei as correções que foram nessárias em hcxdumptool, pacote, o qual teve êxito em seu upload. Nessa sprint além do time de python, também, realizei pacotes do time de go, assim realizei os merge request dos seguintes pacotes: `yattag`, `python-cytoolz`, `paste`, `continuity`, `golang-github-adrg-xdg`, `gojq`, `golang-barcode`, `golang-github-a8m-tree` e `golang-github-akavel-rsrc`. Além de estar acompanhando os merges dos pacotes anteriores e realizando as devidas correções.

## Package yattag

yattag é um gerador de documentos HTML ou XML com Python.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/308)
<br> [Link do respositório no salsa](https://salsa.debian.org/python-team/packages/yattag)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=yattag)
<br> [Link do tracker](https://tracker.debian.org/pkg/yattag)
<br> [Link do Merge Request](https://salsa.debian.org/python-team/packages/yattag/-/merge_requests/4)

![rep](../../img/igor/yattag-merge-request.png)

<div style="text-align:center"> Figura 2: Merge request yattag</div>
<br>

## Package python-cytoolz

python-cytoolz é uma implementação do pacote toolz, o qual provê uma alta performace funções úteis para interáveis, funções e dicionários.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/309)
<br> [Link do respositório no salsa](https://salsa.debian.org/python-team/packages/python-cytoolz)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=python-cytoolz)
<br> [Link do tracker](https://tracker.debian.org/pkg/python-cytoolz)
<br> [Link do Merge Request](https://salsa.debian.org/python-team/packages/python-cytoolz/-/merge_requests/3)

## Package paste

Paste fornece várias peças de "middleware" (ou filtros) que podem ser aninhadas para criar aplicativos da web. Cada peça de middleware usa a interface WSGI (PEP 333) e deve ser compatível com outro middleware baseado nessas interfaces.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/314)
<br> [Link do respositório no salsa](https://salsa.debian.org/python-team/packages/paste)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=paste)
<br> [Link do tracker](https://tracker.debian.org/pkg/paste)
<br> [Link do Merge Request](https://salsa.debian.org/python-team/packages/paste/-/merge_requests/3)

## Package gojq

gojq é uma implementação do comando jq escrita em Go e é possível incorporar o gojq como uma biblioteca aos seus produtos Go.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/320)
<br> [Link do respositório no salsa](https://salsa.debian.org/go-team/packages/gojq)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=gojq)
<br> [Link do tracker](https://tracker.debian.org/pkg/gojq)
<br> [Link do Merge Request](https://salsa.debian.org/go-team/packages/gojq/-/merge_requests/2)

![rep](../../img/igor/gojq-merge-request.png)

<div style="text-align:center"> Figura 3: Merge request gojq</div>
<br>

## Package continuity

Contunnuity é um sistema de manifesto de metadados do sistema de arquivos agnóstico em transporte.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/316)
<br> [Link do respositório no salsa](https://salsa.debian.org/go-team/packages/continuity)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=continuity)
<br> [Link do tracker](https://tracker.debian.org/pkg/continuity)
<br> [Link do Merge Request](https://salsa.debian.org/go-team/packages/continuity/-/merge_requests/5)

## Package golang-github-adrg-xdg

golang-github-adrg-xdg fornece uma implementação da Especificação do Diretório Base XDG. A especificação define um conjunto de caminhos padrão para armazenar arquivos de aplicativos, incluindo dados e arquivos de configuração

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/318)
<br> [Link do respositório no salsa](https://salsa.debian.org/go-team/packages/golang-github-adrg-xdg)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=golang-github-adrg-xdg)
<br> [Link do tracker](https://tracker.debian.org/pkg/golang-github-adrg-xdg)
<br> [Link do Merge Request](https://salsa.debian.org/go-team/packages/golang-github-adrg-xdg/-/merge_requests/3)

## Package golang-barcode

golang-barcode é uma ferramenta utilizada para a criação de diferentes tipos de barcodes.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/323)
<br> [Link do respositório no salsa](https://salsa.debian.org/go-team/packages/golang-barcode)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=golang-barcode)
<br> [Link do tracker](https://tracker.debian.org/pkg/golang-barcode)
<br> [Link do Merge Request](https://salsa.debian.org/go-team/packages/golang-barcode/-/merge_requests/6)

## Package golang-github-a8m-tree

golang-github-a8m-tree é uma implementação do comando tree em go.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/326)
<br> [Link do respositório no salsa](https://salsa.debian.org/go-team/packages/golang-github-a8m-tree)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=golang-github-a8m-tree)
<br> [Link do tracker](https://tracker.debian.org/pkg/golang-github-a8m-tree)
<br> [Link do Merge Request](https://salsa.debian.org/go-team/packages/golang-github-a8m-tree/-/merge_requests/3)

## Package golang-github-akavel-rsrc

golang-github-akavel-rsrc é uma ferramenta para incorporar recursos binários em programas Go.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/327)
<br> [Link do respositório no salsa](https://salsa.debian.org/go-team/packages/golang-github-akavel-rsrc)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=golang-github-akavel-rsrc)
<br> [Link do tracker](https://tracker.debian.org/pkg/golang-github-akavel-rsrc)
<br> [Link do Merge Request](https://salsa.debian.org/go-team/packages/golang-github-akavel-rsrc/-/merge_requests/3)

Resumo das contribuições do Debian para a disciplina de GCES.

## **Resumo geral por Sprint**
|Sprint|Issues|PR/MR aceitos|
|------|------|-------------|
|1     |0     |0            |
|2     |1     |1            |
|3     |1     |0            |
|4     |3     |0            |
|5     |9     |0            |

## **Listagem de Commits e Issues**
|          |Commits|Issues|PR/MR realizados|PR/MR aceitos|
|----------|-------|------|----------------|-------------|
|Individual|64     |14    |13              |1            |


### Histórico de versão

|Data|Autor|Descrição|Versão|
|----|------|------|----|
| 02/09/2024 | Igor Penha | Criação do documento | `1.0` |
| 10/09/2024 | Igor Penha | Atualização para formato do roteiro | `2.0` |
