# Especificação de Caso de Uso: Executar Plano de Testes

## 1. Descrição do Caso de Uso
Essa é a funcionalidade responsável por permitir a execução de um plano de testes.

## 2.Pré-condições
O usuário estar logado com a permissão de testador.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
1. Testador aciona a funcionalidade de Executar Plano de Testes;
1. Sistema lista os cenários contidos no plano; **[[BD01](#bd01)]**
1. Sistema exibe as opções de cadastrar erro, visualizar relatório, finalizar teste e alterar plano;  **[[FA01](#fa01)]**,  **[[FA02](#fa02)]**,  **[[FA03](#fa03)]**
1. Testador modifica o status dos cenários para "Validado"; **[[RN02](#RN02)]**
1. Testador finaliza o teste;  **[[RN01](#RN01)]**, **[[RN03](#RN03)]**, **[[RN04](#RN04)]**, **[[RN05](#RN05)]**
1. Sistema persiste as informações no banco;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
#### FA01
**Cadastrar Erro**

1. Após o passo 3, o testador seleciona a opção de cadastrar erro;
1. Sistema aciona a funcionalidade UC0006_CadastrarErros;
1. Retorna para o passo 7 do fluxo principal.

#### FA02
**Visualizar Relatório de Erros**

1. Após o passo 3, o testador seleciona a opção de cadastrar erro;
1. Sistema aciona a funcionalidade UC0007_VisualizarRelatório;
1. Retorna para o passo 7 do fluxo principal.

#### FA03
**Alterar Plano**

1. Após o passo 3, o testador seleciona a opção de cadastrar erro;
1. Sistema aciona a funcionalidade de alterar plano de testes;
1. Retorna para o passo 7 do fluxo principal.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Cenários**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Título                     | Alphanumérico   | Sim         |         Saida | N/A. |
| Prioridade                 | Imagem          | Sim         |         Saida | N/A. |
| Como:                      | Alphanumérico   | Sim         |         Saida | N/A. |
| Eu quero:                  | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Para:                      | Alphanumérico   | Sim         |         Saida | N/A.                  |
| Número do cenário          | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Dado                       | Alphanumérico   | Sim         |         Saida | N/A.                     |
| E                          | Alphanumérico   | Sim         |         Saida | N/A.                     |
| Quando                     | Alphanumérico   | Sim         |         Saida | N/A.                     |
| Então                      | Seleção única   | Sim         |       Entrada | Opções: Erro e Validado.                    |
| E                          | Seleção única   | Sim         |       Entrada | Opções: Erro e Validado.                     |
| Situação                   | Seleção única   | Sim         |       Entrada | Opções: Pendente, Testando, Erro de teste, Validado **[[RN02](#RN02)]** |
| Testador                   | Seleção única   | Sim         |       Entrada | Opções: Todos os testadores do sistema específico da tarefa.                    |
| Cadastrar Erro            | Imagem          | Sim         |       Entrada | Aciona a funcionalidade UC0006_CadastrarErros enviando o cenário específico.                    |
| Histórico                  | Imagem          | Sim         |       Entrada |**[[BD02](#bd02)]**                    |

Pendente, Testando, Erro de teste, Concluído 1ª Bateria, Concluído 2ª Bateria

### BD02
**Histórico**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Data                       | Data            | Sim         |         Saida | N/A.                   |
| Status                     | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Usuário                    | Alphanumérico   | Sim         |         Saida | N/A.                   |

### BD03
**Resumo**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Pendente                       | Data            | Sim         |         Saida | Deve contabilizar todos os cenários que estão nesse status.                   |
| Testando                     | Alphanumérico   | Sim         |         Saida | Deve contabilizar todos os cenários que estão nesse status.                        |
| Erro de Testes                    | Alphanumérico   | Sim         |         Saida | Deve contabilizar todos os cenários que estão nesse status.                       |
| Validada                   | Alphanumérico   | Sim         |         Saida | Deve contabilizar todos os cenários que estão nesse status.                      |
| Agrupar por Situação:                   | Alphanumérico   | Sim         |         Saida | Deve contabilizar todos os cenários que estão nesse status.                      |
| Agrupar por Testador:                   | Alphanumérico   | Sim         |         Saida | Deve contabilizar todos os cenários que estão nesse status.                      |
| Agrupar por Prioridade:                   | Alphanumérico   | Sim         |         Saida | Deve contabilizar todos os cenários que estão nesse status.                      |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
#### RN01
- Deve ser possível criar um plano de testes sem nenhum cenário.

#### RN02
- Só deve ser possível selecionar a opção "Validado" se todos os campos do "Então" estiverem marcados como validados.

#### RN03
- Ao finalizar o teste todos os erros no status "Cadastrado" devem ser modificados para o status "Pendente".

#### RN04
- Ao finalizar o teste com algum cenário no status "Erro de teste" ou erro no status "Pendente", "Cadastrado" ou "Reincidente", deve-se alterar ao status da tarefa relacionada para "Aguardando Correções".

#### RN05
- Ao finalizar o teste com os cenários no status "Validado" ou erro no status "Finalizado" ou "Desconsiderado", deve-se alterar ao status da tarefa relacionada para "Validada".


## 8. Documentos Relacionados
Não se aplica.
