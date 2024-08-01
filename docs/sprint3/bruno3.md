# Bruno Ribeiro

Ao final de Sprint 2, durante o Merge Request realiazado do pacote, percebi que o programa _bruteforce-luks_ não completava os testes da pipeline. Investigando mais a fundo, percebi que o mesmo entrava em um laço e não saía mais, isso, devido à uma condição de corrida. Haja vista, quando executado o programa em uma única thread este terminava todos os testes, porém ao aumentar o número de threads o programa rodava infinitamente. Desse modo, ainda estou em processo de corrigir este problema no software, para assim, poder proceder com o empacotamento.

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

Correção de um bug causado por uma condição de corrida, ao executar o progragma em mais de uma thread.

### Updates

### Histórico de versão

|Data|Autor|Descrição|Versão|
|----|------|------|----|
| 01/08/2024 | Bruno Ribeiro | Criação do documento | `1.0` |
