![visitors](https://visitor-badge.laobi.icu/badge?page_id=carlosdelfino.InsurMinds)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC_BY--SA_4.0-blue.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
![Language: Portuguese](https://img.shields.io/badge/Language-Portuguese-brightgreen.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Prática-green)
![Status](https://img.shields.io/badge/Status-Educa%C3%A7%C3%A3o-brightgreen)

<!-- Animated Header -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1a56db,100:10b981&height=220&section=header&text=InsurMinds&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Agentes%20Inteligentes%20com%20IA%20Generativa%20Aplicados%20a%20Seguros&descSize=18&descAlignY=55&descColor=94a3b8" width="100%" alt="InsurMinds Header"/>
</p>

## Sobre o Projeto

Repositório de estudo e documentação do programa **InsurMinds** — curso de 6 meses sobre **Agentes Inteligentes com Redes Generativas** aplicados ao mercado de seguros, promovido pelo **I2A2** (Instituto de Inteligência Artificial Aplicada) com patrocínio de empresas do setor (Latin Re, entre outras).

Este repositório contém:

- **Transcrições** das aulas e webinars
- **Documentação estruturada** de cada aula com resumo, índice de tópicos e conteúdo detalhado
- **Scripts utilitários** para processamento de legendas e transcrição por IA
- **Metadados** para controle de aulas processadas

## Estrutura do Projeto

```text
InsurMinds/
├── README.md                          # Este arquivo
├── videos/                            # Vídeos baixados da playlist (não versionados)
│   ├── *.mp4                          # Arquivos de vídeo
│   ├── *.pt.srt                       # Legendas em português (quando disponíveis)
│   ├── *.description                  # Descrições dos vídeos
│   └── *.info.json                    # Metadados completos dos vídeos
├── transcrição das aulas/             # Documentação e transcrições
│   ├── metadata.json                  # Controle de aulas processadas
│   ├── 00 - A Era dos Agentes.md      # Documentação do webinar de abertura
│   ├── 00 - A Era dos Agentes - transcrição.txt
│   ├── 01 - InsurMinds Aula 01.md     # Documentação da Aula 01
│   ├── 01 - InsurMinds Aula 01 - transcrição.txt
│   ├── 02 - InsurMinds Aula 02.md     # Documentação da Aula 02
│   ├── 02 - InsurMinds Aula 02 - transcrição.txt
│   ├── 03 - InsurMinds Agentes Inteligentes com IA Generativa.md
│   └── 03 - InsurMinds Agentes IA - transcrição.txt
└── scripts/                           # Scripts utilitários
    ├── srt_to_text.py                 # Converte legendas SRT em texto limpo
    └── whisper_transcribe.py          # Transcreve vídeos sem legenda via Whisper
```

## Playlist do Curso

| # | Título | Duração | Data | Transcrição |
| --- | --- | --- | --- | --- |
| 0 | [A Era dos Agentes: Da IA Generativa à Arquitetura Cognitiva Autônoma](https://www.youtube.com/watch?v=6RAlXEp7Hwg) | 1h43m | 2026-03-11 | Legendas YouTube |
| 1 | [InsurMinds - Aula 01](https://www.youtube.com/watch?v=9wU8Xpo69ek) | 1h33m | 2026-03-25 | Legendas YouTube |
| 2 | [InsurMinds - Aula 02](https://www.youtube.com/watch?v=99iBBF8pKuA) | 2h01m | 2026-04-06 | Whisper large-v3 |
| 3 | [InsurMinds - Agentes Inteligentes com IA Generativa](https://www.youtube.com/watch?v=xtVntP496IQ) | 2h06m | 2026-04-14 | Whisper large-v3 |

## Ferramentas Utilizadas

- **yt-dlp** - Download de vídeos e legendas do YouTube
- **faster-whisper / openai-whisper** - Transcrição de áudio para texto (suporte a múltiplos modelos)
- **Python 3.8+** - Scripts de processamento

## Como Usar

### Baixar vídeos e legendas

```bash
yt-dlp --cookies-from-browser brave --js-runtimes "node:/path/to/node" \
  -f "bestvideo[height<=720]+bestaudio/best[height<=720]" \
  --write-auto-subs --sub-langs pt --convert-subs srt \
  --write-description --write-info-json \
  -o "videos/%(playlist_index)s - %(title)s [%(id)s].%(ext)s" \
  "https://www.youtube.com/playlist?list=PLW-WdJ6yAI6J1m7t9G915ILp1CLAgd7xL"
```

### Converter legendas SRT para texto

```bash
python3 scripts/srt_to_text.py videos/arquivo.pt.srt "transcrição das aulas/saida.txt"
```

### Transcrever vídeos sem legenda (via Whisper)

O script unificado `transcribe.py` suporta tanto o Whisper original quanto o faster-whisper:

```bash
# Modo simples (um arquivo)
python3 scripts/transcribe.py --file videos/arquivo.mp4 --output "transcrição das aulas/saida.txt" --simple

# Modo completo (múltiplos arquivos)
python3 scripts/transcribe.py --input videos --output "transcrição das aulas"

# Especificar modelo e tipo
python3 scripts/transcribe.py --file videos/arquivo.mp4 --model base --type faster --simple
```

**Modelos disponíveis:**
- `base` - Mais rápido, menor precisão
- `small` - Bom equilíbrio
- `medium` - Alta precisão
- `large` / `large-v3` - Máxima precisão (recomendado)

## Metadados

O arquivo `transcrição das aulas/metadata.json` controla quais aulas já foram processadas, evitando reprocessamento. Contém:

- Informações da playlist
- Status de cada aula (legendas, transcrição, documentação)
- Datas de processamento
- Configurações utilizadas

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:10b981,50:1a56db,100:0f172a&height=120&section=footer" width="100%" alt="Footer"/>
</p>

---
**Resumo:** Repositório de documentação e transcrição do programa InsurMinds — Agentes Inteligentes com IA Generativa aplicados ao mercado de seguros (I2A2).
**Data de Criação:** 2026-04-14
**Autor:** Carlos Delfino
**Versão:** 1.0
**Última Atualização:** 2026-04-14
**Atualizado por:** Cascade AI
**Histórico de Alterações:**
- 2026-04-14 - Criado por Cascade AI - Versão 1.0
