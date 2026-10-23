# ATIVIDADE 02 — ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE (SRS)
## Sistema de Agendamento de Consultório Médico — Etapa 2: Casos de Uso

**Disciplina:** Engenharia de Software — TADS · IFPR Campus Cascavel
**Professor:** Nelson Bellincanta Filho

---

## INTRODUÇÃO

Na **Etapa 1** você elaborou as seções de Introdução, Descrição Geral e Requisitos Específicos (RF e RNF) do SRS do Sistema de Agendamento de Consultório Médico. Agora esses requisitos vão ganhar forma de **interação**: quem usa o sistema, com qual objetivo e o que acontece, passo a passo, quando tudo dá certo e quando algo dá errado.

Os **casos de uso** descrevem o comportamento do sistema do ponto de vista dos atores. Eles servem de base para o desenvolvimento das telas, para os testes de aceitação e, mais adiante, para a Matriz de Rastreabilidade. Por isso, cada caso de uso precisa ser **coerente com os atores da seção 2.3** e com os **RF e RNF da seção 3**.

Nesta **Etapa 2** você deve elaborar as seguintes subseções do SRS:

| Subseção | Conteúdo |
|:--------:|:---------|
| 4.1 | Descrição dos Casos de Uso — ID, descrição, atores, pré e pós-condições, requisitos relacionados e fluxos |
| 4.2 | Diagrama de Caso de Uso — visão geral UML do sistema |

As seções de Backlog do Produto, Matriz de Rastreabilidade, Glossário e Anexos ficam para as próximas etapas.

---

## MATERIAL DE APOIO

- **Estudo de caso:** `atv01.md` (Sistema de Agendamento de Consultório Médico)
- **Seu SRS da Etapa 1:** continue no **mesmo projeto do Overleaf**; os atores (2.3), as funções (2.2) e os requisitos (3.1 e 3.2) são o ponto de partida desta etapa
- **Template LaTeX do SRS:** [📥 Baixar o template SRS.zip](SRS.zip) (consulte se precisar recuperar o exemplo original)
- **Eclipse Papyrus:** ferramenta obrigatória para o diagrama de caso de uso ([eclipse.org/papyrus](https://eclipse.dev/papyrus/))

No template, a seção 4 traz o exemplo **UC01: Cadastrar Imóvel** (subseção 4.1) e o seu diagrama `UC01.png` (subseção 4.2), ambos do **sistema de imobiliária**. Eles servem **apenas como modelo de estrutura**. Substitua todo o conteúdo pelo sistema da clínica.

---

## O QUE DEVE SER FEITO

### Antes de começar — revisão da Etapa 1

- Releia a seção **2.3 Atores e Características dos Usuários**: a lista de atores ali deve ser a **mesma** usada nos casos de uso e no diagrama. Se perceber que falta algum ator (ex.: um sistema externo de envio de mensagens), **corrija a 2.3 primeiro**
- Releia a seção **2.2 Funções do Produto**: cada função listada deve corresponder a **pelo menos um caso de uso** no diagrama
- Confira a numeração dos RF e RNF: você vai referenciá-los em cada caso de uso
- Remova o texto em itálico de *Orientação* da seção 4 depois de preenchê-la

---

### SUBSEÇÃO 4.1: Descrição dos Casos de Uso

No template, o exemplo ocupa a subseção 4.1. Renomeie-a para **Descrição dos Casos de Uso** e coloque cada caso de uso como uma `\subsubsection` dentro dela (4.1.1, 4.1.2, ...). Os títulos dos fluxos passam a ser `\paragraph`:

```latex
\subsection{Descrição dos Casos de Uso}

\subsubsection{UC01: Agendar Consulta}
\begin{itemize}[leftmargin=*]
  \item \textbf{ID:} UC-001
  ...
\end{itemize}

\paragraph{Fluxo Principal}
\begin{enumerate}
  ...
\end{enumerate}

\paragraph{Fluxos Alternativos}
...

\paragraph{Fluxos de Exceção}
...

\subsubsection{UC02: ...}
```

#### Quantidade e casos de uso obrigatórios

- Descreva **no mínimo 5 casos de uso**
- São **obrigatórios**:
  - **Agendar Consulta**
  - **Cancelar Consulta** (ou **Remarcar Consulta**)
  - **Gerar Relatório de Ocupação**
- Os demais são de sua escolha (ex.: confirmar presença, enviar lembrete, gerenciar agenda do profissional, cadastrar paciente, gerenciar usuários e permissões)
- Em conjunto, os casos de uso descritos devem envolver **pelo menos 3 atores diferentes**

#### Estrutura de cada caso de uso

Siga **exatamente a estrutura do exemplo UC01** do template:

- **ID** · **Descrição** · **Atores** · **Pré-condições** · **Pós-condições (sucesso)** · **Requisitos Relacionados**
- **Fluxo Principal** (passos numerados)
- **Fluxos Alternativos** (A1, A2...)
- **Fluxos de Exceção** (E1, E2...)

#### Regras para os fluxos

- **Fluxo Principal:** descreve o cenário de sucesso, do início ao fim, **sem desvios** ("se... senão" não entra aqui). Alterne as ações do **ator** e as respostas do **sistema**, numerando cada passo. O último passo indica que o caso de uso **encerra com sucesso**
- **Fluxos Alternativos:** no mínimo **2 por caso de uso**. Cada um indica **em qual passo** do fluxo principal começa (ex.: *"(passo 4)"*) e **como termina** (retorna a um passo ou encerra o caso de uso)
- **Fluxos de Exceção:** no mínimo **3 por caso de uso**. Indique a condição de erro, a resposta do sistema e a mensagem exibida ao usuário
- Considere as **regras do estudo de caso**: conflito de horários, horário de funcionamento da clínica, 5 consultórios, lembretes para evitar faltas, acesso restrito a dados de saúde (LGPD), pacientes idosos
- O nível de detalhe técnico do exemplo (rotas da API, códigos HTTP) é **opcional**. O essencial é a **interação entre ator e sistema**

#### Rastreabilidade

- Em **Requisitos Relacionados**, cite os **RF e RNF** da seção 3 que o caso de uso atende, usando os mesmos IDs (RF01, RNF03...)
- Todo requisito citado deve **existir** na seção 3
- Todo **RF** da seção 3 deve aparecer em **pelo menos um** caso de uso descrito ou no diagrama. Isso será cobrado na Matriz de Rastreabilidade
- Atualize também o campo **Requisitos Relacionados** dos seus RF e RNF para apontar para os UCs correspondentes (ex.: `RF02 · UC-001`)

---

### SUBSEÇÃO 4.2: Diagrama de Caso de Uso

- Elabore **um único diagrama UML** com a **visão geral do sistema**
- O diagrama deve conter:
  - a **fronteira do sistema** (retângulo com o nome **Sistema de Agendamento de Consultório Médico**)
  - **todos os atores** descritos na seção 2.3, incluindo atores que sejam **sistemas externos** (posicione-os, preferencialmente, do lado direito)
  - **todos os casos de uso** do sistema, e não apenas os 5 descritos na 4.1
  - **pelo menos um «include» e um «extend»**, usados corretamente
  - **generalização de atores**, se fizer sentido no seu sistema (ex.: atores que compartilham casos de uso)
- Os nomes dos casos de uso no diagrama devem ser **idênticos** aos usados nas descrições. Para os casos de uso descritos, inclua também o ID (ex.: *UC01 Agendar Consulta*), como no exemplo do template
- Todo caso de uso deve estar ligado a **pelo menos um ator**, exceto os que participam apenas como **«include»** ou **«extend»**
- No template, **substitua a imagem `UC01.png`** pelo seu diagrama e ajuste a legenda:
  - `\caption{Diagrama de Caso de Uso --- Sistema de Agendamento de Consultório Médico}`
- O diagrama deve ser feito **obrigatoriamente no Eclipse Papyrus** (*File → New → Papyrus Project → UML*, com um *Use Case Diagram*)
- Para inserir no SRS, exporte o diagrama como imagem (*botão direito no diagrama → File → Export → Export All Diagrams*, ou *Export As Image*) em **PNG** ou **SVG/PDF**, com boa resolução para que o texto fique legível no documento
- Guarde o projeto Papyrus: ele também será **entregue** (veja as Instruções Importantes)

---

## ERROS COMUNS — EVITE!

| Erro | Exemplo | Como corrigir |
|:-----|:--------|:--------------|
| Caso de uso que é só um passo | "Clicar em Salvar" | Caso de uso é um **objetivo do ator**: "Agendar Consulta" |
| Nome genérico de caso de uso | "CRUD Paciente" | "Cadastrar Paciente" ou "Manter Paciente", conforme a descrição |
| Desvio dentro do fluxo principal | "5. Se o horário estiver ocupado, o sistema..." | O fluxo principal é o caminho feliz; o desvio vira **fluxo alternativo ou de exceção** |
| Fluxo alternativo sem origem nem fim | "A1: Paciente escolhe outro médico" | Indique o **passo de origem** e se **retorna** a um passo ou **encerra** |
| Pós-condição repetindo o último passo | "Sistema exibe mensagem de sucesso" | Pós-condição é o **estado do sistema** após o caso de uso: "Consulta registrada com status Agendada" |
| Login ligado por «include» a todos os casos de uso | Agendar Consulta «include» Fazer Login | Autenticação é **pré-condição** |
| «include» para comportamento opcional | Agendar Consulta «include» Enviar Lembrete por WhatsApp | Se é opcional ou condicional, é **«extend»** |
| Direção errada do «extend» | Base → Extensão | A seta vai **da extensão para o caso de uso base** |
| Seta na associação ator–caso de uso | Ator → Caso de uso | Associação é uma **linha simples** |
| "Sistema" como ator | Ator "Sistema" ligado a "Enviar Lembrete" | O próprio sistema **não é ator**; um serviço externo (ex.: provedor de SMS) pode ser |
| Ator do diagrama ausente na seção 2.3 | Ator "Enfermeira" só no diagrama | Atores do diagrama, das descrições e da 2.3 devem ser **os mesmos** |
| Requisito relacionado inexistente | "Requisitos Relacionados: RF12" (só existem 9 RF) | Cite apenas IDs que **existem** na seção 3 |
| Nomes diferentes entre texto e diagrama | "Marcar Consulta" × "Agendar Consulta" | Use exatamente o mesmo nome |
| Exemplos da imobiliária esquecidos no documento | UC01: Cadastrar Imóvel · figura `UC01.png` original | Remova todos os exemplos do template |

---

## INSTRUÇÕES IMPORTANTES

- ✓ O trabalho deve ser entregue **individualmente**
- ✓ **Formato da entrega:**
  - o **SRS em .pdf** gerado no Overleaf, **contendo os diagramas**
  - o **projeto LaTeX em .zip** (*Menu → Download → Source*)
  - o **projeto Papyrus em .zip**, com os arquivos `.di`, `.notation` e `.uml` (*File → Export → General → Archive File*, ou compacte a pasta do projeto no workspace do Eclipse)
- ✓ Os diagramas devem ser feitos **obrigatoriamente no Eclipse Papyrus**. Diagramas feitos em outras ferramentas não serão aceitos
- ✓ Entregue o **SRS completo** (seções 1 a 4), já com as correções da Etapa 1
- ✓ Utilize **obrigatoriamente o [template](SRS.zip)** fornecido, no mesmo projeto da Etapa 1
- ✓ **Não é permitido** copiar trabalhos de colegas
- ✓ **Utilize a terminologia apropriada** da engenharia de software
- ✓ Este documento será **continuado nas próximas etapas**: guarde o projeto do Overleaf

---

## REFERÊNCIAS

- **Sommerville, I.** (2018). *Engenharia de Software*. 10ª edição. Pearson.
- **Pressman, R. S.** (2010). *Engenharia de Software: uma abordagem profissional*. McGraw-Hill.
- **IEEE Std 830-1998.** *IEEE Recommended Practice for Software Requirements Specifications*.
- **Guedes, G. T. A.** (2018). *UML 2: uma abordagem prática*. 3ª edição. Novatec.
- **Cockburn, A.** (2005). *Escrevendo casos de uso eficazes*. Bookman.

---
