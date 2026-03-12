# Sudoku

![Platform](https://img.shields.io/badge/platform-web-blue.svg)
![HTML](https://img.shields.io/badge/HTML5-single--file-orange.svg)
![CSS](https://img.shields.io/badge/CSS3-embedded-blue.svg)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-yellow.svg)
![Status](https://img.shields.io/badge/status-ready%20for%20GitHub-brightgreen.svg)

A browser-based Sudoku game built as a single HTML file, with puzzle generation, multiple difficulty levels, notes, hints, timer, and keyboard support.

Jogo de Sudoku para navegador construído em um unico arquivo HTML, com geracao de tabuleiros, multiplas dificuldades, notas, dicas, timer e suporte a teclado.

[English](#english) | [Português](#portugues)

## English

### Overview

This project is a complete Sudoku game implemented in a single `index.html` file. It includes interface, styles, puzzle generation logic, solving logic, game state management, and player interactions without requiring a build step or backend.

### Highlights

- Single-file application using HTML, CSS, and vanilla JavaScript
- Procedural Sudoku generation with uniqueness validation
- Four difficulty levels: Easy, Medium, Hard, and Expert
- Mistake counter with game over after 3 errors
- Timer and victory statistics modal
- Notes mode, hints, erase, undo, and new game actions
- Keyboard navigation and numeric input support
- Responsive layout for desktop and mobile screens
- Confetti animation on victory

### How to Run

#### Requirements

- A modern web browser
- Internet access for the Google Fonts dependency

#### Local usage

1. Download or clone the project.
2. Open `index.html` in your browser.
3. Select a difficulty level and start playing.

No installation, package manager, or server is required.

### Gameplay Features

#### Core gameplay

- 9x9 Sudoku board with visual separation between 3x3 boxes
- Generated puzzles based on clue count by difficulty
- Validation against the hidden solution
- Automatic win detection
- Loss state after reaching the maximum mistake limit

#### Player tools

- Number pad with remaining count per digit
- Notes mode for pencil marks inside cells
- Hint action that fills one unresolved cell
- Erase action for clearing editable cells
- Undo action using a history stack
- New game button to regenerate a puzzle in the current difficulty

#### Feedback and UX

- Highlight for selected cell, same row, same column, and same 3x3 box
- Highlight for repeated selected numbers
- Error styling for incorrect entries
- Pop animation when a correct number is placed
- Victory modal with time, difficulty, and mistake stats
- Game over modal after 3 mistakes

### Keyboard Controls

- `1` to `9`: place a number in the selected cell
- Arrow keys: move the current selection
- `Backspace` or `Delete`: erase the selected editable cell
- `N`: toggle notes mode
- `Ctrl+Z`: undo last action

### Technical Details

The game engine is fully embedded in `index.html` and is organized around these responsibilities:

- board generation through recursive backtracking
- uniqueness checking through a bounded solution counter
- state management for solution, puzzle, player board, notes, history, timer, and mistakes
- dynamic rendering of the board and numpad
- event-driven interactions for mouse, touch, and keyboard usage

### Project Structure

```text
Sudoku/
`- index.html
```

### External Dependency

The project uses one external asset:

- Google Fonts (`Inter`)

### Current Limitations

- No persistence in `localStorage`
- No save/resume feature between sessions
- No offline packaging for external font dependency
- Entire project is concentrated in a single HTML file, which can make long-term maintenance harder

### Roadmap

Suggested future improvements:

- Add local auto-save
- Add theme switching
- Add difficulty statistics and session history
- Add touch-specific quality-of-life improvements
- Split the code into separate HTML, CSS, and JS files if the project grows

### License

This project is licensed under the MIT License. See the `LICENSE` file for the full text.

## Portugues

### Visao geral

Este projeto e um jogo completo de Sudoku implementado em um unico arquivo `index.html`. Ele reune interface, estilos, logica de geracao de tabuleiro, logica de resolucao, gerenciamento de estado e interacoes do jogador sem exigir build ou backend.

### Destaques

- Aplicacao single-file com HTML, CSS e JavaScript vanilla
- Geracao procedural de Sudoku com validacao de unicidade
- Quatro niveis de dificuldade: Facil, Medio, Dificil e Expert
- Contador de erros com game over apos 3 falhas
- Timer e modal de vitoria com estatisticas
- Acoes de notas, dica, apagar, desfazer e novo jogo
- Suporte a navegacao por teclado e entrada numerica
- Layout responsivo para desktop e mobile
- Animacao de confete ao vencer

### Como executar

#### Requisitos

- Navegador moderno
- Acesso a internet para carregar a fonte do Google Fonts

#### Uso local

1. Baixe ou clone o projeto.
2. Abra `index.html` no navegador.
3. Escolha a dificuldade e começe a jogar.

Nao ha necessidade de instalacao, gerenciador de pacotes ou servidor.

### Recursos de jogo

#### Jogabilidade principal

- Tabuleiro 9x9 com separacao visual entre os blocos 3x3
- Geracao de partidas com quantidade de pistas por dificuldade
- Validacao das jogadas contra a solucao interna
- Deteccao automatica de vitoria
- Estado de derrota ao atingir o limite maximo de erros

#### Ferramentas do jogador

- Numpad com contador de quantas ocorrencias faltam para cada numero
- Modo de notas para rascunhos dentro das celulas
- Acao de dica que revela uma celula ainda nao resolvida
- Acao de apagar para limpar celulas editaveis
- Acao de desfazer com base em historico
- Botao de novo jogo para regenerar um tabuleiro na dificuldade atual

#### Feedback e experiencia

- Destaque da celula selecionada, linha, coluna e bloco 3x3 correspondentes
- Destaque para numeros iguais ao numero selecionado
- Estilo visual de erro para entradas incorretas
- Animacao ao inserir um numero correto
- Modal de vitoria com tempo, dificuldade e total de erros
- Modal de game over apos 3 erros

### Controles de teclado

- `1` a `9`: insere um numero na celula selecionada
- Setas direcionais: movem a selecao atual
- `Backspace` ou `Delete`: apagam a celula editavel selecionada
- `N`: alterna o modo de notas
- `Ctrl+Z`: desfaz a ultima acao

### Detalhes tecnicos

O motor do jogo esta totalmente embutido em `index.html` e se organiza em torno destas responsabilidades:

- geracao do tabuleiro por backtracking recursivo
- verificacao de unicidade por contagem limitada de solucoes
- gerenciamento de estado para solucao, puzzle, tabuleiro do jogador, notas, historico, timer e erros
- renderizacao dinamica do tabuleiro e do numpad
- interacoes orientadas a eventos para mouse, toque e teclado

### Estrutura do projeto

```text
Sudoku/
`- index.html
```

### Dependencia externa

O projeto usa um unico asset externo:

- Google Fonts (`Inter`)

### Limitacoes atuais

- Nao ha persistencia em `localStorage`
- Nao existe funcionalidade de salvar e continuar depois
- Nao ha empacotamento offline da dependencia externa de fonte
- Todo o projeto esta concentrado em um unico arquivo HTML, o que pode dificultar manutencao futura

### Roadmap

Melhorias sugeridas para proximas versoes:

- Adicionar auto-save local
- Adicionar troca de tema
- Adicionar estatisticas por dificuldade e historico de partidas
- Adicionar melhorias especificas para toque em dispositivos moveis
- Separar HTML, CSS e JS em arquivos dedicados se o projeto crescer

### Licenca

Este projeto esta licenciado sob a licenca MIT. Consulte o arquivo `LICENSE` para o texto completo.

