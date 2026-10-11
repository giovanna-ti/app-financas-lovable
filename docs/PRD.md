# PRD — Assistente de Finanças Pessoais

**Versão:** 1.1 — MVP  
**Plataforma:** Aplicação web responsiva  
**Desenvolvimento:** Lovable  
**Idioma:** Português brasileiro  
**Moeda:** Real brasileiro (BRL)  
**Diretriz transversal:** Design Universal

## 1. Descrição inicial e visão do produto

O **Assistente de Finanças Pessoais** será um aplicativo web de organização financeira que utiliza conversas em linguagem natural para registrar receitas e despesas, consultar gastos e acompanhar metas. Seu diferencial é combinar **interação conversacional, simplicidade e Design Universal**. A solução pretende reduzir a dependência de formulários e planilhas, mantendo meios alternativos de interação para pessoas que não queiram ou não possam utilizar o chat.

## 2. Problema

Pessoas iniciantes podem abandonar o acompanhamento das finanças quando o registro exige esforço excessivo, navegação complexa e classificações manuais. Interfaces pouco acessíveis também criam barreiras. O aplicativo buscará tornar o registro e a leitura da situação financeira mais simples e inclusivos.

## 3. Público-alvo

Pessoas que desejam iniciar o controle financeiro, incluindo estudantes, jovens adultos, usuários sem experiência com planilhas e pessoas com diferentes necessidades de acessibilidade ou familiaridade tecnológica.

## 4. Objetivo e hipótese do MVP

**Objetivo:** validar se uma experiência conversacional acompanhada por navegação acessível facilita o registro, a consulta e a compreensão das movimentações financeiras.

**Hipótese:** usuários iniciantes conseguirão registrar suas movimentações e consultar indicadores com menos dificuldade do que em fluxos manuais complexos.

## 5. Requisitos funcionais

### RF01 — Conta e autenticação

- Permitir cadastro, login e recuperação de senha por e-mail.
- Vincular os dados financeiros à conta autenticada.
- Impedir acesso aos registros de outro usuário, inclusive por chamadas diretas ao banco ou à API.
- Exibir orientações e erros de maneira acessível.

### RF02 — Registro de transações por chat

- Aceitar frases como “Gastei R$ 35 no almoço hoje”, “Recebi R$ 2.500 de salário ontem” e “Paguei R$ 120 de internet no dia 5”.
- Extrair **tipo** (receita/despesa), **valor**, **categoria**, **data** e **descrição**.
- Apresentar os campos interpretados para confirmação **antes de persistir**.
- Solicitar esclarecimento se algum dado indispensável estiver ausente ou ambíguo, sem inventá-lo.
- Após confirmação, salvar a transação e atualizar os indicadores.
- Disponibilizar também registro simplificado por interface convencional acessível.

### RF03 — Classificação automática

- Categorias de despesas: Alimentação, Moradia, Transporte, Saúde, Educação, Lazer, Compras, Contas e serviços e Outros.
- Categorias de receitas: Salário, Trabalho extra, Rendimentos e Outras receitas.
- Permitir correção de categoria; quando houver incerteza, solicitar confirmação ou usar “Outros”, de maneira explícita.

### RF04 — Histórico e gestão de transações

- Listar movimentações por data e permitir filtro por período, categoria e tipo.
- Permitir consulta, edição e exclusão com confirmação quando houver mudança ou exclusão relevante.
- Recalcular imediatamente os indicadores após alterações persistidas.
- Não depender apenas de cor para distinguir entradas e saídas.

### RF05 — Dashboard

- Exibir receitas, despesas e **saldo do período = receitas − despesas**.
- Mostrar distribuição das despesas por categoria e evolução mensal quando existirem dados suficientes.
- Calcular totais com base nas transações efetivamente armazenadas, nunca em valores inventados pelo modelo de IA.
- Exibir estados vazios e descrições textuais equivalentes para os gráficos.

### RF06 — Metas

- Permitir criar metas com nome, valor-alvo, prazo e valor inicial acumulado.
- Exibir total acumulado, percentual atingido e valor restante.
- Permitir aportes manuais associados à meta.
- Não confundir saldo do período com valor reservado; aportes não geram automaticamente uma despesa na versão inicial.
- Exibir progresso também em texto, sem depender somente de barras ou cores.

### RF07 — Agente Financeiro

- Responder perguntas como “Quanto gastei em alimentação este mês?”, “Qual foi minha maior categoria de despesas?” e “Quanto falta para minha meta de viagem?”.
- Utilizar exclusivamente dados do usuário autenticado e indicar quando eles forem insuficientes.
- Oferecer recomendações de economia simples, contextualizadas e educativas, sem promessa de resultado ou recomendação individualizada de investimentos.
- Não modificar registros por meio de consultas que apenas solicitam informações.
- Utilizar linguagem clara, respeitosa e compreensível.

## 6. Regras de negócio

1. Todas as transações pertencem a um usuário autenticado e serão registradas em BRL.
2. Interpretar datas no fuso do usuário; padrão inicial: **America/Sao_Paulo**. Datas ambíguas devem ser confirmadas.
3. O saldo do período corresponde à soma das receitas menos a soma das despesas selecionadas.
4. Nenhuma transação é persistida sem confirmação explícita.
5. Edições e exclusões exigem confirmação e atualizam os indicadores.
6. Reenvios ou falhas de rede não podem gerar duplicidade de lançamentos confirmados.
7. Respostas do agente devem distinguir fatos registrados, inferências e estimativas.
8. Tarefas essenciais devem ser realizáveis sem uso do chat.
9. Valores financeiros importantes devem ser identificados por texto, não apenas por cor.
10. Valores monetários devem ter representação decimal exata, sem depender de arredondamento binário de ponto flutuante.

## 7. Telas do MVP

1. **Acesso:** cadastro, login, recuperação de senha e breve apresentação.
2. **Dashboard:** cartões de indicadores, gráficos e acesso rápido ao chat.
3. **Chat financeiro:** mensagens, sugestões de perguntas, resultados e cartões de confirmação.
4. **Transações:** histórico, filtros, edição, exclusão e registro alternativo simplificado.
5. **Metas:** criação, edição, acompanhamento e aportes.
6. **Configurações:** conta, preferências de acessibilidade, privacidade e exclusão dos dados.

## 8. Design Universal, acessibilidade e usabilidade

O aplicativo deverá incorporar **Design Universal desde a concepção**, sem tratar acessibilidade como recurso opcional ou melhoria posterior. Os princípios abaixo abrangem a interface visual, a navegação, o chat e a interpretação das informações financeiras.

### DU01 — Uso equitativo

Oferecer acesso às funções essenciais a pessoas com diferentes capacidades e experiência tecnológica, sem segregação ou barreiras desnecessárias.

### DU02 — Flexibilidade de uso

Permitir interação por chat **e** por controles convencionais simplificados. As funcionalidades essenciais devem funcionar por teclado, mouse e toque.

### DU03 — Uso simples e intuitivo

Empregar linguagem direta, ações previsíveis, navegação consistente, orientação contextual e mensagens de erro compreensíveis. Não exigir conhecimento prévio de finanças ou memorização de comandos.

### DU04 — Informação perceptível

Assegurar contraste adequado; disponibilizar títulos, rótulos, descrições de gráficos e equivalentes textuais para indicadores. Evitar comunicação exclusiva por cores, ícones ou animações.

### DU05 — Tolerância ao erro

Confirmar operações relevantes; permitir revisar e corrigir interpretações; explicar como resolver erros; preservar dados durante falhas e prevenir duplicidades.

### DU06 — Baixo esforço físico e cognitivo

Minimizar etapas, informações simultâneas e gestos complexos; apresentar os dados progressivamente; respeitar preferências de redução de movimento.

### DU07 — Dimensão e espaço adequados

Projetar alvos de toque confortáveis, espaçamento suficiente e layouts que se adaptem a dispositivos e níveis de ampliação.

### DU08 — Acessibilidade digital

Usar **WCAG 2.2 nível AA** como referência técnica; assegurar semântica adequada, foco visível, ordem de navegação lógica, acessibilidade por teclado, rótulos compreensíveis e atualizações acessíveis do chat sem anúncios excessivos. Compatibilidade real com tecnologias assistivas precisa ser verificada por testes, não apenas inferida do código.

**Critérios de aceitação de acessibilidade:** as tarefas essenciais devem funcionar sem chat; os principais fluxos devem ser utilizáveis por teclado e tecnologias assistivas; a interface deve permanecer utilizável com ampliação de pelo menos 200%; gráficos precisam de equivalentes textuais; verificações dos critérios aplicáveis das WCAG 2.2 AA e testes com usuários devem identificar e resolver bloqueios críticos.

## 9. Requisitos não funcionais

### Usabilidade e desempenho

- Interface responsiva, legível e consistente, com estados de carregamento, sucesso, erro e ausência de dados.
- Feedback perceptível durante operações, sem prometer tempos de resposta não medidos.
- Estrutura de componentes reutilizáveis para facilitar manutenção.

### Segurança e privacidade

- Proteger autenticação, comunicação e acesso aos dados no servidor/banco.
- Manter chaves e credenciais exclusivamente em ambiente seguro, não no frontend.
- Aplicar controle de acesso por registro, minimização de dados e política de privacidade compatível com o tratamento realizado e a LGPD.
- Permitir exclusão de conta e dados, observadas obrigações legais aplicáveis.

### Confiabilidade

- Separar interpretação da IA de cálculos e operações persistentes.
- Usar validação de valores, datas e permissões.
- Prevenir registros duplicados e informar falhas sem mascará-las.

## 10. Modelo inicial de dados

| Entidade | Campos principais |
| --- | --- |
| Usuários | id, e-mail, data de criação |
| Transações | id, usuário_id, tipo, valor, categoria, descrição, data da transação, data de criação |
| Metas | id, usuário_id, nome, valor-alvo, prazo, valor inicial acumulado |
| Aportes em metas | id, meta_id, valor, data do aporte |

Os aportes compõem o progresso da meta, mas não são lançados automaticamente como despesas no MVP.

## 11. Critérios de aceitação do MVP

- [ ] Cadastro e acesso funcionam com isolamento real entre contas.
- [ ] “Gastei R$ 45 com transporte hoje” apresenta dados corretos para confirmação e só então é salvo.
- [ ] Receitas aumentam e despesas diminuem corretamente o saldo do período.
- [ ] Edição/exclusão recalculam indicadores.
- [ ] Histórico filtra por categoria e período.
- [ ] Meta de R$ 1.000 com R$ 250 acumulados indica 25%.
- [ ] Agente responde usando registros do usuário, sem inventar valores.
- [ ] Mensagens ambíguas geram pedidos de esclarecimento.
- [ ] Reenvio de uma confirmação não duplica registros.
- [ ] As tarefas essenciais funcionam sem chat, incluindo por teclado.
- [ ] Gráficos, cores e controles têm informações acessíveis equivalentes.
- [ ] Fluxos essenciais são avaliados quanto às WCAG 2.2 AA e a barreiras críticas.

## 12. Fora do escopo

- Open Finance e sincronização bancária.
- Leitura automática de comprovantes, áudio e WhatsApp.
- Investimentos avançados, cartões parcelados e projeções complexas.
- Transações recorrentes automáticas, notificações inteligentes e aplicativos nativos.

## 13. Validação inicial

Convidar, preferencialmente, **5 a 10 participantes** com níveis diferentes de experiência tecnológica e, quando possível, necessidades variadas de acessibilidade. Solicitar o registro de movimentações, consulta a gastos e criação/acompanhamento de metas.

**Métricas:** acerto de interpretação, tempo de registro, correções necessárias, conclusão sem ajuda, facilidade percebida, interesse em continuar usando e barreiras de acessibilidade.

**Metas preliminares de validação:** pelo menos 80% das interpretações de teste corretas e 80% dos participantes concluindo tarefas essenciais sem ajuda, além de ausência de bloqueios críticos de acessibilidade. Esses critérios são hipóteses de teste, não resultados comprovados; uma amostra pequena não comprova conformidade geral.

## 14. Plano de implementação no Lovable

1. Interface e navegação acessíveis com dados fictícios claramente identificados.
2. Autenticação e banco de dados.
3. Cadastro/edição/exclusão de transações e cálculos confiáveis.
4. Integração do modelo de IA e fluxo de confirmação.
5. Dashboard e metas com dados reais.
6. Recomendações contextualizadas, testes e refinamentos.

O PRD será a fonte de referência; cada etapa deve ser implementada e validada separadamente, sem adicionar recursos não solicitados. A IA interpreta a intenção; a aplicação controla validação, cálculos, autenticação e persistência. O Design Universal aplica-se a todas as etapas.

## 15. Resultado esperado

Um aplicativo web de finanças pessoais que reúna **conversação natural, indicadores confiáveis e Design Universal**, oferecendo a iniciantes uma maneira acessível e compreensível de organizar suas informações financeiras.
