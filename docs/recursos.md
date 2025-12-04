# 3. Principais Recursos e Funcionalidades

O sistema **Mão na Massa** conta com módulos específicos para atender às necessidades de **clientes**, **prestadores de serviços** e **administradores da plataforma**. Cada módulo foi projetado para tornar o processo de solicitação, execução e acompanhamento de serviços mais eficiente, organizado e transparente.

## Módulos do Sistema

### 1. Cadastro de Usuários (Cliente, Prestador e ADM)

Permite registrar informações completas dos usuários, como nome, e-mail, endereço, telefone, senha e tipo de conta.  
O ADM pode revisar, ativar ou desativar contas quando necessário.

### 2. Solicitação de Serviços (Cliente)

Os clientes podem enviar pedidos detalhados, informando:

- descrição do serviço,
- categoria,
- endereço,
- disponibilidade,
- anexos (imagens ou vídeos).  
  O prestador recebe a solicitação automaticamente em seu painel.

### 3. Criação de Orçamentos (Prestador)

O prestador pode elaborar orçamentos completos contendo:

- serviços incluídos,
- produtos utilizados,
- custo da mão de obra,
- prazo estimado,
- observações técnicas,
- valor total.

O cliente pode aceitar ou recusar o orçamento.

### 4. Cadastro e Gestão de Produtos (Prestador)

Prestadores que também são lojistas podem cadastrar produtos com:

- nome,
- descrição,
- categoria,
- preço,
- quantidade.  
  Esses produtos podem ser usados nos orçamentos ou vendidos separadamente.

### 5. Gestão de Serviços (Prestador e Cliente)

Após a aprovação do orçamento:

- o serviço é iniciado,
- o prestador atualiza o status (em andamento, concluído, aguardando pagamento),
- o cliente acompanha todo o processo em tempo real.

### 6. Contas a Receber (Prestador)

O prestador acessa valores:

- pendentes,
- recebidos,
- em atraso,  
  com visualização mensal ou total.

### 7. Dashboard do Prestador

O painel exibe informações consolidadas:

- solicitações pendentes,
- serviços concluídos,
- serviços em andamento,
- contas a receber,
- gráficos de desempenho mensal,
- avaliação média dos serviços realizados.

### 8. Sistema de Avaliações

Após a conclusão do serviço, o cliente pode avaliar:

- qualidade,
- atendimento,
- tempo de execução,
- observações adicionais.  
  O nível de avaliação influencia o perfil do prestador.

### 9. Área do Cliente

O cliente pode visualizar:

- solicitações feitas,
- orçamentos recebidos,
- serviços concluídos,
- avaliações enviadas,
- histórico completo.

### 10. Administração da Plataforma (ADM)

O administrador pode:

- monitorar usuários,
- verificar métricas gerais,
- consultar categorias de serviços,
- acompanhar movimentação financeira agregada,
- gerar relatórios.

---

# 3.1 Requisitos Funcionais (RF)

| ID       | Descrição do Requisito                                            |
| :------- | :---------------------------------------------------------------- |
| **RF01** | Cadastrar, editar e excluir usuários (cliente, prestador e ADM).  |
| **RF02** | Permitir solicitação de serviços pelos clientes.                  |
| **RF03** | Enviar notificações de novas solicitações para prestadores.       |
| **RF04** | Permitir criação, edição e envio de orçamentos pelos prestadores. |
| **RF05** | Permitir que clientes aprovem ou rejeitem orçamentos.             |
| **RF06** | Cadastrar e gerenciar produtos para uso nos serviços.             |
| **RF07** | Controlar status dos serviços (pendente, andamento, concluído).   |
| **RF08** | Exibir histórico de serviços para cliente e prestador.            |
| **RF09** | Registrar contas a receber e pagamentos concluídos.               |
| **RF10** | Permitir avaliação dos serviços pelo cliente.                     |
| **RF11** | Exibir dashboard com métricas para o prestador.                   |
| **RF12** | Gerenciar usuários, categorias e relatórios (ADM).                |
| **RF13** | Enviar notificações e alertas relevantes aos usuários.            |
| **RF14** | Armazenar anexos de solicitações (imagens, vídeos).               |
| **RF15** | Gerar relatórios administrativos e operacionais.                  |

---

# 3.2 Requisitos Não Funcionais (RNF)

Os requisitos não funcionais definem os critérios de qualidade do sistema:

- **RNF01 – Desempenho:** As operações devem ser executadas em até 3 segundos.
- **RNF02 – Segurança:** Todas as contas devem ter autenticação segura e dados sensíveis criptografados.
- **RNF03 – Disponibilidade:** O sistema deve permanecer disponível em pelo menos 99% do tempo.
- **RNF04 – Usabilidade:** A interface deve ser intuitiva para clientes, prestadores e administradores.
- **RNF05 – Confiabilidade:** Todas as transações devem ser registradas sem risco de perda de dados.
- **RNF06 – Escalabilidade:** O sistema deve suportar o aumento do número de usuários e solicitações.
- **RNF07 – Compatibilidade:** Interface compatível com navegadores modernos e dispositivos móveis.
- **RNF08 – Manutenibilidade:** Código organizado para facilitar manutenção, atualizações e correções.
- **RNF09 – Privacidade:** Dados pessoais devem ser tratados conforme boas práticas de proteção e LGPD.
- **RNF10 – Backup:** O sistema deve realizar backups regulares dos dados essenciais.
