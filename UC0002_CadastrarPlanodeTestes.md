# Especificação de Caso de Uso: Cadastrar Plano de Testes

## 1. Descrição do Caso de Uso
Essa é a funcionalidade responsável por permitir o cadastro de um plano de testes para uma tarefa disponível para testar no GAS.

## 2.Pré-condições
O usuário estar logado com a permissão de testador.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
1. Testador aciona a funcionalidade de Cadastrar Plano de Testes;
1. Sistema exibe os detalhes da tarefa; **[[BD01](#bd01)]**
1. Testador seleciona o(s) caso(s) de uso relacionados à tarefa;
1. Sistema exibe as opções de selecionar cenários, cadastrar novo cenário e cadastrar plano; **[[FA01](#fa01)]**
1. Testador aciona a opção de selecionar cenários;
1. Sistema aciona a funcionalidade UC0005_VisualizarCenários enviando o módulo e o caso de uso selecionado;
1. Sistema lista os cenários selecionados; **[[BD02](#bd02)]**, **[[BD03](#bd03)]**
1. Testador aciona a opção de cadastrar plano de teste; **[[RN01](#RN01)]**
1. Sistema persiste as informações;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
#### FA01
**Cadastrar Novo Cenário**

1. Após passo 4 do fluxo principal, o testador seleciona a opção de cadastrar novo cenário;
1. Sistema aciona a funcionalidade UC0004_CadastrarCenários enviando o módulo e o caso de uso selecionado;
1. Sistema adiciona à lista o cenário cadastrado no passo anterior; **[[BD02](#bd02)]**
1. Retorna para o passo 8 do fluxo principal;

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Ações**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Módulo                     | Seleção única   | Sim         |         Saida | Módulo definido na tarefa no GAS. |
| Casos de Uso               | Seleção múltipla| Sim         |         Saida | Deve ser possível selecionar mais de um caso de uso. |
| Descrição                  | Alphanumérico   | Sim         |       Entrada | Descrição da tarefa no GAS.                   |
| Selecionar Cenários        | Imagem          | Sim         |       Entrada | Só deve ser habilitado se o usuário selecionar algum caso de uso.                   |
| Cadastrar Novo Usuário     | Imagem          | Sim         |       Entrada | Só deve ser habilitado se o usuário selecionar algum caso de uso.                   |
| Cadastrar Plano            | Imagem          | Sim         |       Entrada | Só deve ser habilitado se o usuário selecionar algum caso de uso.                     |

### BD02
**Narrativa**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Título                     | Alphanumérico   | Sim         |         Saida | N/A. |
| Como:                      | Alphanumérico   | Sim         |         Saida | N/A. |
| Eu quero:                  | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Para:                      | Alphanumérico   | Sim         |         Saida | N/A.                  |
| Remover Narrativa            | Imagem          | Sim         |         Entrada | N/A.                  |

### BD03
**Cenários**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Prioridade alta            | Seleção única   | Sim         |       Entrada | Ao selecionar desmarca as outras prioridades. |
| Prioridade média           | Seleção única   | Sim         |       Entrada | Ao selecionar desmarca as outras prioridades. |
| Prioridade baixa           | Seleção única   | Sim         |       Entrada | Ao selecionar desmarca as outras prioridades. |
| Número do cenário          | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Dado                       | Alphanumérico   | Sim         |         Saida | N/A.                     |
| E                          | Alphanumérico   | Sim         |         Saida | Só deve aparecer se estiver preenchido. |
| Quando                     | Alphanumérico   | Sim         |         Saida | N/A.                     |
| Então                      | Alphanumérico   | Sim         |         Saida | N/A.                     |
| E                          | Alphanumérico   | Sim         |         Saida | Só deve aparecer se estiver preenchido. |
| Remover Cenário            | Imagem          | Sim         |         Entrada | N/A.                  |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
#### RN01
- Deve ser possível criar um plano de testes sem nenhum cenário.

## 8. Documentos Relacionados
Não se aplica.
