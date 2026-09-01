# 1. As Duas Fases

## Fase 1: A Superfície

- **Tema:** A fase funciona como o "Mundo Superior" da superfície, um ambiente pacífico e tropical.
- **Ação:** O jogador sai de casa, percorre plataformas sobre a água e avança até encontrar uma fenda no chão.
- **Decisão:** O buraco no final do mapa serve para fazer a transição para a próxima fase.

## Fase 2: Mundo Subterrâneo

- **Tema:** O cenário representa um novo mundo que existe abaixo da superfície.
- **Ação:** O jogador se aventura pelo mundo subterrâneo.
- **Decisão:** Adicionei blocos azuis para serem usados como recompensa de diamantes na área secreta.

---

# 2. O Parallax

- **Camada do Céu:** Na fase 1, usei o `motion_scale` em **(0, 0)**, pois o fundo é uma cor sólida e não fazia sentido alterar a escala para gerar movimento.

- **Camada das Nuvens:** Usei **0,1 no eixo X** e **0,05 no eixo Y**. Deixei o valor do Y menor, pois isso passa uma sensação de movimento mais devagar e suave na vertical do parallax.

- **Água:** Usei **0,3 no eixo X** e **0,2 no eixo Y**. Como era a camada que tinha que passar a sensação de mais próximo, essa ficou com o maior valor das camadas.

- **Tentativa inicial vs. Versão Final:** O que mudou foi que, na primeira tentativa, eu havia confundido os valores, o que fez com que a velocidade de cada camada ficasse invertida. Na versão final, corrigi a ordem para o efeito funcionar corretamente.

---

# 3. Área secreta

A pista é indicado por diamantes, fica em uma mini montanha, mas sem entrada aparente, separei dessa forma para que a unica forma de conseguir é tentar mesmo sem certeza.

# 4. A Câmera

Optei pela **câmera como cena própria**, pois além de ser a versão construída em aula, ela é mais flexível, permitindo trocar o alvo depois, e a outro tipo não permite ser reaproveitada em outras cenas ou projetos sem depender do personagem.

---

# 5. Transição

Trocar a cena durante a detecção de colisão causa um erro, pois o jogo ainda esta processando, ele ainda está usando os nós da cena pra concluir os processamentos de física.

---

# 6. O que travou

Por incrível que pareça, eu só travei na parte da câmera, só estava sendo possivel criar o grupo no nó importado do player, e não direto na cena dele, só depois de salvar o projeto eu descobri que era isso que estava faltando.