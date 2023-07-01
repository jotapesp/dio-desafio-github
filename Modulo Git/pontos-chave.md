# Pontos-chave
**Pontos-chave** que geralmente me geram _dúvidas_.

### Descommitar
 1. Pegar o número _hash_ do _commit_ da versão para qual deseja voltar:
  - `git log`
 2. Voltar/resetar para a versão desejada:
  - `git reset #hash (da versão desejada)``
 3. Após tirar o _commit_, descartar todas as mudanças:
  - `git checkout nome-do-arquivo`

### Lidando com conflito de versões
Às vezes, quando duas pessoas estão trabalhando no mesmo projeto, mais especificamente no mesmo arquivo, elas podem alterar uma mesma versão do arquivo e tentar salvá-la/realizar o _commit_, nesses casos, ocorrerão os conflitos onde a última pessoa a salvar o projeto/fazer o _commit_, deverá escolher o que deve ser feito.

 1. Escolhe qual versão manter, se as duas, altere o arquivo de maneira a manter as duas alterações, caso deseje manter apenas uma das duas, selecionar no editor de texto, qual deseja manter e apagar as partes indesejáveis do código que são geradas automaticamente pelo Git quando há conflito.
  - `git push origin nome-da-branch` ao tentar realizar esse comando, um erro será exibido, mostrando o conflito
  - `git pull origin nome-da-branch` então se faz necessário, para baixar as alterações que não temos ainda localmente.
  - realizar etapas de edição no editor de texto.
 2. Salva a nova versão do arquivo no editor.
 3. No terminal:
  - `git status` mostrará os arquivos alterados ainda não commitados
  - `git add .` adicionará todos esses arquivos para que se possa realizar o _commit_
  - `git commit -m "mensagem do commit"` realizará o _commit_ final
 4. Realizar etapas de pull/push
