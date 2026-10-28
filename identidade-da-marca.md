# WIG Relógios: identidade da marca e briefing de imagem

> Este arquivo serve como briefing para um gerador de imagem (ChatGPT, Higgsfield etc.).
> Cole as seções 1 a 5 como contexto e depois um dos prompts da seção 6.
> Os prompts estão em inglês porque geradores costumam obedecer melhor assim.

## 1. A marca

**WIG Relógios** é um marketplace brasileiro de compra e venda de relógios com **escrow e vistoriador**. O comprador deposita o valor via PIX, um perito confere o relógio em uma sessão com as duas partes, e o dinheiro só vai ao vendedor com **laudo aprovado e código válido**.

O nome vem das **perucas dos juízes britânicos** (as *wigs* de tribunal). A marca leva a piada a sério: o perito é o "juiz do relógio", o laudo é o veredito, o escrow é o tribunal, e o carimbo decide o caso.

**Frase da marca:** "Ordem na corte."

## 2. Tom de voz

- Fun, irreverente e ácido, sempre no clima de tribunal: "Data venia, não vai rolar", "Objeção negada", "Deferido", "Indeferido", "Condenado".
- As piadas têm só dois alvos: o **mundo do direito** (juiz, toga, jargão, processos que duram décadas) e os **caloteiros e golpistas** (a pena é cadeia ou desemprego).
- **Nunca** se faz piada com o cliente. O cliente é o lado esperto da história.

## 3. Paleta

| Papel | Cor | Hex |
|---|---|---|
| Fundo (preto quente, não azulado) | Ink | `#0a0908` |
| Texto e peruca (branco de papel) | Bone | `#ece7dc` |
| Acento principal (limão-néon) | Lime | `#c6ff2e` |
| Carimbos e sentenças ruins | Red | `#ff3b2f` |
| Só para "Liquidada" (final feliz) | Blue | `#3b82ff` |

Uso: o lime é o único acento. O vermelho aparece só em carimbos e em desfechos negativos. O azul é raro.

## 4. Tipografia

- **Fraunces** (serifada, pesos 300 a 900, itálico): títulos e textos.
- **Space Mono**: rótulos, códigos, laudo, dados, carimbos.
- **UnifrakturMaguntia** (gótica): só o logotipo "WIG".

## 5. Direção visual das imagens

**O que queremos:** escultura **sólida e estilizada**, com sombreamento em poucos degraus (cel-shading / toon), contorno grosso em lime, fundo preto quente. Parece um objeto de arte contemporânea, não uma foto. Futurista pela limpeza e pelo contraste, não por efeitos.

**O que evitar:**
- Holográfico, wireframe, vidro, brilho de "IA".
- Gradiente roxo, índigo ou violeta; blobs desfocados; glassmorphism.
- Realismo fotográfico ou aparência de adereço de festa fantasia.
- Anéis ou órbitas em volta do objeto (parece Saturno).
- Pessoas, rostos, marcas reais, texto legível dentro da imagem.
- Fundo azulado ou cinza.

**Requisitos técnicos:**
- Um único objeto, centralizado, com muita margem.
- Fundo **preto liso** (`#0a0908`) ou transparente. Sem chão e sem sombra projetada.
- Iluminação frontal limpa e uniforme, para facilitar a conversão em modelo 3D.
- Alta resolução (pelo menos 2048 px no lado maior).

## 6. Prompts

### 6.1 Peruca de juiz (visão frontal, base para virar modelo 3D)

```
A single British judge's courtroom wig, front view, perfectly centered, large margins.
Classic barrister wig shape: a rounded dome of tight horizontal rolled curls, with two
rows of stacked cylindrical rolled curls hanging symmetrically on each side, and a
small tail at the back. Stylized contemporary sculpture, solid and chunky, cel-shaded
with 3 to 4 flat tonal steps, warm off-white bone color (#ece7dc) with soft grey-beige
shadows. Thick clean neon lime (#c6ff2e) outline around the whole silhouette and around
each curl. Plain flat warm black background (#0a0908), no floor, no cast shadow, no
rings, no halo, no particles. Even front lighting. Not photorealistic, not holographic,
not wireframe, not glass. No text, no people, no logos. 2048 px, sharp edges.
```

### 6.2 Peruca em três quartos (para dar volume na conversão em 3D)

```
Same stylized British judge's wig as above, three-quarter view from the front-left,
slightly above eye level, perfectly centered, large margins. Solid chunky cel-shaded
sculpture in warm bone (#ece7dc) with thick neon lime (#c6ff2e) outline, plain flat warm
black background (#0a0908), no shadow, no rings, no text.
```

### 6.3 Martelo de tribunal

```
A single courtroom judge's gavel with its round sound block, side view, perfectly
centered, large margins. Stylized contemporary sculpture, solid and chunky, cel-shaded
with 3 to 4 flat tonal steps. Gavel in saturated neon lime (#c6ff2e), sound block in
warm bone (#ece7dc), thick clean dark outline. The gavel head is slightly raised above
the block as if about to strike. Plain flat warm black background (#0a0908), no floor,
no cast shadow, no motion lines, no rings. Even front lighting. Not photorealistic, not
holographic, not wireframe. No text, no people, no logos. 2048 px, sharp edges.
```

### 6.4 Carimbo (opcional, para usar como imagem)

```
A rubber stamp mark reading "DEFERIDO", distressed red ink (#ff3b2f), slightly rotated,
rough worn edges like a real ink stamp, monospaced bold capital letters inside a
rectangular double border, on a transparent or plain black background. No other text.
```

## 7. Depois de gerar

1. Salve as imagens finais **dentro de `p0-landingpage/assets/`** (nunca em Downloads), com nomes simples: `peruca-frente.png`, `peruca-3q.png`, `martelo.png`.
2. Para ter rotação 3D de verdade, converta a imagem da peruca em `.glb` (por exemplo com Meshy ou Tripo) e salve como `assets/peruca.glb`. Meta de tamanho: até alguns MB.
3. Use só material que você mesmo gerou ou com licença livre: o repositório é público.
4. Me avise quando os arquivos estiverem na pasta, e eu integro à página.
