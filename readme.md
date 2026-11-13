# 🎹🎸 CifraStudio Pro — Dicionário e Visualizador Interativo de Acordes

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Acessar%20Aplicação-6366f1?style=for-the-badge&logo=github)](https://denis-tek.github.io/cifra-studio/)
[![Repositório](https://img.shields.io/badge/GitHub-Denis--Tek%2Fcifra--studio-181717?style=for-the-badge&logo=github)](https://github.com/Denis-Tek/cifra-studio)
[![Licença](https://img.shields.io/badge/Licença-MIT-10b981?style=for-the-badge)](https://github.com/Denis-Tek/cifra-studio)

O **CifraStudio Pro** é uma aplicação web interativa para visualização, estudo teórico e audição em tempo real de acordes musicais no **Teclado/Piano** e no **Violão/Guitarra**. 

Projetado para músicos, estudantes e professores, o aplicativo conta com um motor harmônico avançado capaz de interpretar desde tríades básicas e acordes abertos tradicionais até acordes complexos de Jazz, Bossa Nova e MPB (incluindo 9ª, 11ª, 13ª, tensões alteradas, cifras compostas e *slash chords* / inversões de baixo).

---

## 📸 Preview da Aplicação

![Preview do CifraStudio Pro](./imagem.png)

---

## 🚀 Demonstração Online (GitHub Pages)

Você pode executar o aplicativo diretamente no navegador, sem necessidade de instalação:

- 🔗 **Executar o CifraStudio Pro:** [https://denis-tek.github.io/cifra-studio/](https://denis-tek.github.io/cifra-studio/)

---

## ✨ Funcionalidades Principais

- **🔍 Reconhecimento Inteligente de Cifras (Parser Universal):**
  - Digite qualquer cifra diretamente no campo de busca (ex: `D`, `D7`, `C7M(9)`, `F#m7(11)`, `G7(13)`, `A6(9)`, `E7(#9/b13)`, `C6/7`, `D/F#`, `G/B`).
  - Diferenciação inteligente entre barras de tensões compostas (`6/7`, `7(9/13)`) e barras de inversão de baixo (`/F#`, `/B`).
- **⚡ Construtor Modular de Cifras Compostas:**
  - Combine livremente intervalos extras (`+6`, `+7`, `+7M`, `+b9`, `+9`, `+#9`, `+11`, `+#11`, `+b13`, `+13`, `b5`, `#5`) sobre qualquer acorde e veja a cifra e os diagramas se atualizarem instantaneamente.
- **🎹 Teclado / Piano Interativo de 3 Oitavas (`C3` a `B5`):**
  - *Voicing* profissional aberto com a nota fundamental/baixo na região grave e a tríade, sétima e extensões (9ª, 11ª, 13ª) distribuídas na oitava superior real.
  - Diferenciação visual por cores: **Âmbar** (Tônica/Baixo), **Azul** (Tríade e 7ª) e **Roxo** (Extensões e Tensões), exibindo o nome da nota e o grau intervalar em cada tecla.
  - Teclas clicáveis individualmente para ouvir cada nota isolada.
- **🎸 Violão / Guitarra com Múltiplas Posições e Validação Biomecânica:**
  - Diagrama completo no braço do instrumento com indicação de cordas soltas (`O`), cordas abafadas (`✕`), pestanas, numeração dos dedos (`1`, `2`, `3`, `4`) e notas/graus resultantes abaixo de cada corda.
  - Seletor de posições (`< Posição 1/N >`) que prioriza acordes abertos clássicos na 1ª posição e permite explorar shapes do sistema CAGED (nas cordas 6, 5 e 4) e *voicings* de MPB/Bossa Nova.
  - Cordas interativas com animação de vibração ao tocar.
- **🔊 Síntese de Áudio Realista (Web Audio API):**
  - Timbres sintetizados separadamente para **Piano Elétrico/Acústico** e **Violão** sem depender de arquivos externos.
  - Modos de reprodução para **Tocar Acorde (Em Bloco / Batida)** e **Dedilhar (Arpejo)**, adaptando-se automaticamente ao instrumento selecionado no modo de visualização (`Ambos`, `🎹 Teclado` ou `🎸 Violão`).
- **📚 Painel de Nomenclatura Harmônica e Graus:**
  - Exibe o nome completo do acorde por extenso em português, sua **Fórmula Intervalar** (ex: `1 - 3 - 5 - 7 - 9 - 13`) e cartões interativos para cada grau do acorde.
- **☀️ / 🌙 Tema Claro e Tema Escuro (Light / Dark Mode):**
  - Alternância instantânea no topo da interface entre o modo escuro de estúdio (`🌙`) e o modo claro de alto contraste (`☀️`), adaptando também as cores do diagrama do violão e dos textos.

---

## 🎸 Como os Acordes de Violão são Gerados?

Diferente de dicionários estáticos limitados, o **CifraStudio Pro** utiliza um motor harmônico em **3 camadas** para listar as posições de violão (`Posição 1/N`):

1. **Camada 1 — Dicionário Prioritário de Acordes Abertos (`OPEN_CHORD_SHAPES`):**
   - Garante que acordes fundamentais do violão popular (`C`, `C7`, `C7M`, `D`, `D7`, `Dm`, `D7M`, `E`, `E7`, `Em`, `G`, `G7`, `A`, `A7`, `Am`, `B7`, `F7M`, `D/F#`, `G/B`, etc.) exibam como **Posição 1** exatamente a digitação aberta clássica de 3 ou 4 dedos nas primeiras casas.
2. **Camada 2 — Matrizes Transponíveis CAGED & MPB/Jazz (`MOVABLE_SHAPES`):**
   - Transpõe matematicamente formas com pestana e *voicings* clássicos de MPB, Bossa Nova e Jazz tomando como referência a tônica na **6ª corda (Mi)**, **5ª corda (Lá)** e **4ª corda (Ré)**.
3. **Camada 3 — Gerador Algorítmico com Validação Biomecânica (`assignPlayableFingers`):**
   - Quando o usuário cria uma cifra composta customizada no construtor modular, o algoritmo busca ao longo do braço *voicings* compactos (máximo de 4 dedos, abertura máxima de 4 casas) e aplica um validador biomecânico que garante que cada nota possua um dedo exclusivo (`1`, `2`, `3`, `4`) ou uma pestana fisicamente executável (sem cordas soltas ou casas anteriores bloqueando a pestana), descartando posições impossíveis de tocar.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 & SVG Dinâmico:** Renderização vetorial responsiva e interativa para o piano de 3 oitavas e para o braço do violão.
- **Tailwind CSS (via CDN):** Estilização moderna, responsiva e suporte nativo a *Dark Mode* / *Light Mode*.
- **JavaScript (Vanilla ES6+):** Motor de teoria musical, parser de expressões regulares para cifras, gerador de *voicings* e validação biomecânica.
- **Web Audio API:** Síntese sonora polifônica em tempo real diretamente no navegador.

---

## 💻 Como Executar Localmente

Como o projeto foi construído em arquitetura *Single-File* (sem dependências de build ou Node.js), executá-lo localmente é extremamente simples:

1. Clone este repositório:
   ```bash
   git clone https://github.com/Denis-Tek/cifra-studio.git
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd cifra-studio
   ```
3. Abra o arquivo `index.html` diretamente em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).

---

## 📖 Guia Rápido de Uso

1. **Pesquisa Rápida:** Digite uma cifra no campo principal (como `D7`, `Cm7(9)` ou `G7(13)`) ou clique nos botões de exemplos rápidos.
2. **Construção Passo a Passo:**
   - Escolha a **1. Nota Fundamental** (alterne entre `#` e `b` se desejar).
   - Filtre e selecione a **2. Qualidade & Extensões Prontas** pelas abas (*Tríades*, *6ª e 7ª*, *Nonas*, *11ª*, *13ª*).
   - Adicione ou remova intervalos no painel **3. Construtor de Cifras Compostas**.
   - Se desejar uma inversão, selecione a **4. Nota no Baixo (Slash Chord)**.
3. **Exploração Visual e Sonora:**
   - Alterne a visualização no topo entre **Ambos**, **🎹 Teclado** ou **🎸 Violão**.
   - Use os botões **Tocar Acorde** e **Dedilhar** ou clique diretamente nas teclas do piano, nas cordas do violão ou nos cartões de graus harmônicos.
   - Clique no botão **☀️ / 🌙** no canto superior direito para alternar entre o tema claro e o tema escuro.

---

## 👤 Autor

Desenvolvido por **Denis** ([@Denis-Tek](https://github.com/Denis-Tek)).

- 📦 **Repositório no GitHub:** [https://github.com/Denis-Tek/cifra-studio](https://github.com/Denis-Tek/cifra-studio)
- 🌐 **Aplicação Online (GitHub Pages):** [https://denis-tek.github.io/cifra-studio/](https://denis-tek.github.io/cifra-studio/)