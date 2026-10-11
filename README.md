[README.md](https://github.com/user-attachments/files/33295106/README.md)
# Assistente de Finanças Pessoais

> Um aplicativo web de organização financeira pessoal que combina conversas em linguagem natural, indicadores simples e Design Universal para tornar o controle das finanças mais acessível.

## Descrição do projeto

Este projeto propõe uma maneira prática e inclusiva de organizar as finanças pessoais. Em vez de depender de planilhas complexas ou de formulários extensos, a pessoa poderá registrar receitas e despesas por meio de mensagens como **“Gastei R$ 45 no supermercado hoje”**. O aplicativo interpretará a mensagem, solicitará confirmação e, nas etapas funcionais do projeto, registrará a movimentação e atualizará os indicadores financeiros.

A solução é pensada principalmente para iniciantes e será desenvolvida com **Design Universal desde o início**: linguagem clara, navegação consistente, compatibilidade com tecnologias assistivas e caminhos alternativos ao chat para realizar tarefas essenciais.

O desenvolvimento é também um projeto de aprendizagem prática de **Vibe Coding**, utilizando o **Lovable** e ciclos curtos de planejamento, implementação, teste e revisão.

## Objetivo

Validar se a interação conversacional, combinada a uma interface simples e acessível, reduz as barreiras para registrar, acompanhar e compreender receitas, despesas e metas financeiras.

## Escopo do MVP

- Registrar receitas e despesas em linguagem natural, com confirmação antes de salvar.
- Classificar transações automaticamente e permitir correções.
- Consultar, editar, excluir e filtrar transações.
- Visualizar receitas, despesas, saldo do período e gráficos acessíveis.
- Criar metas e registrar aportes para acompanhar seu progresso.
- Consultar um agente financeiro que responde a partir dos dados registrados e oferece orientações educativas.
- Utilizar uma alternativa simplificada ao chat para as tarefas essenciais.

**Fora do MVP:** conexão bancária/Open Finance, leitura de comprovantes, áudio, WhatsApp, investimentos avançados, parcelamentos, recorrências automáticas e aplicativo nativo.

## Design Universal e acessibilidade

O Design Universal é um requisito transversal e obrigatório. O aplicativo deve oferecer uso equitativo, flexível, simples e intuitivo, informação perceptível, tolerância ao erro, baixo esforço físico e cognitivo e dimensões apropriadas. As **WCAG 2.2 nível AA** serão referência técnica de acessibilidade digital, com conformidade sujeita a testes.

## Etapas planejadas

1. Protótipo visual responsivo e navegação com dados fictícios.
2. Autenticação, banco de dados e isolamento dos dados de cada usuário.
3. Cadastro e gestão de transações com cálculos determinísticos.
4. Chat com interpretação por IA, validação e confirmação.
5. Dashboard e acompanhamento de metas.
6. Recomendações educativas, testes de segurança, acessibilidade e usabilidade.

## Documentação

- [PRD — Requisitos do Produto](docs/PRD.md)
- [Prompt inicial para o Lovable](docs/PROMPT_INICIAL_LOVABLE.md)

## Como começar no Lovable

1. Leia o [PRD](docs/PRD.md) e use-o como referência para o projeto.
2. Envie o PRD ao Lovable, pedindo análise sem implementação.
3. Após revisar eventuais dúvidas, envie o [prompt inicial](docs/PROMPT_INICIAL_LOVABLE.md) **na mesma conversa**, como instrução para a primeira etapa.
4. Revise a interface, teste navegação e acessibilidade e avance somente após validação.

## Estado do projeto

**Planejamento / preparação do protótipo.** Este repositório documenta o produto proposto; funcionalidades descritas não devem ser interpretadas como já implementadas.

## Princípios técnicos

Dados financeiros reais não devem ser enviados a serviços externos sem base adequada de tratamento e proteção. A IA interpreta solicitações; **cálculos e alterações persistentes** devem ser controlados pela aplicação, com validação, autenticação e autorização. Dados demonstrativos devem ser identificados como fictícios.
