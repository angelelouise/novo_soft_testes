# Especificação de Caso de Uso: Cadastrar Erros

## 1. Descrição do Caso de Uso

## 2.Pré-condições
O usuário estar logado com a permissão de testador.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
1. Testador aciona a funcionalidade de Cadastrar Erros;
1. Sistema exibe o formulário de cadastro. **[[BD01](#bd01)]**
1. Testador preenche e aciona a opção de cadastrar erro;
1. Sistema adiciona erro ao plano de testes;
1. Sistema adiciona um log no histórico do erro;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
Não se aplica.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Cadastrar Erros**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Cenário de testes          | Seleção múltipla| Não         | Entrada       | Deve exibir apenas os cenários adicionados ao plano. Formato: Titulo - Código|
| Ambientes                  | Alphanumérico   | Sim         | Entrada       | N/A.|
| Tipo do Erro               | Seleção única   | Sim         | Entrada       | Opções: Visual, Negócio, Execução, Navegação |
| Logins                     | Alphanumérico   | Sim         | Entrada       | |
| Caso de uso                | Autocomplete    | Sim         | Entrada       | Deve filtrar pelos casos de uso do sistema específico da tarefa. |
| Adicionar mais um caso de uso| Imagem          | Não         | Entrada       | Permite a seleção de mais de um caso de uso. |
| Severidade                 | Seleção única   | Sim         | Entrada       | Opções: SEV-1, SEV-2, SEV-3, SEV-4.|
| Status                     | Seleção única   | Sim         | Entrada       | Opções: Cadastrado, Pendente, Em correção, Corrigido, Finalizado, Reincidente, Desconsiderado. |
| Descrição                  | Alphanumérico   | Sim         | Entrada       | N/A. |
| Anexo                      | Hiperlink       | Sim         | Entrada       | Permite arrastar e soltar arquivos.|

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01
- Ao cadastrar um erro vinculado à um cenário, este automaticamente deve ter seu status alterado para "Erro de Teste".

## 8. Documentos Relacionados
Não se aplica.
