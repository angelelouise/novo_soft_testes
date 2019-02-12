# Especificação de Caso de Uso: Cadastrar Cenários

## 1. Descrição do Caso de Uso
Essa é a funcionalidade responsável por permitir o cadastro de cenários.

## 2.Pré-condições
O usuário estar logado com a permissão de testador.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
1. Testador aciona a funcionalidade de Cadastrar Cenários;
1. Sistema exibe a configuração do cenário; **[[BD01](#bd01)]**, **[[FA01](#fa01)]**
1. Testador seleciona o módulo e o caso de uso relacionados à tarefa;
1. Testador seleciona a opção de buscar uma narrativa já existente;  **[[FA02](#fa02)]**
1. Exibe um formulário para busca de narrativas; **[[BD02](#bd02)]**
1. Testador realiza a pesquisa e seleciona um resultado;
1. Preenche o formulário com os dados da narrativa selecionada;**[[BD03](#bd03)]**
1. Testador preenche as informações do cenário e aciona a opção de cadastrar cenário;
1. Sistema persiste as informações;
1. Sistema adiciona um log no histórico do cenário;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
#FA01

**Funcionalidade acionada pela funcionalidade UC0002_CadastrarPlanodeTestes**
1. Após o passo 2, o sistema preenche  automaticamente o módulo e o caso de uso de acordo com os parâmetros recebidos;
1. Retorna para o passo 4 do fluxo principal.

#FA02

**Criar nova narrativa**
1. No passo 4, o testador seleciona a opção de cadastrar uma nova narrativa;
1. Exibe o formulário para cadastro da narrativa.
1. Retorna para o passo 8 do fluxo principal.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Configuração do cenário**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Módulo                     | Seleção única/Alphanumérico  | Sim         | Entrada/Saida | Seleção única quando acionado pelo testador, alphanumérico quando acionado pelo sistema. |
| Casos de Uso               | Seleção única   | Sim         | Entrada/Saida |  Seleção única quando acionado pelo testador, alphanumérico quando acionado pelo sistema. Quando acionado pelo sistema e tiver mais de um caso de uso relacionado, permitir que o testador selecione um entre as opções. |
| Buscar Narrativa               | Link   | Sim         | Entrada |  Permite que o testador escolha uma narrativa já existente. |
| Nova Narrativa               | Link   | Sim         | Entrada | Permite que o testador cadastre uma nova narrativa. |

### BD02
**Buscar narrativa**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Título                     | Alphanumérico  | Sim         | Entrada | Procura por títulos que contém a entrada inserida. |
| Resultados                 | Seleção única   | Sim         | Entrada | Quando selecionado preenche automaticamente os campos de narrativa do formulário **[[BD03](#bd03)]**.|

### BD02
**Formulário**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Título                     | Alphanumérico   | Sim         | Entrada/Saida | Vem preenchido quando o testador tiver buscado uma narrativa já existente. Caso contrário, exibir editável. |
| Como:                      | Alphanumérico   | Sim         | Entrada/Saida | Vem preenchido quando o testador tiver buscado uma narrativa já existente. Caso contrário, exibir editável. |
| Eu quero:                  | Alphanumérico   | Sim         | Entrada/Saida | Vem preenchido quando o testador tiver buscado uma narrativa já existente. Caso contrário, exibir editável.                  |
| Para:                      | Alphanumérico   | Sim         | Entrada/Saida | Vem preenchido quando o testador tiver buscado uma narrativa já existente. Caso contrário, exibir editável.                 |
| Dado                       | Alphanumérico   | Sim         |   Entrada | N/A.                     |
| Adicionar mais uma pré condição                      | Imagem   | Sim         |   Entrada | Adiciona mais um campo "E".                     |
| E                          | Alphanumérico   | Sim         |   Entrada | N/A.                     |
| Quando                     | Alphanumérico   | Sim         |   Entrada | N/A.                     |
| Então                      | Alphanumérico   | Sim         |       Entrada |                     
| Adicionar mais uma pós condição                      | Imagem   | Sim         |   Entrada | Adiciona mais um campo "E".                     |
| E                          | Alphanumérico   | Sim         |       Entrada |                     |
| Tag                          | Autocomplete   | Sim         |       Entrada |                     |
| Adicionar mais uma tag                      | Imagem   | Sim         |   Entrada | Adiciona mais um campo "Tag".                     |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
#### RN01
Não se aplica.

## 8. Documentos Relacionados
Não se aplica.
