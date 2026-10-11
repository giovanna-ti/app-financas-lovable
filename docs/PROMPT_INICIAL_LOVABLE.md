# Prompt inicial para o Lovable — Etapa 1: interface e navegação

## Contexto para o Lovable

Atue como um desenvolvedor full stack experiente em UX/UI, **Design Universal** e acessibilidade digital. Estou criando o **Assistente de Finanças Pessoais**, um aplicativo web no qual usuários poderão organizar suas finanças por meio de conversas em linguagem natural. O **[PRD do projeto](PRD.md)** é a referência dos requisitos e limitações.

Quero desenvolver o produto progressivamente, compreender as decisões técnicas e validar cada etapa antes de avançar.

## Objetivo desta etapa

Implemente **somente o protótipo visual navegável do MVP**, com dados demonstrativos fictícios e claramente identificados. Não construa funcionalidades de backend nesta etapa.

## Diretriz obrigatória: Design Universal

Adote os princípios do Design Universal em todas as telas e interações. Use **WCAG 2.2 nível AA** como referência técnica, sem presumir conformidade antes dos testes.

- Linguagem clara e simples; navegação previsível e consistente.
- Contraste suficiente, fontes legíveis, foco visível e componentes semanticamente corretos.
- Navegação por teclado; controles com rótulos acessíveis e alvos de toque adequados.
- Gráficos com descrições e dados textuais; não comunicar informações apenas com cores.
- Estados de carregamento, erro, confirmação e ausência de dados com mensagens compreensíveis.
- Layout responsivo para celular, tablet e desktop, mantendo a utilidade com ampliação.
- Caminhos convencionais simplificados para as ações essenciais, sem obrigar o usuário a usar o chat.
- Evitar animações desnecessárias e respeitar a redução de movimento.

Em decisões de interface, priorize compreensão, acessibilidade e autonomia antes de efeitos visuais decorativos.

## Identidade visual

Interface moderna, minimalista e acolhedora, com tons de azul e cores neutras, mantendo contraste adequado. Evite excesso de informações e preserve uma hierarquia visual consistente.

## Telas que devem ser criadas

### 1. Dashboard

Cartões de receitas, despesas e saldo; gráfico de despesas por categoria; evolução mensal; acesso rápido ao chat. Mostrar os dados como **demonstração**.

### 2. Chat financeiro

Interface semelhante a um mensageiro, com exemplos de mensagens, como:

- “Gastei R$ 45 no supermercado hoje.”
- “Quanto gastei com alimentação este mês?”
- “Quero economizar R$ 3.000 para uma viagem.”

Adicionar sugestões de mensagens e **cartões demonstrativos** de confirmação. Não simular salvamento real.

### 3. Transações

Lista ilustrativa de receitas e despesas, filtros visuais e ações de edição/exclusão sem persistência. Incluir uma **alternativa simplificada de registro manual**, apenas como protótipo visual.

### 4. Metas financeiras

Lista de metas, valor desejado, valor acumulado, prazo, progresso e botão de criação. Mostrar exemplos fictícios.

### 5. Configurações

Seções visuais para conta, acessibilidade, privacidade e gerenciamento de dados. Não implementar operações reais.

### 6. Acesso

Telas demonstrativas de login, cadastro e recuperação de senha, sem autenticação real.

## Navegação e comportamento

- Implementar navegação visual e funcional entre as telas.
- Garantir indicação da página atual, caminho de retorno e acesso às ações principais.
- Criar estados vazios e mensagens de feedback demonstrativas.
- Evitar que botões pareçam executar operações reais quando ainda não executam; sinalizar ações como indisponíveis ou demonstrativas.

## Restrições explícitas

- Não implementar autenticação, banco de dados, integração com IA, APIs bancárias ou serviços financeiros.
- Não armazenar dados financeiros reais nem usar credenciais ou chaves nesta etapa.
- Não acrescentar funcionalidades fora do PRD.
- Não apresentar dados simulados como se fossem registros reais.
- Manter componentes reutilizáveis e estrutura de código organizada para evolução posterior.

## Entregáveis e explicação didática

Ao concluir:

1. Apresente o protótipo navegável.
2. Explique os componentes e os arquivos principais.
3. Descreva a organização da navegação.
4. Indique como os princípios do Design Universal foram aplicados.
5. Liste limitações de acessibilidade que ainda precisam ser verificadas.
6. Sugira a próxima etapa, **sem implementá-la automaticamente**.

**Não avance para autenticação, banco de dados ou IA sem minha solicitação.**

---

## Mensagem opcional para enviar antes do prompt

> Este é o PRD do aplicativo de Organização de Finanças Pessoais. Utilize-o como referência permanente do projeto. Neste momento, apenas revise os requisitos, identifique inconsistências e dúvidas e não implemente nenhuma funcionalidade. Após minha validação, enviarei o prompt específico da primeira etapa.
