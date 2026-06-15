# 🚗🍺 Posso Dirigir?

Calculadora web, bem-humorada e **mobile-first**, que estima se a pessoa já pode dirigir depois de beber — ou se é melhor chamar o Uber.

> ⚠️ **Estimativa aproximada.** Não substitui bom senso nem bafômetro. No Brasil vale a **Lei Seca: tolerância zero**. Na dúvida, **não dirija.**

![status](https://img.shields.io/badge/feito%20com-%E2%99%A5-red) ![mobile](https://img.shields.io/badge/mobile-first-blue)

## ✨ O que faz

- Coleta os dados da pessoa: sexo, idade, peso e altura
- Lista suspensa de bebidas (cerveja, vinho, caipirinha, vodka, whisky, gin, tequila, saquê e mais)
- Tamanhos/doses criativos por bebida (latinha, long neck, taça, dose, shot, dose dupla…) com quantidade ajustável
- Permite adicionar **várias bebidas** numa mesma sessão
- Horário do último gole ("acabei agora" ou um horário específico)
- Resultado com **mensagem descontraída** dizendo se pode ou não dirigir
- Estima o **horário em que a pessoa estará liberada** (+ margem de segurança)
- Gera **lembrete no Google Agenda** e arquivo **`.ics`** para baixar no celular
- **Disclaimer** claro de que é um cálculo estimado

## 🧮 Como o cálculo funciona

Usa a fórmula de **Widmark** combinada com o cálculo de **água corporal total (Watson)**, que aproveita sexo, idade, peso e altura:

```
BAC (g/L) = 0,806 × álcool(g) / água_corporal(L) − β × tempo(h)
álcool(g) = volume(ml) × (teor% / 100) × 0,789
```

- `β = 0,15 g/L por hora` (taxa média de eliminação)
- Limite aplicado: **Lei Seca (tolerância zero)**
- Margem de segurança de **+30 min** no horário de liberação

> Os valores são médias populacionais. Metabolismo, alimentação, remédios e sono mudam o resultado real.

## 🚀 Publicar no GitHub Pages

1. Crie um repositório no GitHub (ex.: `posso-dirigir`) e suba os arquivos:

```bash
cd "posso-dirigir"
git init
git add .
git commit -m "feat: calculadora Posso Dirigir"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/posso-dirigir.git
git push -u origin main
```

2. No GitHub: **Settings → Pages → Source: `main` / `root`** e salve.
3. Em alguns minutos o site fica no ar em `https://SEU_USUARIO.github.io/posso-dirigir/`.

É um site 100% estático (HTML/CSS/JS em um único `index.html`) — não precisa de build nem servidor.

## 📁 Estrutura

```
posso-dirigir/
├── index.html   # tudo aqui: HTML + CSS + JS
├── README.md
├── LICENSE
└── .gitignore
```

## 📄 Licença

MIT — veja [LICENSE](LICENSE).

---

Developed with ♥ by **Wanderson Castro**
