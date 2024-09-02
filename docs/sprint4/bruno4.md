# Bruno Campos Ribeiro

Na Sprint 4, que teve uma duração de 2 semana, em uma conversa durante a reunião foi passado alguns pacotes que estavam atrasados e que 
precisavam da atualização upstream dos pacotes. Então nessa sprint também foi realizado o merge request dos pacotes: `gp-saml-gui`, 
`pyvirtualdisplay` e `astroid`.

## Package gp-saml-gui

É um script auxiliar para permitir que você faça login de forma interativa em uma VPN GlobalProtect que utiliza autenticação SAML, de 
modo que você possa se conectar posteriormente com o OpenConnect. (O protocolo GlobalProtect é suportado no OpenConnect v8.0 ou mais 
recente; a versão v8.06+ é recomendada.) Infelizmente, o login interativo é, às vezes, uma alternativa necessária ao login 
automatizado via scripts como zdave/openconnect-gp-okta.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/284)
<br> [Link do respositório no salsa](https://salsa.debian.org/python-team/packages/gp-saml-gui)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=gp-saml-gui)
<br> [Link do tracker](https://tracker.debian.org/pkg/gp-saml-gui)
<br> [Link do Merge Request](https://salsa.debian.org/python-team/packages/gp-saml-gui!1)


## Package pyvirtualdisplay

O `pyvirtualdisplay` é um wrapper em Python para o Xvfb, Xephyr e Xvnc.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/287)
<br> [Link do respositório no salsa](https://salsa.debian.org/python-team/packages/pyvirtualdisplay)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=pyvirtualdisplay)
<br> [Link do tracker](https://tracker.debian.org/pkg/pyvirtualdisplay)
<br> [Link do Merge Request](https://salsa.debian.org/python-team/packages/pyvirtualdisplay!2)


## Package astroid

O objetivo deste módulo é fornecer uma representação base comum para código-fonte Python. Atualmente, é a biblioteca que alimenta 
as capacidades do pylint. Ele fornece uma representação compatível que vem do módulo _ast. O módulo reconstrói a árvore gerada pelo 
módulo _ast embutido ao percorrer recursivamente a AST e construir uma AST estendida. As novas classes de nós possuem métodos e 
atributos adicionais para diferentes usos. Elas incluem suporte para inferência estática e escopos de nomes locais. Além disso, o 
astroid também pode construir árvores parciais ao inspecionar objetos em tempo de execução.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/289)
<br> [Link do respositório no salsa](https://salsa.debian.org/python-team/packages/astroid)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=astroid)
<br> [Link do tracker](https://tracker.debian.org/pkg/astroid)
<br> [Link do Merge Request](https://salsa.debian.org/python-team/packages/astroid!6)


### Histórico de versão

|Data|Autor|Descrição|Versão|
|----|------|------|----|
| 14/08/2024 | Bruno Ribeiro | Criação do documento | `1.0` |
