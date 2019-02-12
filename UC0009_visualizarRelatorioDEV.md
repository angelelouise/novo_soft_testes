# Especificação de Caso de Uso: Visualizar Relatório (Desenvolvedor)

## 1. Descrição do Caso de Uso

## 2.Pré-condições
O usuário estar logado com a permissão de desenvolvedor.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
**Visualizar Relatório**
1. Desenvolvedor aciona a funcionalidade de Visualizar relatório de erros;
1. Exibe a listagem de erros da tarefa; **[[BD01](#bd01)]**, **[[FA01](#fa01)]**, **[[FA02](#fa02)]**, **[[FA03](#fa03)]**, **[[FA04](#fa04)]**, **[[FA05](#fa05)]**
1. Desenvolvedor marca como corrigido todos os erros;
1. Atribui o status "Corrigido" ao erro e adiciona ao histórico;
1. Desenvolvedor aciona a opção de finalizar correção; **[[RN01](#RN01)]**
1. Persiste as informações no banco.
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
#### FA01
**Erro em correção**
1. Após o passo 2 do fluxo principal, o desenvolvedor aciona a opção de marcar erro como em correção;
1. Atribui o status "Em correção" e o usuário do desenvolvedor ao erro e adiciona ao histórico;
1. Retorna para o passo 7 do fluxo principal.

#### FA02
**Marcar como corrigido com observação**
1. Após o passo 2 do fluxo principal, o desenvolvedor aciona a opção de marcar como corrigido com observação;
1. Exibe o formulário para cadastro da observação. **[[BD03](#bd03)]**;
1. Desenvolvedor preenche a observação e finaliza a operação
1. Atribui o status "Corrigido" ao erro e adiciona a observação ao histórico;
1. Retorna para o passo 5 do fluxo principal.

#### FA03
**Marcar como desconsiderado**
1. Após o passo 2 do fluxo principal, o desenvolvedor aciona a opção de marcar como desconsiderado;
1. Exibe o formulário para cadastro da observação. **[[BD03](#bd03)]**;
1. Desenvolvedor preenche a observação e finaliza a operação
1. Atribui o status "Desconsiderado" ao erro e adiciona a observação ao histórico;
1. Retorna para o passo 5 do fluxo principal.

#### FA04
**Marcar como pendente**
1. Após o passo 2 do fluxo principal, o desenvolvedor aciona a opção de marcar como pendente;
1. Atribui o status "Pendente" ao erro e retira a associação do desenvolvedor ao erro, adiciona essas informações ao histórico;
1. Retorna para o passo 7 do fluxo principal.

#### FA05
**Visualizar histórico**
1. Após o passo 2 do fluxo principal, o testador aciona a opção de visualizar histórico do erro;
1. Exibe o detalhamento **[[BD02](#bd02)]**;
1. Retorna para o passo 7 do fluxo principal.


### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Visualizar Erros**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida| Observações |
|----------------------------|-----------------|-------------|-------------|-------------|
| Cenário de testes          | Alphanumérico   | Não         | Saida       | N/A.|
| Ambientes                  | Alphanumérico   | Sim         | Saida       | N/A.|
| Tipo do Erro               | Alphanumérico   | Sim         | Saida       | Opções: Visual, Negócio, Execução, Navegação |
| Logins                     | Alphanumérico   | Sim         | Saida       | N/A. |
| Caso de uso                | Alphanumérico   | Sim         | Saida       | N/A. |
| Severidade                 | Alphanumérico   | Sim         | Saida       | Opções: SEV-1, SEV-2, SEV-3, SEV-4.|
| Status                     | Alphanumérico   | Sim         | Saida       | Opções: Cadastrado, Pendente, Em correção, Corrigido, Finalizado, Reincidente, Desconsiderado. |
| Descrição                  | Alphanumérico   | Sim         | Entrada     | N/A. |
| Anexo                      | Hiperlink       | Sim         | Entrada     | Faz o download dos arquivos. |
| Marcar como em correção    | Hiperlink       | Não         | Entrada     | Não exibir quando o status do erro é "Em correção" |
| Marcar como corrigido     | Hiperlink       | Não         | Entrada     |  |
| Marcar como corrigido com observação | Hiperlink       | Sim         | Entrada     |   **[[BD03](#bd03)]**|
| Marcar como desconsiderado | Hiperlink       | Não         | Entrada     |   **[[BD03](#bd03)]**|
| Marcar como pendente       | Hiperlink       | Não         | Entrada     |  |
| Histórico                  | Hiperlink       | Não         | Entrada     | **[[BD02](#bd02)]** |

### BD02
**Histórico**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Data                       | Data            | Sim         |         Saida | N/A.                   |
| Status                     | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Usuário                    | Alphanumérico   | Sim         |         Saida | N/A.                   |

### BD03
**Observação**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Observação                 | Data            | Sim         |       Entrada | N/A.                   |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01
- Só deve ser possível finalizar a correção se todos os erros estiverem no status "Corrigido" e/ou "Desconsiderados".

## 8. Documentos Relacionados
Não se aplica.
