Atualizar o Upstream de um pacote é um processo relativamente simples, mas no meio do caminho pode acontecer algumas intercorrências, e algumas delas são comuns. Neste documento você verá um tutorial do que fazer quando se deparar com algum desses erros


## Falha no build após a atualização upstream

Após atualizar o upstream de um pacote Debian, você pode encontrar um problema onde a tag no debian/changelog ainda reflete o número da versão antiga, e não a nova versão upstream. Isso resulta em erros durante a construção do pacote com gbp buildpackage.

**Erro:**

```
dpkg-source: informação: Dica: certifique-se que a versão em debian/changelog corresponde à árvore fonte desempacotada
dpkg-source: informação: você pode integrar as alterações locais com dpkg-source --commit
dpkg-source: erro: a abortar devido a alterações do autor inesperadas, veja /tmp/crudini_0.9.4-2.diff.5zHGpT
E: Failed to package source directory 
```

**Causa:** Esse erro ocorre porque o debian/changelog não foi atualizado corretamente para refletir a nova versão upstream. Isso pode acontecer quando a atualização automática falha ou não é executada.

**Solução:** 

- **1. Identifique a Nova Versão Upstream:**

    - Verifique qual é a nova versão upstream, que você pode encontrar no arquivo de origem ou na tag do repositório upstream.

- **2. Atualize o debian/changelog:**

    - Abra o arquivo debian/changelog.
    - Localize a entrada que ainda usa a versão antiga.
    - Atualize o número da versão para refletir a nova versão upstream, seguida pelo sufixo de revisão Debian (-1 para a primeira revisão).

    - **Exemplo:**

    ```
    crudini (0.9.5-1) unstable; urgency=medium
    ```

    Nota: Se a versão antiga era 0.9.4-1, por exemplo, você deve atualizar para 0.9.5-1 após a atualização do upstream para 0.9.5.

    
- **3. Construa o Pacote Novamente:**

    - Após atualizar o debian/changelog, execute:

    ```
    gbp buildpackage
    ```

|Data|Autora|Versão|
|----|------|------|
| 19/08/2024 | Ana Luíza | Criação do documento | 