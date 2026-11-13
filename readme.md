# 🎹🎸 CifraStudio Pro — Dicionário Interativo de Acordes

<p align="center">
  <a href="https://denis-tek.github.io/cifra-studio/" target="_blank">
    <img src="https://img.shields.io/badge/▶_Executar_Aplicação-GitHub_Pages-6366f1?style=for-the-badge&logo=github" alt="Executar no GitHub Pages">
  </a>
  <a href="https://github.com/Denis-Tek/cifra-studio" target="_blank">
    <img src="https://img.shields.io/badge/Repositório-Denis--Tek%2Fcifra--studio-1e293b?style=for-the-badge&logo=git" alt="Repositório GitHub">
  </a>
</p>

O **CifraStudio Pro** é uma aplicação web interativa para músicos, estudantes e professores de música que permite visualizar, construir e ouvir qualquer acorde musical (cifra) simultaneamente em um **Teclado/Piano de 3 oitavas** e no braço do **Violão/Guitarra**, com suporte completo a extensões harmônicas de MPB, Bossa Nova e Jazz.

---

## 🖼️ Preview da Aplicação

<p align="center">
  <img src="./imagem.png" alt="Preview do CifraStudio Pro" width="100%" style="border-radius: 12px; border: 1px solid #334155;" />
</p>

---

## 🚀 Demonstração Online (GitHub Pages)

Acesse e utilize o aplicativo diretamente no navegador, sem necessidade de instalação:

- 🔗 **Link direto do projeto:** [https://denis-tek.github.io/cifra-studio/](https://denis-tek.github.io/cifra-studio/)

---

## ✨ Funcionalidades Principais

* 🧠 **Reconhecimento Inteligente de Cifras (Parser Universal):**
  * Digite qualquer cifra diretamente no campo de busca (ex: `C7M(9)`, `F#m7(11)`, `G7(13)`, `E7(#9)`, `A6(9)`, `D7(9/13)`, `C6/7`, `Bm7(b5)`, `G/B`) e veja a montagem instantânea.
* ⚡ **Construtor Modular de Cifras Compostas & Tensões:**
  * Botões dedicados (`+6`, `+7`, `+7M`, `+b9`, `+9`, `+#9`, `+11`, `+#11`, `+b13`, `+13`, `b5`, `#5`) para combinar tensões livremente sobre qualquer acorde base.
  * Suporte completo a **Inversões de Baixo (*Slash Chords*)**, como `/G`, `/B`, `/F#`.
* 🎹 **Teclado / Piano Interativo de 3 Oitavas (SVG):**
  * Posicionamento real das extensões (`9ª`, `11ª`, `13ª`) na oitava superior.
  * Destaque visual por cores: **Tônica/Baixo** (Âmbar), **Tríade/7ª** (Azul) e **Extensões** (Roxo), além de clique individual em cada tecla para ouvir sua nota.
* 🎸 **Violão / Guitarra com Shapes de MPB, Bossa Nova, Jazz e CAGED:**
  * Diagrama interativo com indicação de pestanas, cordas soltas (`O`), cordas abafadas (`✕`), numeração dos dedos (`1` a `4`) e seletor de múltiplas regiões no braço.
* 🔊 **Motor de Áudio Realista (Web Audio API):**
  * Síntese sonora em tempo real com timbres distintos para **Piano** e **Violão** (modo acorde em bloco/batida ou dedilhado/arpejo).
  * Detecção automática do instrumento selecionado na visualização (`Ambos`, `🎹 Teclado` ou `🎸 Violão`).
* 📚 **Painel de Nomenclatura e Teoria Harmônica:**
  * Exibe o nome completo do acorde por extenso em português, a **Fórmula Intervalar** exata e cartões interativos para cada grau da estrutura do acorde.
* ☀️/🌙 **Alternância de Tema (Claro / Escuro):**
  * Botão dedicado no cabeçalho (`☀️` / `🌙`) que permite alternar instantaneamente entre o tema **Dark Studio** (padrão) e o tema **Claro (Light Mode)**, adaptando automaticamente o contraste dos textos, painéis e do braço do violão para excelente legibilidade em qualquer ambiente.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5 & SVG Dinâmico** — Renderização vetorial responsiva do piano de 36 teclas e do braço do violão.
* **Tailwind CSS** — Estilização moderna com suporte dinâmico aos temas Dark (`🌙`) e Light (`☀️`).
* **JavaScript (Vanilla ES6+)** — Motor de teoria musical, parser de expressões harmônicas e gerador algorítmico de *voicings*.
* **Web Audio API** — Síntese polifônica nativa no navegador (sem dependência de amostras externas de áudio).

---

## 💻 Como Executar Localmente

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

1. **Pesquisa Rápida:** Digite uma cifra na caixa de texto ou escolha a **1. Nota Fundamental** e a **2. Qualidade**.
2. **Adicione Extensões:** Use a seção **3. Construtor de Cifras Compostas** para ativar/desativar tensões como `9`, `11`, `#11` ou `13`.
3. **Explore o Braço do Violão:** Clique nas setas `<` e `>` acima do diagrama do violão para alternar entre diferentes posições no braço.
4. **Ouça o Som:** Clique em **Tocar Acorde**, **Dedilhar** ou diretamente sobre qualquer tecla do piano, corda do violão ou cartão de nota.
5. **Personalize a Visualização:** Escolha entre exibir `Ambos`, apenas `🎹 Teclado` ou apenas `🎸 Violão`, e clique no ícone `☀️` / `🌙` no canto superior direito para alternar entre o **Tema Claro** e o **Tema Escuro**.

---

## 👤 Autor

Desenvolvido por **Denis** — [GitHub (@Denis-Tek)](https://github.com/Denis-Tek)  
Projeto disponível em: [https://github.com/Denis-Tek/cifra-studio](https://github.com/Denis-Tek/cifra-studio)