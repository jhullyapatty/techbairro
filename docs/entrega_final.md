# Entrega final da TechBairro
Aluno(a): Jhullya Patrícia Duarte Silva Dias · Versão entregue: 3.3.2

Por que esse número de versão: Desde a versão 3.3.1 só acrescentei documentação (README, manual de uso, requirements.txt e registro de testes) e corrigi o gerar_pacote.py. Não criei função nova no programa, então somei 1 no último número: 3.3.1 virou 3.3.2.

| # | Item | Evidência |
|---|---|---|
| 1 | A aplicação funciona: os 6 casos de teste passaram | docs/registro_de_testes.md |
| 2 | A versão aparece na janela e é a mesma do CHANGELOG e do README | Janela mostra v3.3.2 no canto; VERSAO = "3.3.2" no techbairro.py; entrada v3.3.2 no CHANGELOG.md; "Versão atual" 3.3.2 no README.md |
| 3 | O pacote foi testado numa pasta limpa | Extraí dist/TechBairro-3.3.2.zip na Área de Trabalho e rodei python techbairro.py: a janela mostrou v3.3.2 e o contador começou em 0 |
| 4 | Tag e release publicadas, com o .zip anexado | Tag v3.3.2 e TechBairro-3.3.2.zip anexado: https://github.com/jhullyapatty/techbairro/releases/tag/v3.3.2 |
| 5 | O repositório não tem banco, __pycache__ nem dist | O .gitignore ignora techbairro.db, __pycache__/, *.pyc e dist/; esses itens não aparecem na página do repositório |
| 6 | O histórico tem commits com mensagens claras | https://github.com/jhullyapatty/techbairro/commits |
| 7 | README, manual de uso e requirements.txt estão no repositório | README.md, docs/manual_de_uso.md e requirements.txt |
| 8 | A Issue "Teste do README" (Aula 26) está fechada | Issue #1 fechada pelo commit com "Closes #1" |
| 9 | O vídeo está publicado e o link abre sem pedir login |https://youtu.be/9ynOUYewUJM?is=QZzjc2LHBNCzAzsA |

## Roteiro do vídeo
| Bloco | Tempo | O que vou mostrar ou dizer |
|---|---|---|
| 1. Problema e solução | 30 s | Me apresento como aluna do Senac DF. A associação de moradores precisava cadastrar clientes sem planilha e sem perder dados. A TechBairro 3.3.2 cadastra, consulta, edita e exclui clientes, valida os dados antes de salvar e guarda tudo num banco SQLite |
| 2. Demonstração | 1 min 30 s | Cadastrar um cliente fictício; tentar salvar com e-mail em formato inválido, e o sistema barra o dado; abrir a Consulta em ordem alfabética; editar trocando o telefone; excluir respondendo Não e depois Sim |
| 3. Como foi construída | 30 s | Camadas: techbairro.py (janela), validacao.py (regras), banco.py (SQLite) e cliente.py (molde do cliente); 6 testes automáticos e 6 testes na tela; GitHub com commits em etapas, tag v3.3.2 e release com o .zip |
| 4. Aprendizado | 30 s | Dificuldade: na Aula 15 a tela dizia "atualizado", mas o banco não mudava porque faltava o commit. Aprendizado: salvar e enviar o trabalho ao GitHub todo dia evita perder arquivos. Melhoria: impedir telefone repetido |

## Perguntas
**Pergunta 1: por que o arquivo techbairro.db não está no GitHub?**
Porque ele guarda dados pessoais dos clientes (nome, telefone, e-mail e endereço), que não devem ser compartilhados. O .gitignore impede que ele suba.

**Pergunta 2: qual caso de teste pegou um defeito de verdade? Qual era o defeito?**
O BUG 4 da Aula 15. Eu editei um cliente, troquei o telefone e salvei. A tela dizia "atualizado com sucesso", mas a Consulta mostrava o telefone antigo. Faltava o conexao.commit() no método atualizar(). Corrigi acrescentando o commit antes do close().

**Pergunta 3: se o voluntário da associação tiver só o link do repositório, como ele instala e executa a TechBairro?**
Ele baixa o TechBairro-3.3.2.zip na página de Releases, ou usa Code e Download ZIP. Precisa ter o Python 3 instalado e nenhuma biblioteca extra, porque a TechBairro usa só Tkinter, sqlite3 e os. Extrai o zip, abre um terminal dentro da pasta e executa python techbairro.py. O banco é criado vazio na primeira execução.

## Autoavaliação
O que ficou bom: a demonstração mostrou o cadastro, a validação, a edição e a exclusão funcionando, com dados fictícios. O que eu mudaria: impedir telefone repetido. O mais importante que aprendi: testar só a tela não basta, é preciso conferir o que foi gravado no banco. Também aprendi que salvar e enviar o trabalho ao GitHub todos os dias evita perder arquivos e reduz riscos, e que o Git e o GitHub deixam o projeto organizado e fácil de entregar.
