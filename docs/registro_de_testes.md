# Registro de testes da TechBairro

Versão testada: 3.3.2 · Data: 26/10/2026 · Responsável: Jhullya Patrícia

Sistema operacional e versão do Python: Python 3.12.0
| ID | Requisito | Passos e dados | Esperado | Obtido | Status |

|---|---|---|---|---|---|

| CT01 | RF01 | Cadastrar um cliente com todos os campos certos | Mensagem verde “Cliente ‘Ana souza’ salvo com sucesso!”, contador aumenta em 1 | Mensagem verde “Cliente ‘Ana souza’ salvo com sucesso!”, contador aumenta em 1 | Passou|

| CT02 | RF01 | Salvar com Nome e Endereço vazios 
|Mensagem vermelha “Preencha o(s) campo(s): Nome, Endereço” e nenhum cliente salvo. |Mensagem vermelha “Preencha o(s) campo(s): Nome, Endereço” e nenhum cliente salvo.| Passou|

| CT03 | RF02 | Telefone 61 9999 0000 (com espaços) 
| Mensagem vermelha “Telefone inválido: use somente números.” e nenhum cliente salvo. | Mensagem vermelha “Telefone inválido: use somente números.” e nenhum cliente salvo.| Passou |

| CT04 | RF03 | E-mail ana@email (sem ponto) 
| Mensagem vermelha “E-mail inválido: use o formato nome@dominio.com” e nenhum cliente salvo. |Mensagem vermelha “E-mail inválido: use o formato nome@dominio.com” e nenhum cliente salvo. |Passou|

| CT05 | RF05 | Editar um cliente, trocar o telefone e salvar |Mensagem verde "Cliente 'Ana souza' atualizado com sucesso, e a consulta mostrou o telefone novo | Mensagem verde "Cliente 'Ana souza' atualizado com sucesso, e a consulta mostrou o telefone novo| Passou|

| CT06 | RF06 | Excluir um cliente: responder Não, depois Sim |Com Não, o cliente continua na lista. Com Sim, mensagem verde “Cliente ‘...’ excluído com sucesso!” e o contador diminui em 1. |Com Não, o cliente continuou na lista. Com Sim, mensagem verde “Cliente ‘Ana souza’ excluído com sucesso!”, o cliente saiu da lista e o contador diminuiu |Passou|



## Testes automáticos
Saída do `python testar_validacao.py`: OK teste_cliente_valido
OK teste_endereco_vazio
OK teste_telefone_com_letras
OK teste_email_sem_ponto
OK teste_nome_e_telefone_vazios
OK teste_email_parece_valido_sem_usuario
Todos os testes passaram.

## Defeitos encontrados
Nenhum defeito encontrado na versão 3.3.2.