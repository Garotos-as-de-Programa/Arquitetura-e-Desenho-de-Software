# Síntese dos Requisitos dos Questionários

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
3. A matriz de habilidades da equipe (RF-035) foi muito valorizada e sobe de Should para Must.
4. A avaliação por pessoas externas (RF-053) foi a funcionalidade de avaliação menos valorizada e desce de Should para Could.
5. O acesso pelo celular é essencial em ambientes sem computador, como o hospital (Q2). Isso contraria a prioridade Could do acesso móvel e gera um novo requisito não funcional (RNF-017).
6. Surgem dois requisitos funcionais novos: reaproveitar dados do ciclo anterior (RF-074) e um painel de pendências por setor para o RH (RF-075).

## 3. Processo atual (perguntas 3 a 5)

| Item | Q1 | Q2 | Convergência com as entrevistas |
|------|----|----|---------------------------------|
| Ferramentas usadas (3) | Planilhas, formulários online, e-mail | Planilhas, formulários online, papel, chat | Confirma: E1 e E2 também citam planilhas, formulários, e-mail e Teams. Q2 acrescenta papel, usado em setores sem computador. |
| Periodicidade do ciclo (4) | Anual | Semestral | Diverge entre todas as fontes (E1: 3 a 6 meses; E2: semestral). Confirma que o ciclo precisa ser configurável (RF-015). |

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

| Funcionalidade | Requisito (EOR) | Prioridade atual | Q1 | Q2 | Média | Efeito na prioridade |
|----------------|-----------------|------------------|----|----|-------|----------------------|
| a) Questionários por cargo | RF-046 | Must | 5 | 5 | 5,0 | Mantém Must |
| b) 360º entre pares, anônimo | RF-050, RF-054 | Must | 4 | 5 | 4,5 | Mantém Must |
| c) Avaliação ascendente | RF-052 | Should | 3 | 4 | 3,5 | Mantém Should |
| d) Avaliação por externos | RF-053 | Should | 3 | 2 | 2,5 | **Desce para Could** |
| e) Radar autoavaliação × gestor | RF-059 | Must | 4 | 3 | 3,5 | Mantém Must (pedido por E1 e E2); divergência registrada |
| f) Comparação entre ciclos | RF-060 | Must | 5 | 4 | 4,5 | Mantém Must |
| g) Matriz de habilidades | RF-035 | Should | 5 | 4 | 4,5 | **Sobe para Must** |
| h) PDI com metas, prazos e status | RF-025, RF-026 | Must | 5 | 5 | 5,0 | Mantém Must |
| i) 1:1 ligado ao PDI | RF-067 a RF-069 | Must | 4 | 3 | 3,5 | Mantém Must (indispensável para E1); divergência registrada |
| j) Lembretes automáticos | RF-065 | Must | 5 | 5 | 5,0 | Mantém Must |
| k) Integrações | RF-071, RF-072 | Could | 2 | 3 | 2,5 | Mantém Could |
| l) Badges | RF-073 | Could | 2 | 3 | 2,5 | Mantém Could |

## 5. Pontos em aberto respondidos (perguntas 7 a 14)

| Ponto em aberto | Pergunta | Q1 | Q2 | Decisão proposta | Requisito afetado |
|-----------------|----------|----|----|------------------|-------------------|
| Quem cria os questionários (P-07) | 7 | RH e gestor, em conjunto | Somente o RH | O RH cria e publica os questionários. O gestor pode propor e editar competências técnicas da sua área, e a publicação depende de aprovação do RH. | RF-046 |
| Quem define avaliadores do 360º (P-07) | 8 | O avaliado indica e o gestor aprova | O RH | O avaliado indica e o gestor aprova. O RH pode incluir ou remover avaliadores antes de o ciclo abrir. | RF-051 |
| Mínimo de respondentes (P-10) | 9 | A partir de 3 | A partir de 5 | O mínimo é configurável pelo RH, com padrão 3 (mesma referência do Lattice) e possibilidade de aumentar. | RF-055 |
| Visibilidade e papéis RH/DP/DHO (P-03) | 10 | Colaborador, gestor direto, RH | Colaborador, gestor direto, RH, DHO | Confirma RN04. Nenhum respondente marcou diretoria ou colegas: a diretoria não acessa dados individuais e colegas nunca acessam. | RF-004, RN04 |
| Prazo de retenção (P-05) | 11 | Enquanto durar o vínculo | Até 5 anos | Sem consenso. O prazo continua configurável por organização (RF-070) e o ponto P-05 segue em aberto, para definição com apoio jurídico. | RF-070, RNF-013 |
| Canal das notificações | 12 | E-mail; notificação no sistema | Notificação no sistema; celular | A notificação dentro do sistema é obrigatória (comum aos dois). E-mail e push no celular são canais adicionais, escolhidos pelo usuário. | RF-065 |
| Rankings | 13 | Negativo | Indiferente | Nenhum respondente vê ranking como positivo. Mantém RN05. | RN05 |
| Prioridade do acesso móvel (P-12) | 14 | Principalmente no computador | Nos dois, na mesma medida | O acesso móvel deixa de ser só para notificações. Ver RNF-017 na seção 6. | RF-066, RNF-010 |

## 6. Requisitos novos (perguntas 14 a 16)

### RF-074 – Reaproveitamento de dados do ciclo anterior

| Campo | Conteúdo |
|-------|----------|
| ID | RF-074 |
| Título | Pré-preenchimento a partir do ciclo anterior |
| Descrição | Como gestor, eu quero que um novo ciclo já traga as informações do ciclo anterior, para apenas atualizar o que mudou em vez de preencher tudo de novo. |
| Critérios de aceitação | 1. Ao abrir um novo ciclo, o sistema traz automaticamente o questionário, as competências, os avaliadores do 360º e as metas do PDI não concluídas do ciclo anterior.<br>2. O gestor pode alterar ou remover qualquer item trazido.<br>3. As notas do ciclo anterior **não** são copiadas para as avaliações do novo ciclo. |
| Prioridade | Should |
| Fonte(s) | Questionário 1 (pergunta 16) |
| Status | Proposto |

### RF-075 – Painel de pendências por setor

| Campo | Conteúdo |
|-------|----------|
| ID | RF-075 |
| Título | Painel de pendências do ciclo por setor |
| Descrição | Como RH, eu quero ver quais avaliações estão atrasadas em cada setor, para cobrar os gestores antes do fim do prazo. |
| Critérios de aceitação | 1. O painel agrupa por setor as etapas do ciclo pendentes e atrasadas.<br>2. O RH pode enviar, a partir do painel, um lembrete aos gestores dos setores com pendências.<br>3. O painel mostra quantidades e status, sem exibir notas. |
| Prioridade | Should |
| Fonte(s) | Questionário 2 (pergunta 15) |
| Status | Proposto |

> Complementa o RF-049, que exibe o status de cada etapa por colaborador.

### RNF-017 – Uso em celular

| Campo | Conteúdo |
|-------|----------|
| ID | RNF-017 |
| Título | Responsividade das tarefas do colaborador |
| Descrição | A autoavaliação, a avaliação de pares, a consulta de resultados e a atualização das metas do PDI devem funcionar pelo navegador do celular, sem aplicativo nativo. |
| Critério de verificação | Em tela de 360 px de largura, as quatro tarefas são concluídas sem rolagem horizontal e sem perda de função em relação ao computador. |
| Prioridade | Should |
| Fonte(s) | Questionário 2 (perguntas 3, 14 e 15); restrição do enunciado (web, com perspectiva futura de uso em dispositivos móveis) |
| Status | Proposto |

> Amplia o RF-066 (Could), que cobre só notificações e prazos. Resolve o ponto P-12 do EOR.

### Respostas que confirmam requisitos existentes

| Resposta | Requisito confirmado |
|----------|----------------------|
| Q1, pergunta 15: ver a equipe por competência e saber quem precisa de treinamento | RF-035 (sobe para Must, seção 4) |
| Q2, pergunta 16: o gestor não pode ver quem respondeu no 360º | RF-054, RNF-014, RN01, RN03 |
| Q2, pergunta 16: o gestor não pode alterar nota depois de encerrado o ciclo | RF-063 |

## 7. Divergências e pontos a validar

1. **Periodicidade:** anual (Q1), semestral (Q2 e E2), de 3 a 6 meses (E1). Resolvido pela configuração do ciclo (RF-015).
2. **Autoria dos questionários e escolha dos avaliadores:** a gestora quer participar, e o RH quer centralizar. A decisão da seção 5 dá a palavra final ao RH, com participação do gestor. Validar na revisão cruzada.
3. **Mínimo de respondentes:** 3 (Q1) × 5 (Q2). Resolvido com valor configurável e padrão 3.
4. **Prazo de retenção:** sem consenso. Segue em aberto (P-05).
5. **Radar e 1:1 (RF-059, RF-067 a RF-069):** os questionários indicam Should, e as entrevistas indicam Must. A prioridade Must foi mantida e deve ser confirmada na revisão cruzada.
6. **Acesso móvel:** Q1 usa o computador, e Q2 precisa do celular. Atendido pelo RNF-017 como Should, sem aplicativo nativo.
7. **IDs novos:** RF-074, RF-075 e RNF-017 seguem a numeração do EOR (último RF: RF-073; último RNF: RNF-016). Devem entrar na Lista Geral e na matriz de rastreabilidade com a fonte indicada.
8. **Tamanho da amostra:** são duas respostas. As médias indicam tendência e não têm valor estatístico.
