# Manual de uso da TechBairro

## A tela principal

Ao abrir o programa, aparece a janela **TechBairro — Cadastro de Cliente**. Nela você encontra:

- Os campos para preencher: **Nome**, **Telefone**, **E-mail** e **Endereço**.
- Os botões: **Salvar**, **Cancelar** e **Consultar**.
- Uma linha de aviso, logo abaixo dos campos. É nela que o sistema escreve o que aconteceu (por exemplo, "Cliente 'Maria' salvo com sucesso!"). Verde significa que deu certo, vermelho significa que algo precisa ser corrigido.
- Quando o programa abre e ainda não há clientes, a linha de aviso mostra, em cinza, "Nenhum cliente cadastrado ainda".
- O contador **Clientes cadastrados**, que mostra quantos clientes existem.
- No canto inferior direito, o número da versão do sistema.

## Cadastrar um cliente

1. Preencha os quatro campos: Nome, Telefone, E-mail e Endereço (veja as regras mais abaixo).
2. Clique no botão **Salvar**.
3. Na linha de aviso aparece, em verde: "Cliente 'nome do cliente' salvo com sucesso!".
4. Os campos ficam limpos, prontos para o próximo cliente, e o contador aumenta em 1.

Se aparecer um aviso em vermelho, leia o que ele pede, corrija e clique em **Salvar** de novo. O cliente só é salvo quando está tudo certo.

## Consultar os clientes cadastrados

1. Clique no botão **Consultar**.
2. Abre a janela **Consulta de Clientes**, com a lista de todos os clientes cadastrados, em ordem alfabética pelo nome. Cada cliente aparece em uma linha, neste formato: nome | telefone | e-mail | endereço. Exemplo: `Maria Souza | 61999998888 | maria@email.com | Quadra 5, Casa 10`. Se não houver nenhum, aparece "Nenhum cliente cadastrado".
3. Para voltar à tela principal, feche a janela de consulta no **X** no canto superior direito.

## Alterar os dados de um cliente

1. Clique em **Consultar** para abrir a lista de clientes.
2. Clique no cliente que deseja alterar e depois no botão **Editar selecionado**. (Dar dois cliques no cliente também funciona.)
3. A lista fecha e os dados do cliente aparecem nos campos da tela principal. A linha de aviso mostra, em azul, "Editando cliente: nome do cliente", e o botão **Salvar** passa a se chamar **Salvar edição**.
4. Corrija o que precisar e clique em **Salvar edição**.
5. Aparece, em verde: "Cliente 'nome do cliente' atualizado com sucesso!".

Para desistir da alteração, clique em **Cancelar**. O sistema avisa "Edição cancelada. Nada foi alterado." e o cliente continua como estava.

## Excluir um cliente

1. Clique em **Consultar** para abrir a lista de clientes.
2. Clique no cliente que deseja excluir.
3. Clique em **Excluir selecionado**.
4. O sistema pergunta, numa janela chamada **Confirmar exclusão**: "Tem certeza que deseja excluir o cadastro de nome do cliente? Essa ação não pode ser desfeita." Clique em **Sim** para excluir ou em **Não** para desistir.
5. Se clicar em **Sim**, o cliente some da lista, o contador diminui em 1 e a tela principal mostra, em verde: "Cliente 'nome do cliente' excluído com sucesso!".

**Atenção:** um cliente excluído não pode ser recuperado.

## Regras de preenchimento

| Campo | Obrigatório? | Regra |
|---|---|---|
| Nome | Sim | Não pode ficar em branco. |
| Telefone | Sim | Use **somente números**, sem espaços, parênteses ou traços. Exemplo: 61999998888. |
| E-mail | Sim | Use o formato **nome@dominio.com**: precisa ter algo antes do @ e um ponto depois dele. |
| Endereço | Sim | Não pode ficar em branco. |

## Mensagens do sistema

| Mensagem | O que significa | O que fazer |
|---|---|---|
| Cliente 'nome' salvo com sucesso! | O cliente foi cadastrado. | Nada. Pode cadastrar o próximo. |
| Cliente 'nome' atualizado com sucesso! | As alterações foram salvas. | Nada. |
| Cliente 'nome' excluído com sucesso! | O cliente foi removido da lista. | Nada. |
| Preencha o(s) campo(s): ... | Algum campo obrigatório ficou em branco. A mensagem diz quais. | Preencha os campos citados e clique em **Salvar** de novo. |
| Telefone inválido: use somente números. | O telefone tem letras, espaços, parênteses ou traços. | Digite o telefone só com números, como 61999998888. |
| E-mail inválido: use o formato nome@dominio.com | O e-mail está sem o @, sem nada antes dele ou sem o ponto depois dele. | Corrija o e-mail. Exemplo: maria@email.com. |
| Selecione um cliente antes de editar. (ou "...antes de excluir.") | Você clicou em **Editar selecionado** ou **Excluir selecionado** sem escolher um cliente na lista. Aparece numa janela chamada **Atenção**. | Clique em OK, escolha um cliente da lista e tente de novo. |
| Edição cancelada. Nada foi alterado. | Você clicou em **Cancelar** durante uma alteração. | Nada. O cliente continua como estava. |
| Formulário limpo | Você clicou em **Cancelar** e os campos foram esvaziados. | Nada. Pode preencher de novo. |
| Cliente não encontrado: ele pode ter sido excluído. Nada foi alterado. | O cliente que você estava alterando já não existe mais. | Confira na lista de **Consultar** se ele ainda está lá e cadastre de novo, se precisar. |
| Cliente não encontrado: nome já não está mais no banco. A lista será atualizada. | Você tentou excluir um cliente que já tinha sido excluído. | Clique em OK. A lista se atualiza sozinha. |
| Não foi possível excluir o cliente. | O sistema não conseguiu excluir. O motivo aparece logo abaixo da mensagem. | Feche os outros programas que possam estar usando os dados, espere alguns segundos e tente de novo. Se continuar, avise quem instalou o sistema. |
| Erro ao ler o banco: ... | O sistema não conseguiu mostrar a lista de clientes. A mensagem aparece dentro da janela de consulta. | Feche a janela, espere alguns segundos e clique em **Consultar** de novo. Se continuar, avise quem instalou o sistema. |
| Erro ao salvar no banco: ... | O sistema não conseguiu gravar os dados. | Feche os outros programas que possam estar usando os dados, espere alguns segundos e tente de novo. Se continuar, avise quem instalou o sistema. |

## Dúvidas frequentes

**Fechei o programa. Perdi os clientes que cadastrei?**
Não. Os clientes ficam guardados no computador e aparecem de novo quando você abre o programa.

**Digitei o telefone com parênteses e traço e deu erro. O que faço?**
O campo Telefone aceita só números. Digite tudo junto, sem espaços, parênteses ou traços. Em vez de (61) 99999-8888, escreva 61999998888.

**Errei os dados de um cliente. Como corrijo?**
Clique em **Consultar**, escolha o cliente, clique em **Editar selecionado**, corrija os campos e clique em **Salvar edição**.

**Como faço uma cópia de segurança dos clientes?**
Feche o programa e copie o arquivo `techbairro.db` (que fica na mesma pasta do programa) para um pen drive ou outra pasta. Se precisar, peça ajuda a quem instalou o sistema.

**Apareceu "database is locked" ou um aviso de erro ao salvar. O que faço?**
Isso acontece quando outro programa está usando os dados ao mesmo tempo. Feche os outros programas que possam estar abertos, espere alguns segundos e tente de novo. Se continuar, avise quem instalou o sistema.