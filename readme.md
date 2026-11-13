<!-- ... existing code ... -->
## 🎸 Como os Acordes de Violão são Gerados?

Diferente de dicionários estáticos limitados, o **CifraStudio Pro** utiliza um motor harmônico em 3 camadas para listar as posições de violão (`Posição 1/N`):

1. **Camada 1 — Dicionário Prioritário de Acordes Abertos (`OPEN_CHORD_SHAPES`):** Garante que acordes fundamentais do violão popular (`C`, `D`, `D7`, `Dm`, `E`, `G`, `A`, `A7`, `Am`, `B7`, `F7M`, `D/F#`, `G/B`, etc.) exibam como **Posição 1** a forma aberta clássica de 3 ou 4 dedos nas primeiras casas.
2. **Camada 2 — Matrizes Transponíveis CAGED & MPB/Jazz (`MOVABLE_SHAPES`):** Transpõe matematicamente formas com pestana e *voicings* de MPB/Bossa Nova tomando como referência a tônica na 6ª, 5ª e 4ª cordas.
3. **Camada 3 — Gerador Algorítmico com Validação Biomecânica (`assignPlayableFingers`):** Quando o usuário monta uma cifra composta customizada no construtor modular, o algoritmo busca ao longo do braço *voicings* compactos (máximo de 4 dedos, abertura máxima de 4 casas) e valida se cada nota possui um dedo exclusivo (`1`, `2`, `3`, `4`) ou uma pestana fisicamente executável, descartando posições impossíveis de tocar.

## 🛠️ Tecnologias Utilizadas
<!-- ... existing code ... -->