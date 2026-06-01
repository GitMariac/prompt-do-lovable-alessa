# Prompt desenvolvido para o Lovable do jogo Alessa.
O prompt visa criar uma plataforma web gamificada chamada Alessa. Os códigos HTML e CSS fornecidos servem apenas como referência visual e estrutural. Não é obrigatório reproduzir a implementação técnica exatamente como apresentada. Utilize-os para compreender layout, hierarquia, espaçamento, proporções, paleta de cores, tipografia e experiência desejada. Você pode adotar outras tecnologias, componentes ou arquiteturas, desde que o resultado final mantenha a mesma identidade visual e comportamento esperado.

## Páginas da Aplicação

A aplicação deve conter as seguintes páginas:

- **Página de Ranking (ranking.html)** — exibe a classificação dos jogadores, pontuações e posições no ranking geral.
- **Página de Scores (scores.html)** — apresenta o histórico de pontuações registradas durante as partidas.
- **Página Sobre o Jogo (sobre-jogo.html)** — contém informações sobre a proposta pedagógica, objetivos e funcionamento do jogo.
- **Página de Configurações (configuracoes.html)** — permite ao usuário ajustar preferências e opções da aplicação.
- **Página de Créditos (creditos.html)** — apresenta os responsáveis pelo desenvolvimento, colaboradores e referências utilizadas.
- **Página de Privacidade (privacidade.html)** — informa as políticas de coleta, armazenamento e utilização de dados.
- **Página Sobre (sobre.html)** — descreve a aplicação, seu contexto de desenvolvimento e informações institucionais.

## Características visuais para todas as páginas

O layout deverá seguir a estrutura:

- Nav fixa no topo;
- Container principal centralizado;
- Footer fixado ao final da página.

O container principal atuará como uma região de conteúdo dinâmico, sendo reutilizado por todas as páginas da aplicação. Apenas os componentes internos desse container serão alterados conforme a funcionalidade selecionada, preservando a mesma estrutura geral de navegação e identidade visual.

- Fundo preto/cinza muito escuro
- Textura vertical sutil
- Glow suave azul/cinza
- Aspecto cyberpunk/minimalista

 O navegador padrão top-nav segue a estrutura:

```
  <nav>
    
    <img src="assets/img/avatar.png" alt="logo" class="logo" />

    <h1 class="nav-title">Alessa</h1>

    <ul class="nav-actions">
        <li><button>🏆</button></li>
        <li><button>⭐</button></li>
        <li><button>📊</button></li>
        <li><button>⚙️</button></li>
        <li><button>⏻</button></li>
    </ul>
  </nav>

```

CSS navbar

```css
/* NAV */
  nav {
    height: 80px;
    background: #1f1f1f;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px;
    border-bottom: 1px solid #333;
  }

  /* LOGO */
  .logo{
    width: 80px;
    height: 80px;

    object-fit: cover;

    cursor: pointer;
    transition: transform 0.3s ease;
  }

  .logo:hover {
    transform: scale(1.1);
  }

  .nav-title {
    font-size: 24px;
    font-weight: bold;
    align-items: center;
    justify-content: center;
    font-family: 'Verdana';
  }

  .nav-sobre {
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
    transition: color 0.3s ease;
    font-family: Verdana;
  }

  .nav-sobre a{
    text-decoration: none;
    color: white;
}

.nav-sobre a:hover{
    color: red;
}

.nav-actions{
    display: flex;
    gap: 15px;

    list-style: none;
}
.nav-actions button{

    width: 50px;
    height: 50px;

    border-radius: 50%;

    border: none;

    background: rgba(50,50,50,0.7);

    color: white;

    cursor: pointer;

    transition: 0.3s;
}

```
Os ícones sugerem funções típicas de uma navegação/app dashboard:

| Ícone | Possível função |
| --- | --- |
| 🏆 | Ranking |
| ⭐ | Meus Scores |
| 📊 | Sobre o jogo |
| ⚙️ | configurações |
| ⏻ | logout/encerrar |
|  |  |

Imagem a ser colocada na Logo:

<img width="300" height="300" alt="avatar" src="https://github.com/user-attachments/assets/06d4c922-d7c0-4320-8a24-addf35952434" />

Estrutura do Footer:

```jsx
<!-- RODAPÉ -->
<footer>
  <div class="footer-content">

    <p class="assinatura">
      Projeto desenvolvido por Maria
    </p>

    <div class="footer-links">
      <a href="sobre.html">Sobre</a>
      <a href="ranking.html">Ranking</a>
      <a href="creditos.html">Créditos</a>
      <a href="privacidade.html">Política de Privacidade</a>
    </div>

    <p class="versao">
      Alessa v0.1
    </p>

  </div>
</footer>

</body>
</html>
```

CSS do Footer:

```jsx
	footer {
    width: 100%;
    height: 60px;
    padding: 15px;
    background: #1f1f1f;
    display: flex;
    align-items: center;
    justify-content: center;
    border-top: 1px solid #333;
    font-size: 0.9rem;
  }

  .footer-content{
    width: 90%;
    max-width: 1200px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
}

.footer-links{
    display: flex;
    gap: 15px;
}

.footer-links a{
    color: white;
    text-decoration: none;
    transition: 0.3s;
}

.footer-links a:hover{
    color: red;
}

  /* RESPONSIVIDADE */
  @media(max-width: 768px) {

    nav {
      padding: 0 20px;
    }

    .conteudo {
      height: 500px;
    }

  }
```

### Container principal centralizado

Região central da interface destinada à exibição do conteúdo específico de cada página. Deve manter alinhamento centralizado, dimensões responsivas e flexibilidade para acomodar diferentes tipos de componentes e informações.

```jsx
  <!-- ÁREA CENTRAL -->
  <main>

    <section class="conteudo">

      <!--
  Container principal da aplicação.

  Esta área é dinâmica e seu conteúdo varia de acordo
  com a funcionalidade acessada pelo usuário.

  Exemplos de conteúdo:
  - dashboards
  - rankings
  - tabelas
  - gráficos
  - formulários
  - jogos
  - canvas
  - iframes
  - componentes renderizados via JavaScript
-->
      <h2>Área dinâmica</h2>

    </section>

  </main>

```
CSS do container:

```jsx
  /* CONTEÚDO CENTRAL */
  main {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
  }

  /* RETÂNGULO DINÂMICO */
  .conteudo {
    width: 90%;
    max-width: 1200px;
    height: 650px;

    background: #222;
    border: 2px solid #444;
    border-radius: 16px;

    display: flex;
    align-items: center;
    justify-content: center;

    overflow: hidden;
  }
 
```

## Alessa Página Inicial
Navbar e Footer como o de todas as páginas.

O container principal deve conter:

- Mensagem de boas-vindas ao jogador;
- Área de seleção de avatares;
- Campo de entrada de texto para nome do jogador;
- Botão "Começar Jogo" para iniciar a partida.

Os elementos devem estar organizados verticalmente e centralizados na área principal da aplicação.
Segue as imagens a serem utilizadas de avatar dos jogadores (não podendo utilizar qualquer outra) podendo somente ser cortadas para melhor ajuste nas bordas ou cores de fundo

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/a38c1058-d8b1-454a-b675-8e81db809d61" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/25877873-8cf5-48b6-9403-3efaeeff335c" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/30504b33-bdf6-46fb-88fa-5a03ebc15948" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/e8467670-6e6b-422a-a735-eb73a2f47539" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/d7177663-cad6-4a04-bfcb-ec531433ea73" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/d6c8c115-9291-4cea-944d-1a7dbc1a982f" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/ff9bbba7-62a1-4d13-b131-646030e518ee" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/0ad2bcd9-8f16-4e8b-b520-4e4bd645c717" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/a5a58429-cb21-4581-9407-e887bc2ace90" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/eb655a81-53c3-428c-9565-a14c82456752" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/e688e874-2d2a-42c3-8566-ffd141838fd4" />

A paleta abaixo serve apenas como referência para elementos de destaque. A aplicação inteira deve permanecer em tema escuro.
Cores sugeridas para o projeto:

| Elemento         | Cor       |
| ---------------- | --------- |
| Fundo principal  | `#F5F7FA` |
| Cards/Containers | `#FFFFFF` |
| Cor primária     | `#2563EB` |
| Cor secundária   | `#14B8A6` |
| Destaques        | `#F59E0B` |
| Texto principal  | `#1F2937` |
| Texto secundário | `#6B7280` |


## Alessa game-area

**Estrutura da área “game-area”**

Seguindo a estrutura padrão de Nav, estrutura container principal centralizado e footer.

Dentro do Container principal a tela é dividida em duas colunas

```
main{
    display:flex;
    gap:40px;
}
```

---

**Painel esquerdo (área principal)**

- tabuleiro
- inventário
- dashboard
- mapa
- grid interativa

---

**Container principal**

```
<sectionclass="board-container">
```

**Características**

- card escuro
- bordas arredondadas
- sombra externa
- glow leve

```
.board-container{
    border-radius:30px;
    background:rgba(30,30,30,0.7);
    backdrop-filter:blur(10px);
}
```

---

**Grid de quadrados**

A parte central é uma grade regular.

**Estrutura provável**

```
<divclass="grid">
<divclass="cell"></div>
<divclass="cell"></div>
</div>
```

---

**Layout técnico**

```
.grid {
    display: grid;
    grid-template-columns: repeat(16, 1fr); /* 16 colunas */
    grid-template-rows: repeat(16, 1fr);    /* 16 linhas */
    gap: 10px;
}
```

---

**Células**

Cada quadrado possui:

- border-radius pequeno
- gradiente escuro
- sombra interna
- aparência “pressionável”

```
.cell{
    width:100%;
    aspect-ratio: 1 / 1;

    border-radius:12px;

    background:linear-gradient(
145deg,
        #2d2d2d,
        #1a1a1a
    );

    box-shadow:
inset2px2px4pxrgba(255,255,255,0.05),
inset-2px-2px4pxrgba(0,0,0,0.5);
}
```

---

**Avatar**

---

O avatar recebe efeitos de animação (Live2D, Spine, da própria biblioteca JS ou PixiJS). Imagem:

<img width="300" height="300" alt="AvatarGameArea" src="https://github.com/user-attachments/assets/fc6d5b94-61db-4269-b47d-cab7ca2fd591" />

**Características**

- parcialmente “saindo” do container
- efeito flutuante
- borda vermelha glow

```
.main-action{
    position:absolute;
    bottom:-40px;
    left:50%;

    transform:translateX(-50%);

    width:120px;
    height:120px;

    border-radius:50%;
}
```

---

**Painel direito (chat/sidebar)**

Funciona como:

- chat
- mensagens
- feed
- painel social

---

**Estrutura**

```
<asideclass="chat-panel">

<divclass="messages">

<divclass="message received"></div>

<divclass="message sent"></div>

</div>

</aside>
```

---

**Balões de mensagem**

Existem dois tipos:

- **Recebidas:** seriam as mensagens do jogo. Caso tenha escolhido a palavra certa retornar: “Muito bem! Você acertou!” (pode variar a frase com outras frases de incentivo). 

Caso contrário:

Se a palavra não estiver na rodada: Esta não é uma palavra da rodada.
Se a palavra escolhida for de grafia errada: retornar a frase! Errado! A grafia correta é (apresentar a versão correta da palavra) pois é uma (apresentar a regra referente a palavra). 

- cinza escuro
- alinhadas à esquerda

**Enviadas:** Traz o que o jogador escolheu com o ponteiro do mouse/touch

- vermelho neon
- alinhadas à direita

---

**Possível CSS**

```
.message.sent{
    background: #ff4b4b;
    align-self:flex-end;
}

.message.received{
    background: #3a3a3a;
}
```

---

**Estilo visual predominante**

---

A imagem mistura:

UI/UX modernos

- Dark UI
- Glassmorphism
- Neumorphism
- Cyberpunk minimalista
- Glow effects
- Soft shadows

---

**Arquitetura visual da página**

Visualmente a hierarquia é:

```text
HEADER
│
├── BOARD PRINCIPAL
│   ├── GRID
│   └── BOTÃO CENTRAL
│
└── CHAT PANEL
    └── MENSAGENS
```
## Estruturas sugeridas para a lógica do jogo:

```jsx
import { useMemo, useState, useCallback } from "react";
import type { Grid, PlacedWord } from "@/lib/grid";
import { lineBetween, cellsEqual } from "@/lib/grid";

type Pos = { row: number; col: number };

export type GridSelectionResult = {
  word: PlacedWord;
} | {
  word: null;
  letters: string;
};

export function WordGrid({
  grid,
  foundWords,
  onSelection,
}: {
  grid: Grid;
  foundWords: PlacedWord[];
  onSelection: (result: GridSelectionResult) => void;
}) {
  const [start, setStart] = useState<Pos | null>(null);
  const [current, setCurrent] = useState<Pos | null>(null);

  const previewLine = useMemo(() => {
    if (!start || !current) return null;
    return lineBetween(start, current);
  }, [start, current]);

  const foundCellSet = useMemo(() => {
    const s = new Set<string>();
    for (const w of foundWords) {
      for (const c of w.cells) s.add(`${c.row}:${c.col}`);
    }
    return s;
  }, [foundWords]);

  const previewSet = useMemo(() => {
    const s = new Set<string>();
    if (previewLine) for (const c of previewLine) s.add(`${c.row}:${c.col}`);
    return s;
  }, [previewLine]);

  const finish = useCallback(() => {
    if (!start || !current || !previewLine) {
      setStart(null);
      setCurrent(null);
      return;
    }
    // Find matching placed word
    const match = grid.words.find((w) => cellsEqual(w.cells, previewLine));
    if (match) {
      onSelection({ word: match });
    } else {
      const letters = previewLine.map((p) => grid.cells[p.row][p.col]).join("");
      onSelection({ word: null, letters });
    }
    setStart(null);
    setCurrent(null);
  }, [start, current, previewLine, grid, onSelection]);

  return (
    <div
      className="select-none touch-none"
      onPointerUp={finish}
      onPointerLeave={finish}
    >
      <div
        className="grid gap-1 rounded-2xl border border-border bg-card/40 p-2 sm:p-3 shadow-2xl shadow-primary/10"
        style={{ gridTemplateColumns: `repeat(${grid.size}, minmax(0, 1fr))` }}
      >
        {grid.cells.flatMap((row, r) =>
          row.map((letter, c) => {
            const key = `${r}:${c}`;
            const isFound = foundCellSet.has(key);
            const isPreview = previewSet.has(key);
            return (
              <button
                type="button"
                key={key}
                onPointerDown={(e) => {
                  e.preventDefault();
                  setStart({ row: r, col: c });
                  setCurrent({ row: r, col: c });
                }}
                onPointerEnter={() => {
                  if (start) setCurrent({ row: r, col: c });
                }}
                className={
                  "flex aspect-square items-center justify-center rounded-md text-sm sm:text-base md:text-lg lg:text-xl font-semibold transition-colors " +
                  (isFound
                    ? "bg-emerald-600/70 text-white"
                    : isPreview
                      ? "bg-primary text-primary-foreground"
                      : "bg-secondary/60 text-foreground hover:bg-secondary")
                }
              >
                {letter}
              </button>
            );
          }),
        )}
      </div>
    </div>
  );
}

```
Banco de dados das palavras

Manter EXATAMENTE COMO ESTÁ:
```jsx
// Banco de palavras: [incorreta, correta, explicação]
export type WordEntry = [string, string, string];

export const wordsDatabase: Record<string, WordEntry[]> = {
  oxitonas: [
    ["vatapa", "Vatapá", "Oxítona terminada em A"],
    ["sofa", "sofá", "Oxítona terminada em A"],
    ["gamba", "gambá", "Oxítona terminada em A"],
    ["Para", "Pará", "Oxítona terminada em A"],
    ["cafe", "café", "Oxítona terminada em E"],
    ["voce", "você", "Oxítona terminada em E"],
    ["Tiete", "Tietê", "Oxítona terminada em E"],
    ["portugues", "português", "Oxítona terminada em E seguido de S"],
    ["avo", "avó", "Oxítona terminada em O"],
    ["jilo", "jiló", "Oxítona terminada em O"],
    ["cipo", "cipó", "Oxítona terminada em O"],
    ["carijo", "carijó", "Oxítona terminada em O"],
    ["chapeu", "chapéu", "Oxítona terminada em ditongo aberto ÉU"],
    ["trofeu", "troféu", "Oxítona terminada em ditongo aberto ÉU"],
    ["papeis", "papéis", "Oxítona terminada em ditongo aberto ÉI seguido de S"],
    ["fieis", "fiéis", "Oxítona terminada em ditongo aberto ÉI seguido de S"],
    ["heroi", "herói", "Oxítona terminada em ditongo aberto ÓI"],
    ["Niteroi", "Niterói", "Oxítona terminada em ditongo aberto ÓI"],
    ["anzois", "anzóis", "Oxítona terminada em ditongo aberto ÓI seguido de S"],
    ["destroi", "destrói", "Oxítona terminada em ditongo aberto ÓI"],
    ["parabens", "parabéns", "Oxítona terminada em ENS"],
    ["armazens", "armazéns", "Oxítona terminada em ENS"],
    ["alguem", "alguém", "Oxítona terminada em EM"],
    ["mantem", "mantém", "Oxítona terminada em EM"],
    ["porem", "porém", "Oxítona terminada em EM"],
    ["tambem", "também", "Oxítona terminada em EM"],
    ["acai", "açaí", "Oxítona acentuada pela regra do hiato"],
    ["Piaui", "Piauí", "Oxítona acentuada pela regra do hiato"],
    ["jacaranda", "jacarandá", "Oxítona terminada em A"],
    ["contrafile", "contrafilé", "Oxítona terminada em E"],
  ],
  paroxitonas: [
    ["facil", "fácil", "Paroxítona terminada em L"],
    ["hifen", "hífen", "Paroxítona terminada em N"],
    ["album", "álbum", "Paroxítona terminada em UM"],
    ["cadaver", "cadáver", "Paroxítona terminada em R"],
    ["albuns", "álbuns", "Paroxítona terminada em UNS"],
    ["torax", "tórax", "Paroxítona terminada em X"],
    ["juri", "júri", "Paroxítona terminada em I"],
    ["lapis", "lápis", "Paroxítona terminada em IS"],
    ["virus", "vírus", "Paroxítona terminada em US"],
    ["biceps", "bíceps", "Paroxítona terminada em PS"],
    ["orfao", "órfão", "Paroxítona terminada em ÃO"],
    ["ima", "ímã", "Paroxítona terminada em Ã"],
    ["proton", "próton", "Paroxítona terminada em ON"],
    ["amavel", "amável", "Paroxítona terminada em L"],
    ["carater", "caráter", "Paroxítona terminada em R"],
    ["individuos", "indivíduos", "Paroxítona terminada em ditongo"],
    ["precarias", "precárias", "Paroxítona terminada em ditongo seguido de S"],
    ["serie", "série", "Paroxítona terminada em ditongo"],
    ["historia", "história", "Paroxítona terminada em ditongo"],
    ["homogenea", "homogênea", "Paroxítona terminada em ditongo"],
    ["medio", "médio", "Paroxítona terminada em ditongo"],
    ["bromelia", "bromélia", "Paroxítona terminada em ditongo"],
    ["imoveis", "imóveis", "Paroxítona terminada em ditongo seguido de S"],
    ["agua", "água", "Paroxítona terminada em ditongo"],
    ["distancia", "distância", "Paroxítona terminada em ditongo"],
    ["industria", "indústria", "Paroxítona terminada em ditongo"],
    ["radio", "rádio", "Paroxítona terminada em ditongo"],
    ["cenario", "cenário", "Paroxítona terminada em ditongo"],
    ["saude", "saúde", "Paroxítona acentuada pela regra do hiato"],
    ["incluido", "incluído", "Paroxítona acentuada pela regra do hiato"],
  ],
  proparoxitonas: [
    ["medico", "médico", "Proparoxítona (todas são acentuadas)"],
    ["lampada", "lâmpada", "Proparoxítona (todas são acentuadas)"],
    ["especifico", "específico", "Proparoxítona (todas são acentuadas)"],
    ["penultimo", "penúltimo", "Proparoxítona (todas são acentuadas)"],
    ["pagina", "página", "Proparoxítona (todas são acentuadas)"],
    ["antonimo", "antônimo", "Proparoxítona (todas são acentuadas)"],
    ["atomo", "átomo", "Proparoxítona (todas são acentuadas)"],
    ["relampago", "relâmpago", "Proparoxítona (todas são acentuadas)"],
    ["caotico", "caótico", "Proparoxítona (todas são acentuadas)"],
    ["unica", "única", "Proparoxítona (todas são acentuadas)"],
    ["politica", "política", "Proparoxítona (todas são acentuadas)"],
    ["atlantico", "atlântico", "Proparoxítona (todas são acentuadas)"],
    ["domestico", "doméstico", "Proparoxítona (todas são acentuadas)"],
    ["tecnicas", "técnicas", "Proparoxítona (todas são acentuadas)"],
    ["cerebro", "cérebro", "Proparoxítona (todas são acentuadas)"],
    ["ergometrica", "ergométrica", "Proparoxítona (todas são acentuadas)"],
    ["artifices", "artífices", "Proparoxítona (todas são acentuadas)"],
    ["ebano", "ébano", "Proparoxítona (todas são acentuadas)"],
    ["incredulo", "incrédulo", "Proparoxítona (todas são acentuadas)"],
    ["sonambulo", "sonâmbulo", "Proparoxítona (todas são acentuadas)"],
    ["valvula", "válvula", "Proparoxítona (todas são acentuadas)"],
    ["idolo", "ídolo", "Proparoxítona (todas são acentuadas)"],
    ["seculo", "século", "Proparoxítona (todas são acentuadas)"],
    ["exito", "êxito", "Proparoxítona (todas são acentuadas)"],
    ["codigos", "códigos", "Proparoxítona (todas são acentuadas)"],
    ["simbolos", "símbolos", "Proparoxítona (todas são acentuadas)"],
    ["decada", "década", "Proparoxítona (todas são acentuadas)"],
    ["esferografica", "esferográfica", "Proparoxítona (todas são acentuadas)"],
    ["interim", "ínterim", "Proparoxítona (todas são acentuadas)"],
    ["aerolito", "aerólito", "Proparoxítona (todas são acentuadas)"],
  ],
  hiatos: [
    ["acai", "açaí", "I tônico em hiato sozinho na sílaba"],
    ["baus", "baús", "U tônico em hiato seguido de S"],
    ["cai", "caí", "I tônico em hiato sozinho na sílaba"],
    ["faisca", "faísca", "I tônico em hiato seguido de S"],
    ["Paraiba", "Paraíba", "I tônico em hiato sozinho na sílaba"],
    ["egoista", "egoísta", "I tônico em hiato seguido de S"],
    ["ruido", "ruído", "I tônico em hiato sozinho na sílaba"],
    ["saude", "saúde", "U tônico em hiato sozinho na sílaba"],
    ["sauva", "saúva", "U tônico em hiato sozinho na sílaba"],
    ["balaustre", "balaústre", "U tônico em hiato seguido de S"],
    ["incluiram", "incluíram", "I tônico em hiato sozinho na sílaba"],
    ["paises", "países", "I tônico em hiato seguido de S"],
    ["prejuizo", "prejuízo", "I tônico em hiato sozinho na sílaba"],
    ["veiculo", "veículo", "I tônico em hiato sozinho na sílaba"],
    ["juizes", "juízes", "I tônico em hiato sozinho na sílaba"],
    ["Piaui", "Piauí", "I tônico em hiato após ditongo em oxítona"],
    ["tuiuiu", "tuiuiú", "U tônico em hiato após ditongo em oxítona"],
    ["teiu", "teiú", "U tônico em hiato após ditongo em oxítona"],
    ["tuiuius", "tuiuiús", "U tônico em hiato seguido de S após ditongo em oxítona"],
    ["saida", "saída", "I tônico em hiato sozinho na sílaba"],
    ["ciume", "ciúme", "U tônico em hiato sozinho na sílaba"],
    ["atribuida", "atribuída", "I tônico em hiato sozinho na sílaba"],
    ["reune", "reúne", "U tônico em hiato sozinho na sílaba"],
    ["raizes", "raízes", "I tônico em hiato sozinho na sílaba"],
    ["pais", "país", "I tônico em hiato seguido de S"],
    ["incluido", "incluído", "I tônico em hiato sozinho na sílaba"],
    ["Icarai", "Icaraí", "I tônico em hiato sozinho na sílaba"],
    ["construisse", "construísse", "I tônico em hiato seguido de S"],
    ["genuina", "genuína", "I tônico em hiato sozinho na sílaba"],
    ["reunem", "reúnem", "U tônico em hiato sozinho na sílaba"],
  ],
  excessoes: [
    ["raínha", "rainha", "Hiato seguido de NH"],
    ["baínha", "bainha", "Hiato seguido de NH"],
    ["moínho", "moinho", "Hiato seguido de NH"],
    ["Saára", "Saara", "Hiato de vogais repetidas"],
    ["Moóca", "Mooca", "Hiato de vogais repetidas"],
    ["xiíta", "xiita", "Hiato de vogais repetidas"],
    ["vadiíce", "vadiice", "Hiato de vogais repetidas"],
    ["semeêmos", "semeemos", "Hiato de vogais repetidas"],
    ["crêem", "creem", "Hiatos -eem não são mais acentuados"],
    ["lêem", "leem", "Hiatos -eem não são mais acentuados"],
    ["dêem", "deem", "Hiatos -eem não são mais acentuados"],
    ["vôo", "voo", "Hiatos -oo não são mais acentuados"],
    ["enjôo", "enjoo", "Hiatos -oo não são mais acentuados"],
    ["dôo", "doo", "Hiatos -oo não são mais acentuados"],
    ["zôo", "zoo", "Hiatos -oo não são mais acentuados"],
    ["feiúra", "feiura", "I ou U tônico após ditongo decrescente em paroxítona"],
    ["baiúca", "baiuca", "I ou U tônico após ditongo decrescente em paroxítona"],
    ["bocaiúva", "bocaiuva", "I ou U tônico após ditongo decrescente em paroxítona"],
    ["sauípe", "sauipe", "I ou U tônico após ditongo decrescente em paroxítona"],
    ["juíz", "juiz", "Forma sílaba com letra que não seja S (no caso, Z)"],
    ["raúl", "Raul", "Forma sílaba com letra que não seja S (no caso, L)"],
    ["ruím", "ruim", "Forma sílaba com letra que não seja S (no caso, M)"],
    ["caír", "cair", "Forma sílaba com letra que não seja S (no caso, R)"],
    ["saír", "sair", "Forma sílaba com letra que não seja S (no caso, R)"],
    ["aínda", "ainda", "Forma sílaba com letra que não seja S (no caso, N)"],
    ["saíndo", "saindo", "Forma sílaba com letra que não seja S (no caso, N)"],
    ["diúrno", "diurno", "Forma sílaba com letra que não seja S (no caso, N)"],
    ["amendoím", "amendoim", "Forma sílaba com letra que não seja S (no caso, M)"],
    ["cauím", "cauim", "Forma sílaba com letra que não seja S (no caso, M)"],
    ["saíu", "saiu", "Forma sílaba com letra que não seja S (no caso, U)"],
  ],
};

```

possivel complementação para words.ts (sugestão, pode ser adaptado de acordo com a necessidade):

```jsx
export type WordItem = {
  /** Word as it appears in the grid (with or without accent depending on isCorrect). */
  display: string;
  /** Display normalized to single uppercase letters (accents preserved as composed glyphs). */
  letters: string[];
  /** True if this is the correctly-accented form. */
  isCorrect: boolean;
  /** Pair: the correct accented form (for showing to player). */
  correctForm: string;
  /** Pair: the incorrect form. */
  incorrectForm: string;
  /** Pedagogical explanation. */
  rule: string;
};

function splitGraphemes(s: string): string[] {
  // Each "letter" cell in the grid renders one accented char.
  return Array.from(s.toUpperCase());
}

/** Pick a fresh round: 10 correct + 10 incorrect words from random categories. */
export function pickRoundWords(count = 10): WordItem[] {
  const all: WordEntry[] = Object.values(wordsDatabase).flat();
  // Shuffle copy
  const pool = [...all].sort(() => Math.random() - 0.5).slice(0, count);
  const result: WordItem[] = [];
  for (const [incorrect, correct, rule] of pool) {
    // For each pair, push both the correct and incorrect versions
    result.push({
      display: correct,
      letters: splitGraphemes(correct),
      isCorrect: true,
      correctForm: correct,
      incorrectForm: incorrect,
      rule,
    });
    result.push({
      display: incorrect,
      letters: splitGraphemes(incorrect),
      isCorrect: false,
      correctForm: correct,
      incorrectForm: incorrect,
      rule,
    });
  }
  return result;
}

```

## Sistema de Ranking e Persistência de Jogadores

Implementar persistência de jogadores e ranking utilizando **Google Sheets + Google Apps Script** como backend.

**Estrutura da Planilha**

Criar uma planilha Google contendo duas abas:

**Aba: Jogadores**

| Campo | Tipo |
| --- | --- |
| JogadorID | Número |
| NomeUsuario | Texto |
| Avatar | Número |
| DataCadastro | Data/Hora |

**Regras**

- `JogadorID` deve ser único.
- `NomeUsuario` deve ser único.
- O sistema não deve permitir cadastro de nomes duplicados.
- O campo `Avatar` armazenará apenas o identificador numérico do avatar selecionado.
- Os arquivos de avatar estão organizados localmente utilizando nomenclatura numérica:

```jsx
avatars/
1.png
2.png
3.png
...
```

Exemplo:

```jsx
{
  "JogadorID": 1,
  "NomeUsuario": "Maria8A",
  "Avatar": 3
}
```

**Aba: Partidas**

| Campo | Tipo |
| --- | --- |
| PartidaID | Número |
| JogadorID | Número |
| Pontuacao | Número |
| Acertos | Número |
| Erros | Número |
| Tempo | Número |
| Fase | Número |
| Data | Data/Hora |

**Regras**

- Cada partida gera um novo registro.
- O histórico de partidas deve ser preservado.
- A relação entre partida e jogador deve ocorrer através de `JogadorID`.

---

**Fluxo de Cadastro**

Quando o jogador iniciar o jogo:

1. Informa um nome de usuário.
2. Seleciona um avatar.
3. O sistema consulta a aba `Jogadores`.

**Caso o nome já exista**

Exibir:

```
Nome de usuário já utilizado.
Escolha outro nome.
```

Não criar novo registro.

**Caso o nome não exista**

Criar automaticamente:

- JogadorID sequencial.
- NomeUsuario.
- Avatar escolhido.
- DataCadastro.

Retornar os dados do jogador para o frontend.

---

**Fluxo de Partida**

Ao finalizar uma partida:

Registrar na aba `Partidas`:

- JogadorID
- Pontuacao
- Acertos
- Erros
- Tempo
- Fase
- Data

---

**Ranking**

Implementar consulta das partidas para exibição do ranking.

Ordenação:

1. Maior pontuação.
2. Menor tempo (desempate).

Exibir:

- NomeUsuario
- Avatar
- Pontuação

---

**Requisitos Técnicos**

- Utilizar Google Apps Script como API.
- Utilizar Google Sheets como armazenamento de dados.
- Frontend em TypeScript.
- Não armazenar imagens na planilha.
- Armazenar apenas o identificador numérico do avatar.
- O sistema deve estar preparado para futuras expansões como:
    - conquistas;
    - progresso do jogador;
    - estatísticas individuais;
    - ranking por fase;
    - salvamento de progresso.

Priorizar simplicidade, baixo custo e fácil manutenção para um projeto educacional.

Já existe uma planilha Google chamada "Alessa_Ranking" contendo as abas Jogadores e Partidas com os cabeçalhos definidos. Crie o Apps Script necessário para cadastro de jogadores, validação de nomes únicos, gravação de partidas e consulta de ranking.

https://docs.google.com/spreadsheets/d/1De46pnM_Ltycbe46esonztgI9cdX8H0SanrtR-rhTyE/edit?usp=sharing

A cada palavra selecionada pelo mouse haverá uma reação do avatar do jogo que ficará no canto inferior do grid pela animação que usar. Caso o jogador acerte, haverá confetes, emissão de som em festejo e o avatar ficará feliz. caso o jogador erre, leve avermelhar nas bordas da tela com emissão de som de buzina leve. No canto inferior da tela uma caixa de mensagem surge com a regra explicando a acentuação daquela palavra (haverá descrição mais adiante desta caixa).

---
## Edições do prompt: Fluxo de entrada

Jogador digita: Maria

O sistema verifica:

Caso 1 - Nome não existe
Bem-vinda, Maria!
[Nova Jogadora]

Cria o registro normalmente.

Caso 2 - Nome já existe
Já existe uma jogadora chamada Maria.

Você é essa pessoa?

[Sim, sou eu]
[Usar outro nome]

Se clicar em "Sim, sou eu", carrega o progresso existente.

Se clicar em "Usar outro nome", volta para a tela de entrada.

---
Quero simplificar a geração das palavras no tabuleiro.

**ALTERAÇÃO**

As palavras devem ser posicionadas apenas:

* Horizontal 
* Vertical 

Não permitir:

* Diagonais

**OBJETIVO**

Facilitar a leitura das palavras e tornar o jogo mais acessível para estudantes do ensino fundamental.

**REQUISITOS**

1. Atualizar apenas o algoritmo de posicionamento das palavras.
2. Manter o restante da lógica do jogo inalterada.
3. Garantir que as palavras continuem sem sobreposição inválida.
4. Se não houver espaço disponível para posicionar uma palavra horizontalmente ou verticalmente, tentar outra posição válida.
5. Preservar desempenho e funcionamento atual do tabuleiro.






faça uma página para configurações onde o jogador pode editar nome, escolher novamente o avatar e mutar avisos sonoros e música.



