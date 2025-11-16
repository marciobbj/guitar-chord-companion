## Chord Finder

Chord Finder é uma ferramenta de teoria musical "tudo-em-um" para guitarristas.

Este aplicativo é totalmente autossuficiente e funciona em um único arquivo .html, combinando um metrônomo preciso com utilitários avançados de acordes, escalas e harmonia.

## Funcionalidades

O aplicativo é dividido em um cabeçalho global (Metrônomo) e três abas principais.

### Metrônomo (Global)

O cabeçalho do aplicativo é um metrônomo funcional que persiste em todas as abas:

BPM Control: O BPM (Batidas Por Minuto) pode ser ajustado de 30 a 240 usando um "knob" (botão circular) interativo.

Controles: Botão "START/STOP" e um "blip" visual que pisca no tempo.

Áudio Preciso: Utiliza a Web Audio API para agendar os "ticks" de áudio, garantindo precisão rítmica que o setInterval não pode oferecer.

Batida Acentuada: O "tick" da batida "1" é mais alto e o "blip" visual fica azul, ajudando a manter a contagem do compasso (4/4).

### Aba CHORD ID (Identificador de Acordes)

Esta aba permite que você identifique qualquer acorde tocado no braço da guitarra.

Braço Interativo: Clique em qualquer traste ou corda solta para adicionar notas.

Identificação Inteligente: A lógica analisa as notas e identifica o acorde. Funciona com:

Díades: (ex: Power Chords).

Tríades: (Maior, Menor, Aumentado, etc.).

Tétrades e Extensões: (ex: m7, Maj9, 7(b5), etc.).

"Shell Voicings": (ex: C, E, A# é identificado como C7).

Detecção de Baixo (Inversões): Identifica corretamente acordes com inversão, mostrando o baixo na nota mais grave (ex: G Major / B).

Lógica de Ambiguidade: Prioriza a interpretação onde a tônica é o baixo (ex: as notas "G" e "D" são identificadas como G5 e não D(Perfect 4th) se G for a nota mais grave).

### 3. Aba: SCALES (Escalas)

Um visualizador de escalas para estudar padrões no braço da guitarra.

Seleção: Escolha uma Tônica (ex: "C#") e um Tipo de Escala (ex: "Minor Pentatonic").

Mapa de Notas: O braço da guitarra ilumina todas as notas pertencentes àquela escala.

Destaque da Tônica: Todas as tônicas (notas "C#") são destacadas em azul para fácil visualização dos pontos de ancoragem.

### Aba: HARMONY (Campos Harmônicos)

Uma ferramenta poderosa para analisar a estrutura harmônica e encontrar inversões de acordes.

Seleção de Harmonia: Escolha um Tom (ex: "A") e um Tipo de Harmonia (ex: "Minor (Harmonic)").

Lista de Acordes: O aplicativo gera a lista completa de acordes (tétrades) para aquele campo harmônico (ex: i-maj7, ii-m7(b5), V7, etc.).

Analisador de Intervalos: Ao clicar em um acorde da lista (ex: "V7"):

O braço da guitarra ilumina todas as notas desse acorde em todo o braço.

As notas são rotuladas com seus intervalos (ex: R, 3, 5, b7).

Guia de Inversões: Uma seção de ajuda explica como usar esse "mapa de intervalos" para construir qualquer inversão do acorde (Estado Fundamental, 1ª, 2ª ou 3ª inversão).

### Tecnologias Utilizadas

HTML5

Tailwind CSS (para design e responsividade)

JavaScript (Puro/Vanilla) (para toda a lógica de teoria musical, abas e interatividade)

Web Audio API (para o metrônomo)

### Como Executar

Este projeto é um único arquivo .html. Basta salvar o arquivo chord_identifier.html e abri-lo em qualquer navegador moderno.
