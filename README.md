# 🌍✨ Web Tradutor

Um tradutor web simples, direto e funcional — feito com **HTML, CSS e JavaScript puro** — com um toque especial: **tradução por voz** 🎤.

> Projeto com cara de prática real: você fala, ele transcreve e traduz. Sem complicação. 💙

## 🚀 Visão geral

A ideia do projeto é ser fácil de usar e fácil de entender:

- ✍️ você digita um texto em português;
- 🌐 escolhe o idioma de destino;
- 🔄 traduz com API externa;
- 🎙️ ou fala no microfone para transcrever e traduzir automaticamente.

É aquele tipo de projeto que ensina bem os fundamentos e já entrega valor na prática.

## 💪 Pontos fortes (destaques reais)

- **Integração com API de tradução**: usa a API MyMemory via `fetch`, permitindo tradução dinâmica sem precisar de backend próprio. ⚡
- **Tradução por voz**: integração com `webkitSpeechRecognition` para captar fala em `pt-BR`, transcrever e acionar a tradução em sequência. 🎤➡️🌍
- **Experiência de uso objetiva**: interface limpa e com fluxo curto (digitar/falar → traduzir → visualizar resultado). ✅
- **Código enxuto e didático**: ótimo para estudar DOM, requisições HTTP e eventos de voz em JavaScript. 📚
- **Base pronta para evolução**: fácil de expandir com histórico, leitura por voz, novos idiomas e melhorias de UX. 🛠️

## 🗂️ Estrutura de arquivos

```text
web-tradutor/
├── index.html      # Estrutura da interface
├── styles.css      # Estilos visuais
├── scripts.js      # Lógica de tradução e voz
├── img/            # Ícones e imagem de fundo
└── README.md       # Documentação do projeto
```

## ▶️ Como executar

Você pode abrir o `index.html` direto no navegador.

Mas, para melhor compatibilidade (principalmente com microfone e políticas do browser), o ideal é rodar com servidor local:

```bash
python3 -m http.server 5500
```

Depois abra:

```text
http://localhost:5500
```

## 🧩 Funcionalidades atuais

- Tradução de texto de **pt-BR** para:
  - 🇺🇸 Inglês (`en`)
  - 🇪🇸 Espanhol (`es`)
  - 🇫🇷 Francês (`fr`)
  - 🇩🇪 Alemão (`de`)
  - 🇮🇹 Italiano (`it`)
  - 🇯🇵 Japonês (`ja`)
- Entrada por voz com transcrição em `pt-BR`.
- Exibição imediata da tradução na interface.

## ⚙️ Fluxo técnico

1. Usuário digita texto (ou usa o microfone).
2. O JavaScript monta a URL da API (`q` + `langpair`).
3. A aplicação faz a requisição com `fetch`.
4. A resposta JSON é convertida.
5. O texto traduzido é exibido no bloco de resultado.
6. No modo voz, a transcrição já alimenta o campo e dispara a tradução.

## ⚠️ Observações importantes

- `webkitSpeechRecognition` pode variar de suporte entre navegadores (normalmente funciona melhor no Chrome).
- Ainda não há tratamento robusto de erro para falhas de rede/API.
- O idioma de origem está fixo em `pt-BR`.

## 🔮 Melhorias sugeridas

- Adicionar tratamento de erro com mensagens amigáveis.
- Usar `encodeURIComponent` no texto antes de montar a URL da API.
- Ajustar `inputTexto.textContent` para `inputTexto.value` no fluxo de voz (`textarea`).
- Exibir estado de carregamento durante a tradução.
- Permitir seleção do idioma de origem.
- Criar testes básicos de UI e integração.

## 🧰 Tecnologias

- HTML5
- CSS3
- JavaScript (ES6+)
- API MyMemory Translation
- Web Speech API (`webkitSpeechRecognition`)

---

## ❤️ Consideração final

Esse projeto é pequeno no tamanho, mas grande no potencial.
Com poucos arquivos, ele já demonstra integração com API, manipulação de DOM e reconhecimento de voz — um combo muito bom para portfólio e aprendizado prático.
