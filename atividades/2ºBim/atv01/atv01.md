# ESTUDO DE CASO: SISTEMA DE AGENDAMENTO DE CONSULTÓRIO MÉDICO

---

## INTRODUÇÃO

Uma clínica médica com 5 consultórios e 15 profissionais de saúde (médicos e enfermeiras) identificou a necessidade de modernizar seu sistema de agendamento de consultas. Atualmente, todas as marcações são realizadas manualmente por telefone ou presencialmente, o que causa diversos problemas operacionais.

Como analista de requisitos, você foi contratado para levantar os requisitos funcionais e não funcionais para este novo sistema. Este documento apresenta o cenário, e você deverá identificar e classificar os requisitos.

---

## CONTEXTO DA ORGANIZAÇÃO

### Informações Gerais

- **Clínica multiespecialidades** com funcionamento de segunda a sexta, das 07:00 às 19:00
- **5 consultórios equipados** com computadores
- **Aproximadamente 200 agendamentos** por semana
- **Clientes com idades variadas** (alguns idosos com dificuldade com tecnologia)
- **Armazenamento de dados sensíveis** (informações médicas e pessoais dos pacientes)

### Problemas Identificados com Sistema Atual

- Frequentes **conflitos de agendamento** (pacientes marcados no mesmo horário)
- Elevada **taxa de pacientes que não comparecem** (falta de lembretes)
- **Dificuldade em gerar relatórios** de ocupação dos consultórios
- **Impossibilidade de pacientes marcarem consultas** fora do horário comercial
- **Falta de controle de acesso** e confidencialidade dos dados

### Expectativas dos Stakeholders

#### Gerência da Clínica

- Aumentar eficiência operacional
- Reduzir custos com pessoal administrativo
- Melhorar a experiência do paciente

#### Pacientes

- Agendar consultas de forma fácil e rápida
- Receber confirmações e lembretes de consultas
- Acessar histórico de agendamentos anteriores

#### Profissionais de Saúde

- Visualizar agenda de forma clara e organizada
- Consultar histórico do paciente antes da consulta
- Sistema fácil de usar, sem treinamento extenso

---

## QUESTÕES 

Baseando-se no contexto apresentado acima, responda às seguintes questões:

---

### QUESTÃO 1: Identificar Requisitos Funcionais

**Instruções:**
- Identifique pelo menos **8 requisitos funcionais** para o sistema de agendamento
- Para cada requisito, descreva: **o que o sistema DEVE FAZER**
- **Dica:** Comece seus requisitos com verbos de ação (permitir, registrar, gerar, validar, etc.)

| Nº | Requisito Funcional | Descrição (O que o sistema faz?)|
|:--:|:------------------:|:--------------------------------:|
| 1  |                    |                                  |
| 2  |                    |                                  |
| 3  |                    |                                  |
| 4  |                    |                                  |
| 5  |                    |                                  |
| 6  |                    |                                  |
| 7  |                    |                                  |
| 8  |                    |                                  |

---

### QUESTÃO 2: Identificar Requisitos Não Funcionais

**Instruções:**
- Identifique pelo menos **6 requisitos não funcionais**
- Para cada requisito, indique a **categoria** (desempenho, segurança, usabilidade, confiabilidade, etc.)
- Descreva: **COMO o sistema deve se comportar**

| Nº | Categoria | Requisito | Descrição (Como?) |
|:--:|:---------:|:---------:|:-----------------:|
| 1  |           |           |                   |
| 2  |           |           |                   |
| 3  |           |           |                   |
| 4  |           |           |                   |
| 5  |           |           |                   |
| 6  |           |           |                   |

---

### QUESTÃO 3: Análise Comparativa

**Instruções:**
- Escolha **um requisito funcional** e **um não funcional** que estejam relacionados
- Explique **como o requisito não funcional INFLUENCIA** a implementação do requisito funcional
- Descreva **pelo menos 2 exemplos de impacto**
- Responda em **um parágrafo de no mínimo 150 palavras**

**Resposta:**

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

---

### QUESTÃO 4: Resolução de Conflitos de Requisitos

Um dos requisitos não funcionais é que o sistema deve responder a qualquer consulta em menos de 2 segundos. Porém, você identificou que o sistema precisa armazenar informações médicas detalhadas de aproximadamente 20.000 pacientes com histórico de 5 anos de consultas.

**Instruções:**
- Qual é o **conflito potencial** entre esses requisitos?
- Sugira **3 soluções possíveis** para resolver esse conflito
- Para cada solução, explique as **vantagens e desvantagens**

**Resposta:**

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

_______________________________________________________________________________

---

### QUESTÃO 5: Classificação Segundo Sommerville

O autor Ian Sommerville classifica os requisitos não funcionais em **3 categorias**:

1. **Requisitos de Produto:** especificam ou restringem o comportamento do software durante a execução (dependabilidade, usabilidade, segurança, eficiência)

2. **Requisitos Organizacionais:** relacionados aos processos, políticas e procedimentos da organização do cliente e do desenvolvedor (desenvolvimento, operacionais, ambientais)

3. **Requisitos Externos:** derivam de fatores externos ao sistema e seu processo de desenvolvimento (legais, éticos, reguladores)

**Instruções:**
- Classifique cada um dos **6 requisitos não funcionais** que você identificou na Questão 2 segundo a classificação de Sommerville
- **Justifique a classificação** para cada um

**Resposta:**

| Nº | Requisito | Classificação | Justificativa |
|:--:|:---------:|:-------------:|:-------------:|
| 1  |           |               |               |
| 2  |           |               |               |
| 3  |           |               |               |
| 4  |           |               |               |
| 5  |           |               |               |
| 6  |           |               |               |

---


## INSTRUÇÕES IMPORTANTES

- ✓ O trabalho deve ser entregue **individualmente**
- ✓ **Data de entrega:** 01/06
- ✓ **Formato:** arquivo em .pdf
- ✓ **Não é permitido** copiar respostas de colegas
- ✓ **Respostas devem ser claras** e bem estruturadas
- ✓ **Utilize a terminologia apropriada** da engenharia de software
- ✓ **Referencie** os conceitos vistos em aula

---

## DICAS PARA OS ALUNOS

### Para Requisitos Funcionais:

Utilize verbos de ação como:
- Permitir
- Registrar
- Gerar
- Validar
- Consultar
- Enviar
- Calcular
- Armazenar
- Autorizar
- Notificar

### Para Requisitos Não Funcionais:

Categorias comuns:
- **Desempenho:** velocidade, tempo de resposta
- **Segurança:** proteção de dados, autenticação
- **Usabilidade:** facilidade de uso, interface
- **Confiabilidade:** disponibilidade, recuperação de falhas
- **Manutenibilidade:** facilidade de manutenção
- **Portabilidade:** funcionamento em diferentes plataformas
- **Escalabilidade:** capacidade de crescimento

---

## REFERÊNCIAS

- **Sommerville, I.** (2018). *Engenharia de Software*. 10ª edição. Pearson.
- **Pressman, R. S.** (2010). *Engenharia de Software: uma abordagem profissional*. McGraw-Hill.

---
