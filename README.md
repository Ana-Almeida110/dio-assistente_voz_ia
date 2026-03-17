# 🎙️ Assistente de Voz Simples com Whisper e gTTS

Este projeto demonstra um assistente de voz básico construído no Google Colab, utilizando:

- **Whisper** → reconhecimento de fala (Speech-to-Text)
- **gTTS** → síntese de fala (Text-to-Speech)

O assistente é capaz de gravar áudio, transcrever comandos e responder com áudio, além de executar ações simples como abrir o Google Agenda ou o YouTube.

---

## 🚀 Funcionalidades

- 🎤 **Gravação de Áudio**
  Captura áudio diretamente do microfone do usuário no navegador.

- 🧠 **Reconhecimento de Fala (Speech-to-Text)**
  Transcreve o áudio usando o modelo `small` do Whisper, com suporte para português.

- 🔎 **Reconhecimento de Comandos**
  Identifica comandos como:
  - `"agenda"`
  - `"youtube"`
 
- 🔊 **Síntese de Fala (Text-to-Speech)**
  Gera respostas em áudio utilizando **gTTS**.

- 🌐 **Ações Simples**
  Abre URLs no navegador, como:
  - Google Calendar
  - Youtube

 ---

 ## ⚙ Como funciona

 O notebook está dividido nas seguintes etapas:
 1. **Definição do Idioma**
    Define o idioma principal como português:
    ```python
    language = 'pt'
    
 2. **Gravação de Áudio**
    Um trecho em JavaScript grava o áudio do microfone e salva como `audio_gravado.wav`
    
 3. **Instalação de Dependências**
    Instala bibliotecas necessárias  
    !pip install git+https://github.com/openai/whisper.git  
    !sudo apt update && sudo apt install ffmpeg
    
 4. **Carregamento do Modelo Whisper**
    modelo = whisper.load_model('small')
 
 5. **Transcrição e Reconhecimento de Comandos**
    resultado = modelo.transcribe("audio_gravado.wav")
    
 6. **Resposta e Ação**
    O assistente pode:
    - Exibir mensagens na tela
    - Gerar links clicáveis
    - Produzir resposta em áudio
   
---

## ▶ Como Usar no Google Colab
1. Abra o Notebook
2. Execute as células em ordem:
   - Definição do idioma: language = 'pt'
   - Gravação de áudio: execute a função "gravar_audio()" > permita acesso ao microfone
   - Instalação do Whisper e FFmpeg
   - Carregamento do modelo
   - Transcrição
   - Reconhecimento de comandos e ações
   - Instalação do gTTS
   - Geração de resposta em áudio
  
---

## 📦 Dependências Principais
- openai-whisper → reconhecimento de fala
- gTTS → síntese de fala
- ffmpeg → processamento de áudio
- IPython.display → exibição de áudio e execução de JavaScript

---

## 💬Exemplo de Interação
Ao executar a gravação, o assistente dirá:
--"Pode falar..."

Você pode dizer:
- "Agenda"
- "Youtube"

O assistente irá:
1. Transcrever sua fala
2. Identificar o comando
3. Executar a ação correspondente
4. Responder com áudio

---

Projeto criado por: Ana Paula de Almeida Coiado

