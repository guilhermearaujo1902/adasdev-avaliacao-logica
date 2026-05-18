# Prova de Lógica de Programação — Portugol

## Identificação da prova

| Campo | Informação |
|-------|------------|
| **Disciplina** | Lógica de Programação |
| **Linguagem** | Portugol (pseudocódigo) |

### Instruções gerais

- Leia todos os enunciados antes de começar.
- Nos algoritmos, use: `algoritmo`, `var`, `inicio`, `fim`, `escreva`, `leia`, indentação clara.
- Comente apenas quando o enunciado pedir.
- Critérios: correção lógica, uso adequado das estruturas estudadas, nomes de variáveis claros.

---

# Bloco A — Conhecimento teórico

---

### Questão 1 — Variáveis e tipos

> **Contexto:** Você está montando um perfil num app de estudos (tipo *studygram*).

Para cada dado abaixo, indique o **tipo mais adequado** em Portugol (`inteiro`, `real`, `caractere` ou `logico`) e **um nome de variável** sugerido (em português, sem espaços):

| Dado | Tipo | Nome da variável |
|------|:----:|------------------|
| Quantidade de horas estudadas hoje | | |
| Nota da última atividade (0 a 10, com decimal) | | |
| Nome da matéria favorita | | |
| Marcou "lembrar de estudar amanhã"? (sim/não) | | |

---

### Questão 2 — Operadores aritméticos

> **Contexto:** Uma influencer postou um vídeo de 2 minutos e 30 segundos. O app só guarda a duração em **segundos totais**.

Escreva uma lógica que converta **2 minutos e 30 segundos** em segundos (use apenas números e operadores).

---

### Questão 3 — Operadores relacionais e lógicos

> **Contexto:** Promoção em app de delivery — frete grátis se o pedido for *bom o suficiente*.

Sabendo: `valor_pedido` (real), `cupom_ativo` (logico), `distancia_km` (real).

O frete é grátis quando: **(valor do pedido ≥ 50)** E **(cupom ativo OU distância ≤ 3 km)**.

**a)** Escreva essa condição em uma única expressão lógica guardando o resultado em uma variável.

**b)** Se `valor_pedido = 45`, `cupom_ativo = FALSO`, `distancia_km = 2`, o frete é grátis? **Justifique** calculando a expressão passo a passo.

---

### Questão 4 — Estrutura SE…SENÃO

> **Contexto:** Playlist automática de treino.

Complete o trecho para classificar o nível do treino conforme `minutos` (inteiro):

| Minutos | Classificação |
|---------|---------------|
| até 20 | `"leve"` |
| de 21 a 45 | `"moderado"` |
| acima de 45 | `"intenso"` |

```portugol
se (__________) entao
    escreva("leve")
senao
    se (__________) entao
        escreva("moderado")
    _____
        escreva("intenso")
    fimse
fimse
```

Preencha apenas as condições nos espaços em branco.

---

### Questão 5 — Variáveis e tipos (conceito)

> **Contexto:** Cadastro em fórum de série.

Explique com suas palavras:

**a)** Em um cadastro, o algoritmo guarda o nome da série em `nome_serie`. O que é uma **variável**? O que ela armazena e o que pode acontecer com o valor dela durante o algoritmo?

**b)** A mesma pessoa também informa `idade` (quantos anos tem). Qual **tipo** você escolheria para `idade` (`inteiro`, `real`, `caractere` ou `logico`)? Por quê?

---

### Questão 6 — Operadores (revisão integrada)

> **Contexto:** Enquete rápida no grupo da turma.

Dadas as variáveis: `votos_a = 12`, `votos_b = 12`, `total_votos = 24`.

Calcule o valor **verdadeiro ou falso** de cada expressão (mostre o cálculo):

| Item | Expressão |
|:----:|-----------|
| **a)** | `votos_a > votos_b` |
| **b)** | `votos_a = votos_b` |
| **c)** | `(votos_a + votos_b) = total_votos` |
| **d)** | `NAO (votos_a < votos_b) E (total_votos > 20)` |

---

### Questão 7 — Estrutura ESCOLHA

> **Contexto:** Food truck na faculdade — o cliente digita um código no totem para escolher o lanche. Use a folha de apoio com as estruturas apenas se precisar consultar a sintaxe.

A variável `codigo` (inteiro) já foi lida. Cada valor exibe uma mensagem:

| codigo | Mensagem exibida |
|:------:|------------------|
| 1 | `"Cachorro-quente"` |
| 2 | `"Refrigerante"` |
| 3 | `"Combo do dia"` |
| 4 | `"Sorvete"` |
| outro | `"Item nao encontrado"` |

**a)** Em uma ou duas frases: quando faz sentido usar `escolha` em vez de vários `se…senão`?

**b)** Se `codigo` vale **3**, qual mensagem aparece na tela?

**c)** Qual valor (ou valores) `codigo` pode ter para aparecer `"Item nao encontrado"`? Dê pelo menos dois exemplos.

---

### Questão 8 — Laço ENQUANTO (conceito)

> **Contexto:** Jogo mobile — a personagem só pode pular enquanto tiver energia.

**a)** Em uma frase: quando usamos `enquanto` em vez de `para`?

**b)** O trecho abaixo tem um erro que pode causar **loop infinito**. Circule a linha problemática e reescreva-a corretamente.

```portugol
energia <- 3
enquanto energia > 0 faca
    escreva("Pulo!")
fimenquanto
```

---

# Bloco B — Rastreio e leitura de código

---

### Questão 9 — Operadores + SE…SENÃO

> **Contexto:** *Streak* de dias seguidos usando um app de hábitos.

Considere o algoritmo:

```portugol
dias <- 5
bonus <- 0
se dias >= 7 entao
    bonus <- 10
senao
    se dias >= 3 entao
        bonus <- 5
    fimse
fimse
pontos <- dias * 2 + bonus
escreva(pontos)
```

**a)** Qual valor é exibido na tela?

**b)** Se `dias` fosse 7, qual seria o valor exibido?

---

### Questão 10 — ESCOLHA

> **Contexto:** Escolha de figurinha para avatar.

```portugol
codigo <- 2
escolha codigo
    caso 1: tema <- "gato"
    caso 2: tema <- "praia"
    caso 3: tema <- "astronauta"
    outrocaso: tema <- "padrao"
fimescolha
escreva(tema)
```

**a)** O que é impresso?

**b)** Altere **apenas** o valor inicial de `codigo` para que imprima `"padrao"`. Qual valor você usaria e porque?

---

### Questão 11 — ENQUANTO

> **Contexto:** Máquina de vendas de água reutilizável — a cada uso ganha 1 ponto ecológico.

```portugol
garrafas <- 4
pontos <- 0
enquanto garrafas > 0 faca
    pontos <- pontos + 1
    garrafas <- garrafas - 1
fimenquanto
escreva(pontos)
```

**a)** Valor final de `pontos`?

**b)** Quantas vezes o bloco do `enquanto` é executado?

**c)** Se começássemos com `garrafas <- 0`, quantas vezes o bloco executaria? Por quê?

---

### Questão 12 — PARA

> **Contexto:** Contagem regressiva para live.

```portugol
para i de 3 ate 1 passo -1 faca
    escreva(i)
fimpara
escreva("Ao vivo!")
```

**a)** Escreva, **na ordem**, tudo que apareceria na tela (uma linha por saída).

**b)** Quantas vezes o `escreva(i)` dentro do `para` executa e porque?

---

# Bloco C — Prática: algoritmos

---

### Questão 13 — SE…SENÃO + variáveis + operadores

> **Contexto:** Ingresso para cinema/clube escolar com meia-entrada.

Leia: `idade` (inteiro) e `estudante` (logico — verdadeiro se a pessoa é estudante).

Calcule e exiba o **valor do ingresso**:

| Condição | Valor |
|----------|:-----:|
| `estudante` verdadeiro **OU** idade menor que 18 | R$ 15,00 |
| caso contrário | R$ 30,00 |

Use variável `valor` (real). Escreva uma mensagem de saída de dados utilizando o valor.

---

### Questão 14 — ESCOLHA

> **Contexto:** Calculadora de *humor do dia* (versão descontraída para redes).

Leia um inteiro `emoji` de 1 a 5:

| emoji | Mensagem |
|:-----:|----------|
| 1 | `"Dia produtivo"` |
| 2 | `"Preciso de cafe"` |
| 3 | `"Modo foco"` |
| 4 | `"Só observando"` |
| 5 | `"Playlist triste on"` |
| outro | `"Emoji desconhecido"` |

Monte o algoritmo completo com `escolha`. **Não** use vários `se` encadeados — use `escolha`.

---

### Questão 15 — ENQUANTO

> **Contexto:** Desafio de hidratação — meta de copos de água por dia.

Leia `meta` (inteiro, quantos copos quer beber).

Enquanto `copos_bebeidos < meta`:

- incremente `copos_bebeidos`
- a cada copo, exiba: `"Copo X de Y"` (X = atual, Y = meta)

Ao terminar, exiba: `"Meta do dia alcancada!"`

**Requisitos:** usar `enquanto`; inicializar contadores; **não** usar `para`.

---

### Questão 16 — PARA + operadores + variáveis

> **Contexto:** Votação para melhor música da festa junina da turma.

Dada a quantidade total de 10 votos na turma, para cada voto:

- leia `nota` (inteiro de 0 a 10)

Ao final, exiba:

- `soma` das notas
- `media` (real)
- se `media >= 7`, escreva `"Aprovada para o playlist!"`
- senão, escreva `"Ainda da para melhorar"`

Use `para`. Trate `media` como `soma / quantidade_votos` (divisão real).

---

*Fim da prova*
