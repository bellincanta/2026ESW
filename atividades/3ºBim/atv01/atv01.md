# ATIVIDADE 01 — ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE (SRS)
## Sistema de Agendamento de Consultório Médico — Etapa 1

**Disciplina:** Engenharia de Software — TADS · IFPR Campus Cascavel
**Professor:** Nelson Bellincanta Filho

---

## INTRODUÇÃO

Na **Atividade 01 do 2º Bimestre** você analisou o estudo de caso da clínica médica e levantou os primeiros requisitos funcionais e não funcionais do sistema de agendamento. Agora esses requisitos vão ser organizados em um documento formal: a **Especificação de Requisitos de Software (SRS)**.

O SRS é o documento que a equipe de desenvolvimento usa para construir e testar o sistema. Por isso, tudo o que for escrito nele precisa ser **claro, completo, sem ambiguidade e verificável**.

O trabalho será construído em etapas. Nesta **Etapa 1** você deve elaborar as seguintes seções do SRS:

| Seção | Conteúdo |
|:-----:|:---------|
| 1 | Introdução |
| 2 | Descrição Geral |
| 3 | Requisitos Específicos — 3.1 Requisitos Funcionais (RF) · 3.2 Requisitos Não Funcionais (RNF) |
| 4 | Casos de Uso — descrições e Diagrama de Caso de Uso |

As seções de Backlog do Produto, Matriz de Rastreabilidade, Glossário e Anexos ficam para as próximas etapas.

---

## MATERIAL DE APOIO

- **Estudo de caso:** `atv01.md` (Sistema de Agendamento de Consultório Médico)
- **Suas respostas da Atividade 01:** ponto de partida para os RF e RNF — revise e melhore o que for necessário
- **Template LaTeX do SRS:** [📥 Baixar o template SRS.zip](SRS.zip) (importe no Overleaf em *New Project → Upload Project*)

O template contém exemplos de um **sistema de imobiliária** (RF01, RF02, RNF01 e UC01). Eles servem **apenas como modelo de estrutura**. Substitua todos os exemplos pelo conteúdo do sistema da clínica.

---

## O QUE DEVE SER FEITO

### Antes de começar — capa e metadados

- Altere o título para **Sistema de Agendamento de Consultório Médico**
- Troque "Sistema ImoBill" e o nome do autor na capa pelos seus dados
- Remova os textos em itálico de *Orientação* depois de preencher cada seção

---

### SEÇÃO 1: Introdução

No template, as subseções da Introdução estão comentadas (linhas iniciadas com `%`). **Remova o `%`** e preencha:

- **1.1 Finalidade:** o que este documento pretende alcançar e quem vai usá-lo
- **1.2 Escopo:** nome do sistema, o que ele fará em alto nível e o que **não** faz parte do escopo (ex.: prontuário eletrônico completo, faturamento de convênios)
- **1.3 Definições, Acrônimos e Abreviações:** termos usados no documento (ex.: SRS, RF, RNF, UC, LGPD, *no-show*)
- **1.4 Referências:** bibliografia e documentos consultados, no padrão **ABNT NBR 6023**
- **1.5 Visão Geral do Documento:** como o SRS está organizado

---

### SEÇÃO 2: Descrição Geral

Apresente a **visão macro** do sistema, **sem detalhar requisitos** ainda. Preencha:

- **2.1 Perspectiva do Produto:** o sistema é novo? Substitui o processo manual atual? Integra com algum serviço externo (e-mail, SMS, WhatsApp)? Onde será usado (consultórios, recepção, internet)?
- **2.2 Funções do Produto:** lista das principais funções do sistema (ex.: agendamento, confirmação e lembretes, gestão de agendas, relatórios de ocupação, controle de acesso)
- **2.3 Atores e Características dos Usuários:** para cada perfil de usuário, descreva responsabilidades, nível de familiaridade com tecnologia e restrições de uso
- **2.4 Restrições:** regulatórias (LGPD, dados sensíveis de saúde), de funcionamento (horário da clínica, 5 consultórios) e de acessibilidade (pacientes idosos)
- **2.5 Suposições e Dependências:** hipóteses adotadas (ex.: pacientes possuem e-mail ou celular) e dependências externas (ex.: provedor de envio de mensagens)

> **Atenção:** os atores identificados na seção 2.3 devem ser **os mesmos** que aparecem nos casos de uso e no diagrama.

---

### SEÇÃO 3: Requisitos Específicos

#### 3.1 Requisitos Funcionais (RF)

- Especifique **no mínimo 8 requisitos funcionais**
- Siga **exatamente a estrutura do exemplo RF01** do template:
  - **ID** · **Função** · **Descrição** · **Entradas** · **Fonte** · **Saídas** · **Destino** · **Ação** · **Requisitos** · **Pré-condições** · **Pós-condições** · **Efeitos colaterais** · **Requisitos Relacionados**
- Os RF devem, em conjunto, resolver **todos os problemas** identificados no estudo de caso:
  - conflitos de agendamento
  - pacientes que não comparecem (falta de lembretes)
  - dificuldade em gerar relatórios de ocupação
  - impossibilidade de agendar fora do horário comercial
  - falta de controle de acesso e confidencialidade
- Numere em sequência: RF01, RF02, RF03...

#### 3.2 Requisitos Não Funcionais (RNF)

- Especifique **no mínimo 6 requisitos não funcionais**, de **pelo menos 4 categorias diferentes**
- Siga **exatamente a estrutura do exemplo RNF01** do template:
  - **ID** · **Categoria** · **Descrição** · **Condições de medição** · **Métrica de verificação** · **Requisitos Relacionados**
- Todo RNF deve ser **mensurável**. Evite termos vagos como "rápido", "fácil" ou "seguro" sem um número ou critério que permita testar
- Devem aparecer obrigatoriamente RNF de:
  - **Segurança/Privacidade** (dados sensíveis de saúde e LGPD)
  - **Usabilidade/Acessibilidade** (pacientes idosos; profissionais sem treinamento extenso)
  - **Desempenho** (considere cerca de 200 agendamentos por semana)
- Numere em sequência: RNF01, RNF02, RNF03...

---

### SEÇÃO 4: Casos de Uso

#### Descrição dos Casos de Uso

- Descreva **no mínimo 3 casos de uso** principais do sistema
- **"Agendar Consulta" é obrigatório**
- Siga **exatamente a estrutura do exemplo UC01** do template:
  - **ID** · **Descrição** · **Atores** · **Pré-condições** · **Pós-condições (sucesso)** · **Requisitos Relacionados**
  - **Fluxo Principal** (passos numerados)
  - **Fluxos Alternativos** (A1, A2...)
  - **Fluxos de Exceção** (E1, E2...)
- Cada caso de uso deve indicar quais **RF e RNF** ele atende

#### Diagrama de Caso de Uso

- Elabore **um diagrama UML** com a visão geral do sistema
- O diagrama deve conter:
  - a **fronteira do sistema** (retângulo com o nome do sistema)
  - **todos os atores** descritos na seção 2.3
  - **todos os casos de uso** do sistema, e não apenas os 3 descritos
  - relacionamentos **«include»** e **«extend»** quando fizerem sentido
- Os nomes dos casos de uso no diagrama devem ser **idênticos** aos usados nas descrições
- Insira o diagrama como figura, **logo abaixo das descrições**, com legenda (`\caption`)
- Ferramentas sugeridas: Astah, draw.io, PlantUML ou TikZ (no próprio LaTeX)

---

## ERROS COMUNS — EVITE!

| Erro | Exemplo | Como corrigir |
|:-----|:--------|:--------------|
| Requisito não testável | "O sistema deve ser rápido" | "A agenda do dia deve carregar em até 2 segundos" |
| RF descrevendo como fazer, e não o que fazer | "O sistema deve usar MySQL" | Isso é restrição/RNF, não RF |
| Caso de uso que é só um passo | "Clicar em Salvar" | Caso de uso é um **objetivo do ator**: "Agendar Consulta" |
| Nome genérico de caso de uso | "CRUD Paciente" | "Cadastrar Paciente" ou "Manter Paciente", conforme a descrição |
| Login ligado por «include» a todos os casos de uso | Agendar Consulta «include» Fazer Login | Autenticação é **pré-condição** |
| Seta na associação ator–caso de uso | Ator → Caso de uso | Associação é uma **linha simples** |
| Direção errada do «extend» | Base → Extensão | A seta vai **da extensão para o caso de uso base** |
| Nomes diferentes entre texto e diagrama | "Marcar Consulta" × "Agendar Consulta" | Use exatamente o mesmo nome |
| Exemplos da imobiliária esquecidos no documento | RF01: Cadastrar Imóvel | Remova todos os exemplos do template |


---

## INSTRUÇÕES IMPORTANTES

- ✓ O trabalho deve ser entregue **individualmente**
- ✓ **Formato:** arquivo **.pdf** gerado no Overleaf **e** o projeto LaTeX em **.zip** (*Menu → Download → Source*)
- ✓ Utilize **obrigatoriamente o [template](SRS.zip)** fornecido
- ✓ **Não é permitido** copiar trabalhos de colegas
- ✓ **Utilize a terminologia apropriada** da engenharia de software
- ✓ Este documento será **continuado nas próximas etapas**: guarde o projeto do Overleaf

---

## REFERÊNCIAS

- **Sommerville, I.** (2018). *Engenharia de Software*. 10ª edição. Pearson.
- **Pressman, R. S.** (2010). *Engenharia de Software: uma abordagem profissional*. McGraw-Hill.
- **IEEE Std 830-1998.** *IEEE Recommended Practice for Software Requirements Specifications*.
- **Guedes, G. T. A.** (2018). *UML 2: uma abordagem prática*. 3ª edição. Novatec.

---
