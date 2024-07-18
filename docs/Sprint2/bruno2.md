# Bruno Ribeiro

Na Sprint 2, com duração de 9 dias, conduzi a atualização upstream de um pacote. Para realizar esse empacotamento, foi necessário estudar detalhadamente arquivos como debian/watch, além de adquirir e aplicar conhecimentos sobre gerenciamento de patches e testes automatizados.

## Package bruteforce-luks

O objetivo deste programa é tentar encontrar a senha de um volume criptografado com LUKS.

Ele pode ser usado de duas maneiras:

- Testar todas as senhas possíveis, dado um conjunto de caracteres.
- Testar todas as senhas em um arquivo.
 
Há uma opção na linha de comando para especificar o número de threads a serem utilizadas.

Enviar um sinal USR1 para um processo bruteforce-luks em execução faz com que ele imprima o progresso e continue.

[Link issue no Salsa](https://salsa.debian.org/debian-brasilia-team/docs/-/issues/254)
<br> [Link do respositório no salsa](https://salsa.debian.org/pkg-security-team/bruteforce-luks)
<br> [Link do Lintian](https://udd.debian.org/lintian/?packages=bruteforce-luks)
<br> [Link do tracker](https://tracker.debian.org/pkg/bruteforce-luks)

### Empacotamento

O primeiro passo foi modificar o arquivo debian/watch, pois ele não conseguia baixar e ler corretamente o arquivo de assinatura do mantenedor do pacote. Para solucionar essa questão, o arquivo foi atualizado para o padrão utilizando a API do GitHub.

Adicionalmente, a RegEx foi ajustada para funcionar corretamente. Agora, a busca pela assinatura é realizada nas releases, em vez de nas tags.

### Updates

### Histórico de versão

|Data|Autor|Descrição|Versão|
|----|------|------|----|
| 18/07/2024 | Bruno Ribeiro | Criação do documento | `1.0` |
