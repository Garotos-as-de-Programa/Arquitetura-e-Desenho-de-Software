# [Marco 3] Síntese dos Requisitos dos Questionários

**Projeto:** Sistema de Gestão de Competências
**Etapa:** 1ª Etapa – Levantamento de Requisitos
**Instrumento:** `Questionario-Gestao-de-Competencias.md` (v1.0)
**Respostas:** `Questionario-1-Respostas.md` (Q1) e `Questionario-2-Respostas.md` (Q2)
**Versão:** 1.0

## 1. Fontes

| Fonte | Respondente | Função / Empresa | Perfil (pergunta 1) | Data | Consentimento | Já entrevistado? |
|-------|-------------|------------------|---------------------|------|---------------|------------------|
| Questionário 1 (Q1) | Mariana Costa Ribeiro | Coordenadora de Operações, Distribuidora Alfa Logística | Gestora, avalia 12 liderados | 11/11/2026 | Sim | Não |
| Questionário 2 (Q2) | Rafael Almeida Nunes | Analista de DHO, Hospital Exemplo Vida | RH/DHO, organiza as avaliações | 11/11/2026 | Sim | Não |

Os telefones constam nos anexos de respostas e não são repetidos aqui (LGPD).

Os dois respondentes são diferentes dos entrevistados, como exige o enunciado, e trazem dois perfis que faltavam nas entrevistas: **quem avalia** (gestora) e **quem organiza** (RH/DHO), de áreas fora de TI (logística e saúde). Isso responde ao ponto 10 da Síntese das Entrevistas e ao risco P-01 do EOR.

## 2. Principais conclusões

1. As seis dores do BPMN foram confirmadas pelos dois respondentes, com destaque para a falta de histórico, a consolidação manual e a desconexão entre 1:1 e avaliação.
2. Questionários por cargo, PDI com metas e lembretes automáticos receberam nota máxima dos dois respondentes.
3. A matriz de habilidades da equipe (RF-034) foi muito valorizada e sobe de Should para Must.
4. A avaliação por pessoas externas (RF-017) foi a funcionalidade de avaliação menos valorizada e desce de Should para Could.
5. O acesso pelo celular é essencial em ambientes sem computador, como o hospital (Q2). Isso contraria a prioridade Could do acesso móvel e gera um novo requisito não funcional (RNF-008).
6. Surgem dois requisitos funcionais novos: reaproveitar dados do ciclo anterior (RF-024) e um painel de pendências por setor para o RH (RF-036).

## 3. Processo atual (perguntas 3 a 5)

| Item | Q1 | Q2 | Convergência com as entrevistas |
|------|----|----|---------------------------------|
| Ferramentas usadas (3) | Planilhas, formulários online, e-mail | Planilhas, formulários online, papel, chat | Confirma: E1 e E2 também citam planilhas, formulários, e-mail e Teams. Q2 acrescenta papel, usado em setores sem computador. |
| Periodicidade do ciclo (4) | Anual | Semestral | Diverge entre todas as fontes (E1: 3 a 6 meses; E2: semestral). Confirma que o ciclo precisa ser configurável (RF-012). |

### Validação das dores do BPMN (pergunta 5, escala 1 a 5)

| Dor do BPMN | Afirmação | Q1 | Q2 | Média | Dor confirmada? |
|-------------|-----------|----|----|-------|-----------------|
| Sem histórico entre ciclos | 5a (nota baixa confirma) | 1 | 2 | 1,5 | Sim |
| Consolidação lenta e retrabalho | 5b (nota alta confirma) | 5 | 4 | 4,5 | Sim |
| Metas travam e ficam esquecidas | 5c (nota baixa confirma) | 2 | 3 | 2,5 | Sim, com menor intensidade em Q2 |
| Questionário genérico | 5d (nota baixa confirma) | 2 | 3 | 2,5 | Sim, com menor intensidade em Q2 |
| 1:1 desconectada da avaliação | 5e (nota baixa confirma) | 2 | 1 | 1,5 | Sim |
| Informação descentralizada / perda de dados | 5f (nota alta confirma) | 4 | 3 | 3,5 | Sim, com menor intensidade em Q2 |

Nenhuma dor foi contestada. As mais fortes, para os dois perfis, são a falta de histórico (5a), a consolidação manual (5b) e a desconexão entre 1:1 e avaliação (5e).

## 4. Importância das funcionalidades (pergunta 6, escala 1 a 5)

Critério: média ≥ 4,5 indica Must; 3,5 a 4,4 indica Should; 2,5 a 3,4 indica Could; abaixo de 2,5 indica Won't. Quando o questionário indica uma prioridade menor que a atual, mas as entrevistas já sustentam a prioridade maior, a prioridade atual é mantida e a divergência fica registrada (seção 7).

| Funcionalidade | Requisito (Lista Consolidada / EOR) | Prioridade atual | Q1 | Q2 | Média | Efeito na prioridade |
|----------------|-------------------------------------|------------------|----|----|-------|----------------------|
| a) Questionários por cargo | RF-008, RF-009 | Must | 5 | 5 | 5,0 | Mantém Must |
| b) 360º entre pares, anônimo | RF-015, RF-044 | Must | 4 | 5 | 4,5 | Mantém Must |
| c) Avaliação ascendente | RF-016 | Should | 3 | 4 | 3,5 | Mantém Should |
| d) Avaliação por externos | RF-017 | Should | 3 | 2 | 2,5 | **Desce para Could** |
| e) Radar autoavaliação × gestor | RF-032 | Must | 4 | 3 | 3,5 | Mantém Must (pedido por E1 e E2); divergência registrada |
| f) Comparação entre ciclos | RF-033 | Must | 5 | 4 | 4,5 | Mantém Must |
| g) Matriz de habilidades | RF-034 | Should | 5 | 4 | 4,5 | **Sobe para Must** |
| h) PDI com metas, prazos e status | RF-028, RF-029 | Must | 5 | 5 | 5,0 | Mantém Must |
| i) 1:1 ligado ao PDI | RF-026, RF-027 | Must | 4 | 3 | 3,5 | Mantém Must (indispensável para E1); divergência registrada |
| j) Lembretes automáticos | RF-037, RF-038 | Must | 5 | 5 | 5,0 | Mantém Must (RF-037); canais extras Could (RF-038) |
| k) Integrações | RF-050, RF-051 | Could | 2 | 3 | 2,5 | Mantém Could |
| l) Badges | RF-031 | Could | 2 | 3 | 2,5 | Mantém Could |

## 5. Pontos em aberto respondidos (perguntas 7 a 14)

| Ponto em aberto | Pergunta | Q1 | Q2 | Decisão proposta | Requisito afetado |
|-----------------|----------|----|----|------------------|-------------------|
| Quem cria os questionários (D-02) | 7 | RH e gestor, em conjunto | Somente o RH | O RH cria e publica os questionários. O gestor pode propor e editar competências técnicas da sua área, e a publicação depende de aprovação do RH. | RF-010 |
| Quem define avaliadores do 360º (D-03) | 8 | O avaliado indica e o gestor aprova | O RH | O avaliado indica e o gestor aprova. O RH pode incluir ou remover avaliadores antes de o ciclo abrir. | RF-018 |
| Mínimo de respondentes (D-04) | 9 | A partir de 3 | A partir de 5 | O mínimo é configurável pelo RH, com padrão proposto 3 (mesma referência do Lattice) e possibilidade de aumentar. | RF-019 |
| Visibilidade e papéis RH/DP/DHO (D-05) | 10 | Colaborador, gestor direto, RH | Colaborador, gestor direto, RH, DHO | Confirma RN-01. Nenhum respondente marcou diretoria ou colegas: a diretoria não acessa dados individuais e colegas nunca acessam. | RF-003, RN-01 |
| Prazo de retenção (D-06) | 11 | Enquanto durar o vínculo | Até 5 anos | Sem consenso. O prazo continua configurável por organização (RF-049) e o ponto D-06 segue em aberto, para definição com apoio jurídico. | RF-049, RNF-013 |
| Canal das notificações (D-07) | 12 | E-mail; notificação no sistema | Notificação no sistema; celular | A notificação dentro do sistema é obrigatória (RF-037, Must). E-mail e push no celular são canais adicionais (RF-038, Could). | RF-037, RF-038 |
| Rankings (D-09) | 13 | Negativo | Indiferente | Nenhum respondente vê ranking como positivo. Mantém RN-07. | RF-031, RN-07 |
| Prioridade do acesso móvel (D-08) | 14 | Principalmente no computador | Nos dois, na mesma medida | O acesso móvel deixa de ser só para notificações. Ver RNF-008 na seção 6. | RNF-008 |

## 6. Requisitos novos (perguntas 14 a 16)

### RF-024 – Reaproveitamento de ciclo

| Campo | Conteúdo |
|-------|----------|
| ID | RF-024 |
| Título | Reaproveitamento de ciclo |
| Descrição | Como gestor, eu quero que um novo ciclo já traga as informações do ciclo anterior, para apenas atualizar o que mudou em vez de preencher tudo de novo. |
| Critérios de aceitação | 1. Ao abrir um novo ciclo, o sistema traz automaticamente o questionário, as competências, os avaliadores do 360º e as metas do PDI não concluídas do ciclo anterior.<br>2. O gestor/RH pode alterar ou remover qualquer item trazido.<br>3. As notas do ciclo anterior **não** são copiadas para as avaliações do novo ciclo (RN-06). |
| Prioridade | Should |
| Fonte(s) | Questionário 1 (pergunta 16) |
| Status | Proposto |

### RF-036 – Painel de pendências por setor

| Campo | Conteúdo |
|-------|----------|
| ID | RF-036 |
| Título | Painel de pendências por setor |
| Descrição | Como RH, eu quero ver quais avaliações estão atrasadas em cada setor, para cobrar os gestores antes do fim do prazo. |
| Critérios de aceitação | 1. O painel agrupa por setor as etapas do ciclo pendentes e atrasadas.<br>2. O RH pode enviar, a partir do painel, um lembrete aos gestores dos setores com pendências.<br>3. O painel mostra quantidades e status, sem exibir notas. |
| Prioridade | Should |
| Fonte(s) | Questionário 2 (pergunta 15) |
| Status | Proposto |

> Complementa o RF-020, que exibe o status de cada etapa por colaborador.

### RNF-008 – Responsividade móvel

| Campo | Conteúdo |
|-------|----------|
| ID | RNF-008 |
| Título | Responsividade móvel |
| Descrição | A autoavaliação, a avaliação de pares, a consulta de resultados e a atualização das metas do PDI devem funcionar pelo navegador do celular, sem aplicativo nativo. |
| Critério de verificação | Em tela de 360 px de largura, as quatro tarefas são concluídas sem rolagem horizontal e sem perda de função em relação ao computador. |
| Prioridade | Should |
| Fonte(s) | Questionário 2 (perguntas 3, 14 e 15); restrição do enunciado (web, com perspectiva futura de uso em dispositivos móveis) |
| Status | Proposto |

> Resolve a divergência D-08 da Consolidação da Elicitação.

### Respostas que confirmam requisitos existentes

| Resposta | Requisito confirmado |
|----------|----------------------|
| Q1, pergunta 15: ver a equipe por competência e saber quem precisa de treinamento | RF-034 (sobe para Must, seção 4) |
| Q2, pergunta 16: o gestor não pode ver quem respondeu no 360º | RF-015, RF-044, RNF-005, RN-04 |
| Q2, pergunta 16: o gestor não pode alterar nota depois de encerrado o ciclo | RF-022, RN-03 |

## 7. Divergências e pontos a validar

1. **Periodicidade:** anual (Q1), semestral (Q2 e E2), de 3 a 6 meses (E1). Resolvido pela configuração do ciclo (RF-012).
2. **Autoria dos questionários e escolha dos avaliadores:** a gestora quer participar, e o RH quer centralizar. A decisão da seção 5 dá a palavra final ao RH, com participação do gestor (RF-010, RF-018). Validar na revisão cruzada.
3. **Mínimo de respondentes:** 3 (Q1) × 5 (Q2). Resolvido com valor configurável e padrão proposto 3 (RF-019).
4. **Prazo de retenção:** sem consenso. Segue em aberto (D-06, RF-049).
5. **Radar e 1:1 (RF-032, RF-026, RF-027):** os questionários indicam Should, e as entrevistas indicam Must. A prioridade Must foi mantida e deve ser confirmada na revisão cruzada.
6. **Acesso móvel:** Q1 usa o computador, e Q2 precisa do celular. Atendido pelo RNF-008 como Should, sem aplicativo nativo.
7. **IDs consolidados:** RF-024, RF-036 e RNF-008 já estão integrados na numeração unificada da Lista Geral de Requisitos Consolidada (RF-001 a RF-051 e RNF-001 a RNF-016) e nas matrizes de rastreabilidade.
8. **Tamanho da amostra:** são duas respostas. As médias indicam tendência e não têm valor estatístico.
