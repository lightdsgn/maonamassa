# 4. Diagrama de Caso de Uso

Abaixo está o diagrama que representa as interações entre os atores (Cliente, Prestador e Administrador) e as principais funcionalidades do sistema.

![Diagrama de Caso de Uso](/USOCLIENTE.png)
_Imagem: Casos de Uso parte Cliente_

![Diagrama de Caso de Uso](/USOPRESTADOR.png)
_Imagem: Casos de Uso parte Prestador_

![Diagrama de Caso de Uso](/USOADM.png)
_Imagem: Casos de Uso parte Administrador_

## **Link no diagrams.net:**https://app.diagrams.net/?src=about#G1BdPXGro4AepwQkwFw5gfgjcY_7AqyQuk#%7B"pageId"%3A"C5RBs43oDa-KdzZeNtuy"%7D

## 4.1 Descrição de Casos de Uso

A seguir estão detalhados os principais fluxos do sistema, demonstrando como cada ator interage com as funcionalidades essenciais.

---

# Caso de Uso 1: Solicitar Serviço

**Ator Principal:** Cliente  
**Atores Secundários:** Prestador (recebe a solicitação), Sistema (envio de notificações).  
**Objetivo:** Permitir que o cliente envie uma solicitação de serviço com descrição, imagens, endereço e categoria.

### Pré-condições:

- O cliente deve estar cadastrado e autenticado.
- Deve existir ao menos um prestador ativo na plataforma.

### Pós-condições:

- A solicitação é registrada no sistema.
- O prestador recebe uma notificação de novo pedido.

### Fluxo Principal:

1. O cliente acessa a página "Solicitar Serviço".
2. O sistema exibe o formulário de descrição, categoria, endereço e anexos.
3. O cliente preenche todas as informações.
4. O cliente envia a solicitação.
5. O sistema valida os dados.
6. O sistema registra a solicitação no banco.
7. O sistema envia notificação ao prestador.
8. O sistema confirma o envio ao cliente.

### Fluxos Alternativos:

- **A1: Dados incompletos:** O sistema exibe mensagem de erro e impede o envio.
- **A2: Falha no upload de imagens:** O sistema solicita novo envio dos arquivos.
- **A3: Cliente sem endereço cadastrado:** Sistema obriga o preenchimento antes de enviar.

---

# Caso de Uso 2: Criar Orçamento

**Ator Principal:** Prestador  
**Atores Secundários:** Cliente  
**Objetivo:** Elaborar um orçamento em resposta à solicitação de serviço.

### Pré-condições:

- Deve existir uma solicitação pendente.
- O prestador deve estar autenticado.

### Pós-condições:

- O orçamento é registrado e enviado ao cliente.

### Fluxo Principal:

1. O prestador acessa sua lista de solicitações.
2. O sistema exibe detalhes da solicitação.
3. O prestador clica em "Criar Orçamento".
4. O sistema exibe formulário com produtos, valores e prazo.
5. O prestador insere produtos cadastrados e informa mão de obra.
6. O prestador confirma o orçamento.
7. O sistema registra e envia ao cliente.
8. O cliente recebe notificação.

### Fluxos Alternativos:

- **A1: Prestador sem produtos cadastrados:** O sistema permite orçamento somente com mão de obra.
- **A2: Valor total zerado:** O sistema alerta e solicita revisão.

---

# Caso de Uso 3: Aprovar Orçamento

**Ator Principal:** Cliente  
**Atores Secundários:** Prestador  
**Objetivo:** Permitir que o cliente aceite ou recuse o orçamento enviado.

### Pré-condições:

- O cliente deve ter recebido um orçamento válido.

### Pós-condições:

- O serviço muda para "Em andamento" quando aprovado.

### Fluxo Principal:

1. O cliente acessa "Orçamentos Recebidos".
2. O sistema lista os orçamentos pendentes.
3. O cliente seleciona o orçamento.
4. O cliente clica em "Aprovar".
5. O sistema atualiza o status para "Em andamento".
6. O sistema notifica o prestador.

### Fluxos Alternativos:

- **A1: Cliente recusa:** O sistema encerra a solicitação.
- **A2: Orçamento expirado:** O sistema impede aprovação e solicita novo orçamento.

---

# Caso de Uso 4: Cadastrar Produtos (Prestador)

**Ator Principal:** Prestador  
**Objetivo:** Adicionar produtos que podem ser usados em serviços ou vendidos separadamente.

### Pré-condições:

- Prestador autenticado.

### Pós-condições:

- Produto adicionado ao catálogo do prestador.

### Fluxo Principal:

1. O prestador acessa "Meus Produtos".
2. O sistema exibe lista e botão "Cadastrar Produto".
3. O prestador insere nome, categoria, preço e estoque.
4. O sistema valida os dados.
5. O produto é registrado.

### Fluxos Alternativos:

- **A1: Nome duplicado:** O sistema alerta e sugere renomear.
- **A2: Preço inválido:** O sistema impede cadastro.

---

# Caso de Uso 5: Visualizar Dashboard

**Ator Principal:** Prestador  
**Objetivo:** Acompanhar desempenho, serviços pendentes, agenda, gráficos e contas a receber.

### Fluxo Principal:

1. O prestador acessa o dashboard.
2. O sistema exibe estatísticas:
   - serviços pendentes,
   - serviços em andamento,
   - concluídos,
   - contas a receber,
   - avaliação média,
   - gráficos mensais.
3. O prestador utiliza filtros e navega entre os dados.

---

# Caso de Uso 6: Gerenciar Plataforma (ADM)

**Ator Principal:** Administrador  
**Objetivo:** Supervisionar usuários, categorias, solicitações e métricas globais.

### Fluxo Principal:

1. O ADM acessa o painel administrativo.
2. O sistema exibe gráficos e indicadores gerais.
3. O ADM pode:
   - ativar/desativar contas,
   - gerenciar categorias,
   - visualizar relatórios,
   - acompanhar volume financeiro agregado.

---
