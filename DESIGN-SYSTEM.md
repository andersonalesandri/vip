# Design System: Visão Ideal Produções

Base: Raycast (https://getdesign.md/raycast/design-md), adaptado. Usado como referência de componentes e acabamento. O Raycast é 100% escuro; aqui o site é **branco predominante com seções pretas** e acento **magenta**. Implementação de referência: `index.html`.

## Princípios
- Magenta é pontuação: CTA, selo "18 anos", linha condutora, hover. Nunca pintar seções inteiras.
- Preto `#0A0A0B` (nunca `#000`) nas seções escuras. Branco nas seções de conteúdo, para as fotos das obras aparecerem.
- Hover por **opacidade** (0.65), não por troca de cor.
- Bordas sutis em vez de sombras pesadas.
- Uma linha magenta condutora liga os blocos (referência SEGD).

## Cores
| Token | Valor | Uso |
|---|---|---|
| `--preto` | `#0A0A0B` | Seções escuras, navbar, rodapé |
| `--grafite` | `#151517` | Cards e formulário sobre preto |
| `--branco` | `#FFFFFF` | Fundo principal |
| `--off` | `#F6F6F7` | Seções alternadas, faixas |
| `--magenta` | `#E6007E` **[?]** trocar pelo HEX do logo | Acento |
| `--magenta-15` | `rgba(230,0,126,.15)` | Anel de foco, tags |
| `--cinza` | `#9C9C9D` | Texto secundário no escuro |
| `--cinza-claro` | `#CECECE` | Texto de apoio no escuro |
| `--texto-suave` | `#55555A` | Texto de apoio no claro |
| `--borda-escuro` | `rgba(255,255,255,.1)` | Bordas no escuro |
| `--borda-claro` | `#E4E4E7` | Bordas no claro |

Contraste: branco sobre `#E6007E` ≈ 4,5:1 (limite do AA). Se o HEX do logo for mais claro, usar texto preto nos botões ou escurecer o tom.

## Tipografia
Inter (Google Fonts), pesos 400/500/600/700. Tracking +0.1px no corpo; títulos −0.02em.
| Papel | Tamanho | Peso |
|---|---|---|
| Hero (h1) | 38–66px (fluido) | 600 |
| Seção (h2) | 30–46px (fluido) | 600 |
| Card (h3) | 21–22px | 600 |
| Corpo | 16px, linha 1.6 | 400/500 |
| Botão | 15px | 600 |
| Legenda / tag | 12–14px | 500/600 |
| Eyebrow | 12px, caixa alta, tracking .12em | 600 |

## Espaçamento e grid
- Escala: 4 / 8 / 16 / 24 / 40 (base 8px).
- Container 1200px, gutter lateral 20px.
- Seções com 88px de respiro vertical (64px no mobile).
- Grade: 3 colunas → 2 (≤900px) → 1 (≤600px).

## Raios e profundidade
- Botões: pill (9999px). Cards: 12px. Fotos/painéis: 16px. Inputs: 8px. Tags: 6px.
- Contenção por borda de 1px. Sombra só no botão flutuante de WhatsApp.

## Componentes
| Componente | Especificação |
|---|---|
| **Navbar** | Fixa, fundo preto translúcido com blur, links cinza → branco, CTA pill magenta à direita. Menu some abaixo de 900px |
| **Botão primário** | Pill magenta, texto branco, 15px/600. Hover: opacidade .65 |
| **Botão secundário** | Pill com contorno (branco no escuro, preto no claro) |
| **Link de ação** | Texto 600 com seta magenta |
| **Selo** | Pill grafite com bolha magenta ("18 anos") |
| **Eyebrow** | Traço magenta de 28px + texto em caixa alta |
| **Card de serviço** | Borda clara, raio 12px, imagem 16:10 com barra magenta na base, título, texto, link. Hover: borda magenta |
| **Tag** | Fundo off-white ou `magenta-15`, raio 6px |
| **Item de lista (food)** | Fundo grafite, borda sutil, raio 10px, título + legenda |
| **Painel de marca/ambiente** | Raio 16px, linha magenta com ponto no topo, chips de escopo |
| **Pacote** | Card claro; versão destaque em preto |
| **Portfólio** | Mosaico de 12 colunas (7+5, 4+4+4), legenda sobre a foto, filtros em pills |
| **Processo** | 4 colunas, filete superior e rótulo "Etapa N" magenta (sequência real) |
| **Logos / depoimentos** | Logos em grade de 6 (3 no mobile); depoimentos em cards de 3 colunas |
| **Formulário** | Painel grafite, inputs pretos com borda sutil, foco com borda magenta + anel `magenta-15` |
| **WhatsApp flutuante** | Pill magenta fixa no canto inferior direito |
| **Rodapé** | Preto, links cinza → branco |

## Responsivo
Mobile-first. Breakpoints: 600 / 900. Hero cai para uma coluna e a foto muda para 16:10. Sem rolagem horizontal.

## Acessibilidade
Foco visível (contorno magenta 2px), `prefers-reduced-motion` respeitado, alt text em todas as imagens reais, rótulos em todos os campos.

## Não adotar do Raycast
Teclas de atalho (keycaps), janelas de macOS, brilho quente, fundo escuro em todo o site, cores semânticas extras (azul, amarelo). Verde e vermelho só para estados do formulário.
