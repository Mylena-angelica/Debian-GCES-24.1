# Apresentação final- Henrique Pucci

Resumo das contribuições do Debian para a disciplina de GCES.

## **Resumo geral por Sprint**

| Sprint | Issues | PR/MR aceitos |
| ------ | ------ | ------------- |
| 1      | 1      | 0             |
| 2      | 2      | 0             |
| 3      | 2      | 0             |
| 4      | 2      | 1             |
| 5      | 2      | 0             |

## **Listagem de Commits e Issues**

|            | Commits | Issues | PR/MR realizados | PR/MR aceitos |
| ---------- | ------- | ------ | ---------------- | ------------- |
| Individual | 18      | 6      | 4                | 1             |

## Empacotamento por Sprint

### Sprint 1

Realizado as conigurações para o amiente Debian.

### Package java autocomplete

Iniciada a tentativa de realizar a atualização do upstream.

---

### Sprint 2

### Package java autocomplete

Foi realizada uma tentativa de atualização do upstream. No entanto, foi encontrado problemas persistentes com a versão do Gradle sendo utilizada durante o processo de construção, apesar das várias tentativas de garantir o uso da versão 7.4.2.

#### Package Bleak

Foi realizada uma atualização upstream, com a remoção de patches desnecessários pós a atulaização e adição de um novo. MR foi realizado, porém, mesmo com a mudança e atulização dos patches,continuou aparecendo mais conlitos em seu build.

---

### Sprint 3

#### Java auto64fto32f

Houve atualização do upstream. Para isso, foi modificado o script do debian/rules para garantir que todos os arquivos gerados fossem corretamente copiados para o diretório de destino. E por fim, resolvi erros de dpkg-source com arquivos binários modificados especificando claramente quais binários deveriam ser incluídos na construção do pacote. Foi feito o MR.

---

### Sprint 4

#### Java auto64fto32f

Realizado correções para que fosse feito novamnte o PR.

#### Google-auth-java

Foi realizada tentativa de  atualização upstream. Porém, um descompasso entre o patch e o estado atual do arquivo pom.xml impediu a aplicação correta do patch e, consequentemente, a construção bem-sucedida do pacote.

---

### Sprint 5

#### python-transitions

Foi realizada uma atualização upstream e a criação de um patch. O PR ainda está em fase de revisão.

### wlc

Foi realizada uma atualização upstream e a criação de um patch. O PR ainda está em fase de revisão.

---

## Insigths

| Tipo                  | Quantidade |
| --------------------- | ---------- |
| Upstream              | 6          |
| Modificar patches     | 2          |
| Outras contribuiçõe   | 2          |

### Outras contribuições

- Elaboração das apresentações individuais do "Show me The code" no GitHub Pages;
- Elaboração do Template de Issues no GitHub;

### Linguagens Utilizadas nos Pacotes

- **Linguagens**: Python, Java
