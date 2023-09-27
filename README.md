                                    ***git clone***

- Clona um repositório em um diretório recém-criado, cria ramificações de rastreamento remoto para cada ramificação no repositório clonado (visível usando git branch --remotes) e cria e faz check-out de uma ramificação inicial que é bifurcada a partir da ramificação atualmente ativa do repositório clonado.
Após o clone, um plain git fetchsem argumentos atualizará todas as ramificações de rastreamento remoto, e um git pullsem argumentos irá, além disso, mesclar a ramificação master remota na ramificação master atual, se houver (isso não é verdade quando "--single-branch" é dado; veja abaixo).
Essa configuração padrão é obtida criando referências aos chefes de ramificação remota refs/remotes/origine inicializando remote.origin.urle remote.origin.fetch configurando variáveis.


                                 ***git branch***

- Se --listfor fornecido, ou se não houver argumentos de não opção, as ramificações existentes serão listadas; a filial atual será destacada em verde e marcada com um asterisco. Quaisquer ramificações retiradas em árvores de trabalho vinculadas serão destacadas em ciano e marcadas com um sinal de mais. A opção -rfaz com que as ramificações de rastreamento remoto sejam listadas e a opção -amostra as ramificações locais e remotas.


                                 ***git push***

- Atualize as referências remotas utilizando as referências locais, enquanto envia os objetos necessários para que sejam concluídas as referências informadas.
Você pode fazer com que coisas que intereçam aconteçam com um repositório toda vez que você adicionar, configurando os ganchos lá. Consulte a documentação para git-receive-pack[1] .

                                 ***git checkout***

- Atualiza os arquivos na árvore de trabalho para corresponder à versão no índice ou na árvore especificada. Se nenhum pathspec for fornecido, git checkout também será atualizado HEADpara definir o branch especificado como o branch atual.


                                  ***git status***

- O comando git status exibe o estado do diretório de trabalho e da área de teste. Ele permite que você veja quais alterações foram preparadas, quais não foram e quais arquivos não estão sendo rastreados pelo Git.


                                  ***git add***

- Este comando atualiza o índice usando o conteúdo atual encontrado na árvore de trabalho, para preparar o conteúdo preparado para o próximo commit. Normalmente adiciona o conteúdo atual dos caminhos existentes como um todo, mas com algumas opções também pode ser usado para adicionar conteúdo com apenas parte das alterações feitas nos arquivos da árvore de trabalho aplicadas ou remover caminhos que não existem na árvore de trabalho não mais.


                                 **git commit**

- Crie um novo commit contendo o conteúdo atual do índice e a mensagem de log fornecida descrevendo as alterações. O novo commit é filho direto de HEAD, geralmente a ponta do branch atual, e o branch é atualizado para apontar para ele (a menos que nenhum branch esteja associado à árvore de trabalho, caso em que HEAD é "desanexado" conforme descrito em git -checkout[1] ).

                                 ***git pull***

- Incorpora as alterações de um repositório remoto no ramo atual. Em seu modo predefinido, o comando git pull é uma abreviação do comando git fetch seguido por git merge FETCH_HEAD.
- Mais precisamente, o comando git pull executa o git fetch com os parâmetros informados e chama o git merge para mesclar os cabeçalhos recuperados da ramificação no ramo atual. Com --rebase, ele executa o comando git rebase em vez do git merge.


                              ***git revert***

- O comando git revert é uma operação de desfazer avançada que oferece um método seguro de desfazer alterações. Em vez de excluir ou tornar órfãos os commits no histórico de commits, uma reversão criará um novo commit que inverte as alterações especificadas.


                              ***git merge***

- Incorpora alterações dos commits nomeados (desde o momento em que seus históricos divergiram do branch atual) no branch atual. Este comando é usado por git pull para incorporar alterações de outro repositório e pode ser usado manualmente para mesclar alterações de um branch em outro.


![Alt text](./image-1.png)