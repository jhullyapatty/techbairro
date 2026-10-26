# TechBairro

Sistema de cadastro de clientes para a associação de moradores, com janela gráfica simples. Permite cadastrar, consultar, alterar e excluir clientes. Os dados ficam guardados no computador da secretaria e continuam lá depois de fechar o programa.

**Versão atual:** 3.3.1 · Histórico de mudanças no [CHANGELOG](CHANGELOG.md)

## Funcionalidades

- Cadastrar clientes (nome, telefone, e-mail e endereço)
- Consultar a lista de clientes cadastrados
- Alterar os dados de um cliente
- Excluir um cliente
- Validar os dados antes de salvar
- Guardar os dados em um banco local, sem precisar de internet

## Requisitos para execução

| Item | Requisito |
|---|---|
| Sistema operacional | Windows (versão testada: Windows 11) |
| Python | Python 3 (versão testada: 3.12.0) |
| Tkinter | Já vem junto com o Python. No Linux pode ser preciso instalar: `sudo apt install python3-tk` |
| Bibliotecas externas | Nenhuma (veja o [requirements.txt](requirements.txt)) |
| Internet | Só para baixar o projeto. Para usar o sistema, não precisa |

## Instalação

**Opção 1: com Git**

```bash
git clone https://github.com/jhullyapatty/techbairro.git
cd techbairro
```

**Opção 2: pelo site do GitHub (sem Git)**

1. Abra https://github.com/jhullyapatty/techbairro
2. Clique no botão verde **Code** e depois em **Download ZIP**.
3. Extraia o arquivo ZIP em uma pasta do computador.
4. Abra o terminal dentro da pasta extraída (a que contém o `techbairro.py`).

**Dependências:** o `requirements.txt` não lista nenhum pacote, porque o projeto usa só a biblioteca padrão do Python. Para conferir, rode o comando abaixo. Ele deve terminar sem erro e sem instalar nada:

```bash
pip install -r requirements.txt
```

**Executar o programa:**

```bash
python techbairro.py
```

Ao abrir, aparece a janela da TechBairro com o formulário de clientes. No terminal aparece uma mensagem com o caminho do banco, como esta:

```
Banco em uso: C:\...\TechBairro\techbairro.db
```

## Configuração do banco de dados

Os clientes ficam guardados em um arquivo chamado `techbairro.db` (banco SQLite). Ele é criado vazio, automaticamente, na primeira vez que o programa é executado, na mesma pasta do `techbairro.py`.

Para saber qual banco está em uso, olhe a mensagem "Banco em uso" que aparece no terminal quando o programa abre. Ela mostra o caminho completo do arquivo.

O arquivo `techbairro.db` **não vem no repositório** porque contém dados pessoais dos clientes (nome, telefone, e-mail e endereço), protegidos pela LGPD. Por isso ele está no `.gitignore` e não é enviado ao GitHub. Quem baixa o projeto começa com um banco vazio.

**Cópia de segurança:** feche o programa e copie o arquivo `techbairro.db` para outro lugar (um pen drive ou outra pasta), de preferência com a data no nome, por exemplo `techbairro_2026-10-26.db`. Para restaurar, feche o programa e coloque a cópia de volta na pasta do projeto, com o nome `techbairro.db`.

## Como usar

O passo a passo está no [Manual de uso](docs/manual_de_uso.md).

## Estrutura do projeto

- `techbairro.py`: programa principal. Abre a janela e liga as telas às outras partes.
- `cliente.py`: define o que é um cliente e quais dados ele tem.
- `banco.py`: guarda, busca, altera e exclui os clientes no banco.
- `validacao.py`: confere se os dados digitados estão corretos antes de salvar.
- `scripts/travar_banco.py`: script de teste. Simula outro programa usando o banco ao mesmo tempo e segura uma trava nele, para mostrar o erro "database is locked". Não faz parte do uso normal.
- `gerar_pacote.py`: gera o arquivo .zip da versão para distribuição.
- `CHANGELOG.md`: histórico das mudanças de cada versão.
- `COMO_EXECUTAR.txt`: instruções curtas de execução que vão dentro do pacote .zip.
- `requirements.txt`: lista de dependências (nenhuma).
- `docs/manual_de_uso.md`: manual para quem usa o sistema.
- `.gitignore`: lista o que não deve ir para o GitHub (como o banco de dados).

## Autor

Jhullya Patrícia Duarte Silva Dias, Técnico em Desenvolvimento de Sistemas, Senac DF