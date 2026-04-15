![visitors](https://visitor-badge.laobi.icu/badge?page_id=ArvoreDosSaberes.Curso_Livre_InsurMinds_Inteligencia_Artificial_em_Seguros)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC_BY--SA_4.0-blue.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
![Language: Portuguese](https://img.shields.io/badge/Language-Portuguese-brightgreen.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Prática-green)
![Status](https://img.shields.io/badge/Status-Educa%C3%A7%C3%A3o-brightgreen)
![Repository Size](https://img.shields.io/github/repo-size/ArvoreDosSaberes/Curso_Livre_InsurMinds_Inteligencia_Artificial_em_Seguros)
![Last Commit](https://img.shields.io/github/last-commit/ArvoreDosSaberes/Curso_Livre_InsurMinds_Inteligencia_Artificial_em_Seguros)

<!-- Animated Header -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1a56db,100:10b981&height=220&section=header&text=InsurMinds%20-%20Aula%2003&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Intera%C3%A7%C3%A3o%20com%20IA%20Generativa%20e%20Prompt%20Engineering&descSize=18&descAlignY=55&descColor=94a3b8" width="100%" alt="InsurMinds Aula 03 Header"/>
</p>

## Resumo

Terceira aula do programa **InsurMinds**, focada em **interação com IA generativa** e **prompt engineering**. O instrutor apresenta os principais insights do **Stanford AI Index 2026**, discute os fundamentos dos **LLMs (Large Language Models)**, o **mecanismo de atenção**, técnicas avançadas de **prompt engineering** (zero-shot, one-shot, few-shot, chain-of-thought), e os diferentes **tipos de raciocínio** que as LLMs podem executar. A aula inclui uma sessão prática com **desafios obrigatórios** envolvendo análise de textos desconhecidos, identificação de equipamentos defeituosos em planilhas, e criação de conteúdo jornalístico sobre os Três Porquinhos usando múltiplas LLMs.

| Informação | Detalhe |
| --- | --- |
| **Título** | InsurMinds - Agentes Inteligentes com IA Generativa |
| **Instrutor** | Celso Azevedo (I2A2) |
| **Canal** | I2A2 (YouTube) |
| **Data de Publicação** | 2026-04-14 |
| **Duração** | 2h06min23s |
| **URL** | [Assistir no YouTube](https://www.youtube.com/watch?v=xtVntP496IQ) |
| **Transcrição** | Whisper medium (GPU CUDA) |

---

## Índice de Tópicos

1. [Abertura e Recapitulação](#1-abertura-e-recapitulação)
2. [Stanford AI Index 2026 - Principais Insights](#2-stanford-ai-index-2026---principais-insights)
3. [Fundamentos dos LLMs](#3-fundamentos-dos-llms)
4. [Mecanismo de Atenção](#4-mecanismo-de-atenção)
5. [Prompt Engineering - Técnicas Fundamentais](#5-prompt-engineering---técnicas-fundamentais)
6. [Frameworks de Prompt](#6-frameworks-de-prompt)
7. [Boas Práticas em Prompt Engineering](#7-boas-práticas-em-prompt-engineering)
8. [Tipos de Raciocínio em LLMs](#8-tipos-de-raciocínio-em-llms)
9. [Técnicas de Raciocínio](#9-técnicas-de-raciocínio)
10. [Segurança e Considerações Importantes](#10-segurança-e-considerações-importantes)
11. [Estrutura de um Agente de IA](#11-estrutura-de-um-agente-de-ia)
12. [Desafios Práticos - Atividades Obrigatórias](#12-desafios-práticos---atividades-obrigatórias)
13. [Orientações de Entrega](#13-orientações-de-entrega)

---

## 1. Abertura e Recapitulação

A aula inicia com boas-vindas e esclarecimento sobre o foco do curso: enquanto originalmente planejado para incluir IA preditiva no início, o programa foi reestruturado para focar primeiro em **IA generativa**. O certificado intermediário será emitido ao final desta fase, antes de avançar para aspectos técnicos de construção de código.

**Recapitulação da aula anterior:**
- Definição de inteligência artificial: conjunto de técnicas/algoritmos que imitam capacidade humana de agir/tomar decisões
- Hierarquia: IA > Machine Learning > Deep Learning > IA Generativa/LLMs
- Tipos de aprendizado: supervisionado, não supervisionado, por reforço

## 2. Stanford AI Index 2026 - Principais Insights

O instrutor apresenta 15 principais conclusões do relatório Stanford AI Index 2026:

| Conclusão | Impacto |
| --- | --- |
| **Infraestrutura Industrial** | Quem tem infraestrutura para rodar modelos domina o jogo |
| **Investimento de US$ 0.5 trilhão** | Volume massivo investido em data centers |
| **Dependência de Taiwan** | Maioria dos chips produzidos por empresa taiwanesa |
| **Paridade EUA-China** | Vantagem americana em desempenho reduzida a <3% |
| **Modelos Caixa-Preta** | 80-95% dos principais modelos sem transparência de treinamento |
| **Paradoxo da Inteligência** | Resolvem tarefas de nível doutorado mas falham em regras básicas |
| **Agentes no Mundo Digital** | ~100% sucesso digital, limitado em interações físicas |
| **Esgotamento de Dados** | Em 6 anos esgotaremos todo texto humano produzido |
| **Consumo Energético** | Inferência consome 29.6 GW (equivalente à rede elétrica da Suíça) |
| **Adoção Acelerada** | 53% de adoção em 3 anos (mais rápido que PCs/internet) |
| **Monetização Desafio** | Uso gratuito massivo, poucos pagantes |
| **Produtividade Real** | Ganhos em tarefas estruturadas, humano necessário em decisões complexas |
| **Mercado de Trabalho** | Substituição de posições junior, risco de formação de seniors |
| **Otimismo Especialistas vs Público** | 73% especialistas otimistas vs 23% público geral |
| **Gap Regulatório** | Excesso em algumas áreas, falhas graves em outras |

**Ferramenta recomendada:** NotebookLM para análise de textos, resumos, apresentações, podcasts e mapas mentais.

## 3. Fundamentos dos LLMs

**LLMs (Large Language Models)** são modelos treinados com vasta quantidade de texto e informações, praticamente toda a informação produzida pela humanidade.

**Timeline relevante:**
- **2012:** Revolução Deep Learning com redes neurais profundas
- **2017:** Paper "Attention Is All You Need" (Google) - mecanismo de atenção
- **2018 em diante:** Evolução dos Transformers e LLMs
- **2020+:** Expansão para multimodal (texto, imagem, áudio, vídeo)

## 4. Mecanismo de Atenção

O **mecanismo de atenção** é a técnica fundamental que possibilitou a existência dos LLMs:

**Definição simplificada:** Capacidade de identificar quais elementos são mais importantes em um texto.

**Exemplo:** "A capital da França é Paris"
- Mais importante: "França" (contexto de país)
- Segundo: "capital" (relação)
- Terceiro: "Paris" (resposta)

O mecanismo permite recortar elementos relevantes em textos simples ou complexos com milhares de palavras.

## 5. Prompt Engineering - Técnicas Fundamentais

### Zero-Shot Prompting
- Instrução direta sem exemplos
- Funciona para tarefas simples

### One-Shot Prompting  
- Um exemplo de como a resposta deve ser
- Útil para tarefas com pouca variação

### Few-Shot Prompting
- Múltiplos exemplos
- Adequado para tarefas complexas com padrões específicos

### Chain-of-Thought
- Solicita explicação passo a passo do raciocínio
- Melhora qualidade das respostas em tarefas complexas

**Exemplo prático de prompt estruturado:**
```
Você recebeu um texto. Sua tarefa deve ser realizada em dois passos:
1. Resuma o texto em uma frase concisa
2. Traduza o resumo para o espanhol
Garanta que a essência seja mantida. Omita "passo 1" e "passo 2".
```

## 6. Frameworks de Prompt

### PACE (Papel, Ação, Contexto, Exemplo)
- **Papel:** Definir persona da LLM
- **Ação:** O que deve ser feito
- **Contexto:** Informações adicionais
- **Exemplo:** Formato da resposta

### COAST (Contexto, Objetivo, Audiência, Estilo, Tipo)
- **Contexto:** Informações necessárias
- **Objetivo:** O que a LLM deve fazer
- **Audiência:** Público-alvo
- **Estilo:** Tom emocional (neutro, enfático, etc.)
- **Tipo:** Formato da resposta

### A-utomat
- **Agir como:** Persona
- **Usuário:** Público
- **Ação:** Tarefa
- **Definição:** Formato saída
- **Modo:** Estilo/tom
- **Atípico:** Exceções
- **Tópicos:** Lista de permissões

## 7. Boas Práticas em Prompt Engineering

1. **Forneça contexto** - Dê identidade clara à LLM
2. **Enquadre positivamente** - Diga o que quer, não o que não quer
3. **Inclua exemplos** - Amostras condicionam melhor o prompt
4. **Seja específico e claro** - Exatamente o que deseja
5. **Imponha limites** - Tamanho e formato da resposta
6. **Forneça amplo contexto** - Para respostas mais relevantes
7. **Organize o prompt** - Mantenha ordem lógica
8. **Use sinônimos** - Se não funcionar, tente variações
9. **Utilize delimitadores** - Markdown, aspas, etc.
10. **Use placeholders** - `{variável}` para respostas estruturadas

## 8. Tipos de Raciocínio em LLMs

### Raciocínio Biológico
- **Dedutivo:** Premissas verdadeiras -> conclusão verdadeira
- **Indutivo:** Evidências -> conclusão provável (ex: todos os cisnes são brancos)
- **Abdutivo:** Explicação mais plausível
- **Analógico:** Comparações entre coisas
- **Causal:** Causa e efeito
- **Probabilístico:** Decisões baseadas em probabilidade
- **Formal vs Informal:** Metodológico/lógico vs intuitivo/experiencial

**Desafio do bom senso:** Varia culturalmente e temporalmente (ex: dentes podres eram sinal de riqueza na Idade Média)

## 9. Técnicas de Raciocínio

- **Prompting:** Estrutura adequada do prompt
- **In-context Learning:** Zero/one/few-shot + chain-of-thought
- **Pré-treinamento:** Padrões aprendidos no treinamento
- **Fine-tuning:** Ajuste específico do modelo
- **Mixture of Experts:** Técnica moderna de arquitetura
- **Alinhamento:** Treinamento de alinhamento com humanos
- **Agentes Autônomos:** Combinam múltiplas técnicas

**Memória em LLMs:** LLMs não têm memória inerente - memória é passada via contexto.

## 10. Segurança e Considerações Importantes

### Riscos de Segurança
- **Prompt Injection:** Injetar instruções maliciosas
- **Shadow AI:** Uso não autorizado em empresas
- **Dados Sensíveis:** Nunca transmitir informações críticas em versões gratuitas
- **Alucinações:** LLMs sempre tentam responder, mesmo sem conhecimento

### Medidas de Proteção
- **Anonimizar dados** antes de enviar para LLMs
- **Verificar resultados** sempre
- **Usar versões corporativas licenciadas** quando disponível
- **Governança:** Regras claras e punições para uso indevido
- **Validação cruzada:** Comparar respostas entre múltiplos modelos

### Bring Your Own AI (BYOAI)
- Empresas permitem uso de modelos pessoais
- Requer garantias de privacidade e segurança
- Cria desafios de compliance

## 11. Estrutura de um Agente de IA

Componentes fundamentais de um agente:
```
Agente = {
  prompt: "Instruções e contexto",
  memória: "Contexto persistente",
  modelo: "LLM (cérebro/raciocínio)",
  RAG: "Base de conhecimento enriquecida",
  ferramentas: "APIs, bancos de dados, etc."
}
```

O prompt é uma das partes mais importantes na estrutura do agente.

## 12. Desafios Práticos - Atividades Obrigatórias

**Atividade 1: Análise de Textos Desconhecidos**
- 4 textos base (Base Text 1-4) no drive do curso
- Usar pelo menos 3 LLMs diferentes (ChatGPT, Gemini, Copilot, Claude, etc.)
- Perguntas a responder:
  - Qual LLM teve melhor desempenho e por quê?
  - O que deu certo e o que não deu certo?
  - A tradução fez sentido?
  - Quem foi o autor do texto?

**Atividade 2: Identificação de Equipamento Defeituoso**
- Planilha "Defective Equipment V2026414.xlsx"
- 9 equipamentos (V1-V9) com 17 sensores cada
- Um equipamento está com defeito
- Objetivo: Identificar qual equipamento (não o sensor)
- Dica: Use validação cruzada, primeira resposta nem sempre correta

**Atividade 3: Criação Jornalística dos Três Porquinhos**
- Criar nova versão da história como notícia de jornal
- Final diferente e inovador
- Incluir 3 imagens ilustrativas no corpo do texto
- Todo conteúdo criado por LLMs (pode usar múltiplas)
- No final: documentar os prompts usados
- Formato: PDF (máximo 1MB)
- **Atividade eliminatória** - quem não entrega está fora do curso

## 13. Orientações de Entrega

### Formato de Entrega
- **Email:** challenge@i2a2.academy
- **Assunto:** "InsurMinds atividade obrigatória 1" (exato)
- **Remetente:** Mesmo email da inscrição
- **Corpo do email:** Respostas atividades 1 e 2 + nome completo
- **Anexo:** PDF da atividade 3

### Prazo
- **Data limite:** 24 de abril (domingo) até 23h59
- **Processamento:** Segunda-feira seguinte
- **Consequência:** Desistentes definitivos e irreversíveis
- **Exceções:** Apenas casos documentados (doença, falecimento)

### Recomendações
- Não deixar para última hora
- Usar recursos disponíveis (múltiplas LLMs, ajuda de colegas)
- Foco no aprendizado, não em "resposta certa"
- Esforço e justificativas são mais importantes que acertos

### Próximos Passos
- Até 27/04: Novo link do grupo WhatsApp (fase 2)
- Próxima aula: 28/04

---

## Transcrição Completa

A transcrição completa está disponível no arquivo: [`04 - InsurMinds Aula 03 - transcrição.txt`](./04%20-%20InsurMinds%20Aula%2003%20-%20transcrição.txt)

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:10b981,50:1a56db,100:0f172a&height=120&section=footer" width="100%" alt="Footer"/>
</p>

---
**Resumo:** Documentação completa da Aula 03 do InsurMinds cobrindo interação com IA generativa, Stanford AI Index 2026, fundamentos de LLMs, prompt engineering, raciocínio e desafios práticos obrigatórios.
**Data de Criação:** 2026-04-14
**Autor:** Transcrição automática (Whisper medium + GPU CUDA)
**Versão:** 1.0
**Última Atualização:** 2026-04-14
**Atualizado por:** Cascade AI
**Histórico de Alterações:**
- 2026-04-14 - Criado por Cascade AI - Versão 1.0
