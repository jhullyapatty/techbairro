# Changelog da TechBairro

## v3.3.2 (Aula 27)
### Adicionado
- README com requisitos, instalação e configuração do banco.
- Arquivo requirements.txt.
- Manual de uso em docs/manual_de_uso.md.
- Registro de testes em docs/registro_de_testes.md.

## Em desenvolvimento
### Adicionado
- Código publicado no GitHub, com histórico de versões.

## v3.3.1 (Aula 21)
### Alterado
- Foi divido partes do codigo central(techbairro) em arquivos separados.

## v3.3.0 (Aula 20)
### Corrigido
- Edição e o excluimento usam o cliente selecionada da lista.
- O sistema verifica se o cliente ainda existe no banco de dados antes de atualizar ou excluir
- Cancelar a edição de limpa os campos

### Adicionado
- Duplo clique na lista para seleciona/editar um cliente.
- Botãso muda para "Salva edição" durante a edição do mesmo.

## v3.2.1 (Aula 17)
### Alterado
- O número da versão passou a ser colocada como uma constante.

### Adicionado
- Script scripts/gerar_pacote.py, que gera o pacote da versão em .zip.
- Arquivo COMO_EXECUTAR.txt, com os requisitos e instruções .

## v3.2 (Aula 16)
### Alterado
- O banco agora é aberto pelo caminho completo (os.path + __file__),
  sempre na pasta do projeto, não importa de onde o programa seja executado.
### Adicionado
- Mensagem "Banco em uso" no terminal, mostrando qual arquivo de banco está sendo usado.

## v3.1 (Aula 15)
### Corrigido
- O Endereço voltou a ser obrigatório no cadastro.
- A validação de e-mail passou a recusar e-mail sem nome antes do @ ou sem ponto depois do @.
- A Consulta voltou a listar os clientes em ordem alfabética.
- A edição de um cliente passou a ser gravada no banco (faltava o commit).
- A exclusão só acontece quando o usuário responde Sim na confirmação.

## v3.0 (Aula 14)
### Alterado
- O GerenciadorClientes deixou de guardar os clientes numa lista em memória
  e passou a gravar no banco SQLite techbairro.db.
- Editar e excluir passaram a usar o id do cliente no banco (id_em_edicao),
  e não mais a posição na lista (indice_em_edicao).
- O contador de clientes passou a vir do banco ao abrir a aplicação.
### Adicionado
- Tratamento de erros do banco com try/except sqlite3.Error.

## v2.0 (Aulas 11 e 12)
### Adicionado
- Classes Cliente e GerenciadorClientes.
- Tela de Consulta com a lista de clientes e os botões Editar e Excluir.
- Confirmação antes de excluir um cliente.

## Antes da v2.0 (Aulas 5 a 10)
- Janela de cadastro com Tkinter, eventos dos botões e validação dos campos.
