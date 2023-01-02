# Git Commands

Este repositório contém alguns dos principais comandos em git aos quais eu listei e separei por tópicos com o intuido de ajudar aos mais curiosos e interessados sobre essa ferramenta. Tentei fazer uma explicação breve e sucinta sobre cada funcionalidade, porém é de interesse do usuário sempre consultar a documentação atual para que possíveis bugs ou dúvidas mais específicas possam ser sanadas. 

Documentação : [https://git-scm.com/doc](https://git-scm.com/doc)

---

## Comandos básicos: 

Essas são algumas das funções mais básicas do Git. Funções ao qual o usuário provavelmente irá usar com certa frequência. Aqui estão alguns comando responsáveis por **criar**, **clonar**, **resetar**, **checar status**, **adicionar** ou **remover** arquivos e **criar versões** de código.

| Comando | Função |
| ------- | --------- |
| `git init` | Cria ou Inicializa um repositório Git vazio ou já existente |
| `git clone [url_do_repositório]` | Clona um repositório já existente na sua máquina |
| `git status` | Checa o status, indicando se um arquivo foi ou não incluido no cotrole de versão ou atualizado |
| `git add [nome_arquivo.extensão]` | Adiciona um arquivo para área de stage (Controle de Versão)|
| `git add .` | Adiciona todos os arquivos novos ou modificados de uma só vez ao controle de versão |
| `git commit -m "[Mensagem de Commit]"` | Cria uma versão do cógido com as alterações e com uma mensagem junto |
| `touch .gitignore` | Cria um arquivo git, e dentro dele, o usuário irá decidir quais pastas ou arquivos serão ou não adicionádos ao controle de versão |
| `git reset --hard- [id_da_versão]` | volta o código a uma versão anterior ao qual ele estava |
| `git rm -r [nome_do_arquivo.extensão]` | Remove um arquivo (ou pasta). também pode ser usado para remover arquivos do índice de staging e do diretório de trabalho|

## Inspecionando e Comparando repositórios:

Esses são os comandos responsáveis por inspecionar e comparar o código. Com eles é possível **mostrar modificações feitas**, **versões adicionadas**, **detalhes das modificações** e **visualizar alterações**.

| Comando | Função |
| ------- | --------- |
| `git log` | Mostra as modificações feitas no código |
| `git reflog` | Mostra quais foram as versões adicionadas ao código |
| `git log --summary` | Monstra modificações mais detalhadas sobre os commits e alterações, juntamente com data e autor(es) do mesmo |
| `git diff [branch_original] [branch_desejada]` | Mostra alterações antes de mesclar. Essas alterações podem ser commits, ramificações, arquivos, etc. |

## Branch e Merge:

Antes de sqguir com os comandos demais comandos, é interessante que você tenha em mente os conceitos sobre branch e merge. 

### Branch:

Numa tradução literal, o significado de branch remete a palavra galhos, no contexto da programação, branchs poderiam ser vistam como ramificações, mais especificamente como divisões aos quais versões diferentes de um projeto poderão ser armazenadas e/ou versionadas. Essas novas versões podem significar várias coisas, sejam elas funcionalidades, correções de erros ou bugs, etc.

Caso o usuário esteja desenvolvendo de forma solo, algo como uma aplicação pessoal, uma unica branch já poderia resolver seus problemas. Porém, caso esteja em uma aplicação mais profissíonal, como em uma empresa, mais de uma branch é importante para manter o código fonte organizado.

### Merge:

O conceito de merge remeta a algo como mesclagem. Após o usuário terminar seus testes numa brach paralela, e ter a certeza que aquele código está funcinando, ele poderá fazer uma merge para a branch principal, ou seja, fazer uma mesclagem daquele novo trecho de código na ramificação principal.


| Comando | Função |
| ------- | --------- |
| `git branch` | Lista as branches existentes. O asterisco e cor verde apontas para a branch atual |
| `git branch -a` | Lista todas as branches locais e remotas |
| `git branch [nome_da_branch]` | Cria uma nova branch. Normalmente são chamadas de staging, esse nome se refere a branchs que está recebendo atualizações que não estão testadas em produção |
| `git branch -d [nome_da_branch]` | Deletar a branch |
| `git checkout -b [nome_da_branch]` | Cria uma nova branch e muda para ela |
| `git checkout -b [nome_da_branch_nova] [nome_da_branch_desejada]` | Cria uma nova branch com base nos arquivos existente de uma branch desejada |
| `git checkout [nome_da_branch]` | Seleciona uma branch desejada |
| `git checkout -` | Volta para a última branch | 
| `git checkout -- [nome_do_arquivo.extensão]` | Descarta modificações de um arquivo |
| `git merge [nome_da_branch]` | Faz um merge de uma branch para a branch atual |
| `git merge [branch_ramificada] [branch_desejada]` | Faz com que os códigos da branch remificada sejam enviados para a branch alvo |
| `git stash` | Salva as alterações sem commit |
| `git stash clear` | Remove todas as entradas arquivadas |

## Compartilhamento e Atualizações de projetos:

Aqui estão alguns dos comandos responsáveis por enviar **alterações** e **atualizações** nas branchs, **deletar**, **receber alterações** e **definir** para onde um código deverpa ser **compartilhado**.
| Comando | Função |
| ------- | --------- |
| `git push origin [nome_da_branch]` | Envia alterações para uma branch desejada |
| `git push -u origin [nome_da_branch]` | Envia as alterações da branch informada para um repositório remoto |
| `git push` | Envia as alterações para o repositório remoto (branch atual) |
| `git push origin --delete [nome_da_branch]` | Deleta uma branch remota |
| `git pull` | Atualiza o repositório local com as ultimas atualizações feitas no servidor |
| `git pull origin [nome_da_branch]` | Recebe alterações de uma branch remota |
| `git remote add origin [url_do_repositório]` | Define para onde o código deverá ser compartilhado, seja outro dev ou algum serviço de hospedagem em nuvem |
| `git remote set-url origin [url_do_repositório]` | Altera uma banch remota para outar usando a url |
