# InfinitePay Splash Prototype

Protótipo HTML/CSS/JS da splash screen dinâmica do app InfinitePay.

## Como usar

1. Abra `index.html` em um servidor local (necessário para carregar os assets)
2. Ou acesse via GitHub Pages

### Rodar localmente

```bash
# Python
python -m http.server 8080

# Node.js
npx serve
```

Acesse: http://localhost:8080

## Funcionalidades

- 🎲 **Sorteio aleatório** entre 3 produtos (PIX, Link, Loja)
- 🎬 **Animação de ícone** a 60fps (sequência de WebP)
- ✨ **Transição Rive** com animação de entrada/saída
- ⚙️ **Painel de configurações** (clique no ⚙️):
  - Tamanho do ícone (60-200px)
  - Tempo de leitura
  - Tempo de loading
  - Escolher produto específico

## Estrutura

```
├── index.html          # Protótipo principal
└── assets/
    ├── fonts/          # Fonte CeraPro
    ├── products/       # Frames das animações
    │   ├── pix/
    │   ├── link/
    │   └── loja/
    └── rive/           # Arquivo Rive da transição
```

## Fluxo da Splash

1. Sorteia produto aleatório
2. Exibe ícone animado + texto
3. Após tempo de leitura → Rive ENTER (1º trigger)
4. Após tempo de loading → Rive EXIT (2º trigger)
5. Transição completa
