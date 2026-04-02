# Resoluções — Lógica e Raciocínio 📚

> Explicações detalhadas para cada questão, do jeito mais simples possível.

---

## Questão 1 — Contrapositiva

**O que a questão pede?**
Encontrar uma sentença **logicamente equivalente** a "Se Carlos é matemático, então ele é professor."

### O que é equivalência lógica?

Duas sentenças são logicamente equivalentes quando têm **exatamente os mesmos valores verdade** em todas as situações. Ou seja, quando uma é verdadeira, a outra também é; quando uma é falsa, a outra também é.

### O que é contrapositiva?

Toda sentença do tipo **"Se P então Q"** tem uma equivalente chamada **contrapositiva**, que é **"Se não Q então não P"** — ou seja, você nega os dois lados E inverte a ordem.

```
Original:      Se P       → então Q
Contrapositiva: Se (não Q) → então (não P)
```

### Aplicando na questão:

```
Original:       Se Carlos É matemático   → então ele É professor
                     P                          Q

Contrapositiva: Se Carlos NÃO É professor → então ele NÃO É matemático
                        ¬Q                          ¬P
```

> **Atenção:** as outras opções são armadilhas comuns:
> - **Inversa** (negar os dois sem inverter): "Se não é matemático → não é professor" ❌ não é equivalente
> - **Recíproca** (inverter sem negar): "Se é professor → é matemático" ❌ não é equivalente

✅ **Resposta: A — "Se Carlos não é professor, então ele não é matemático."**

---

## Questão 2 — Tabela-verdade [P→Q] ∧ [Q∨R]

**O que a questão pede?**
Preencher a última coluna da tabela-verdade para a proposição **[P→Q] ∧ [Q∨R]**.

### Revisando os conectivos:

| Conectivo | Símbolo | Quando é VERDADEIRO? |
|-----------|---------|----------------------|
| E (AND) | ∧ | Somente quando os **dois** lados são V |
| OU (OR) | ∨ | Quando **pelo menos um** lado é V |
| SE...ENTÃO | → | **Falso APENAS** quando o 1º é V e o 2º é F |

### Calculando linha por linha:

A expressão tem duas partes: **[P→Q]** e **[Q∨R]**. O resultado final é a conjunção (∧) das duas.

| P | Q | R | P→Q | Q∨R | **[P→Q] ∧ [Q∨R]** |
|---|---|---|-----|-----|-------------------|
| V | V | V | V | V | **V** |
| V | V | F | V | V | **V** |
| V | F | V | F | V | **F** |
| V | F | F | F | F | **F** |
| F | V | V | V | V | **V** |
| F | V | F | V | V | **V** |
| F | F | V | V | V | **V** |
| F | F | F | V | F | **F** |

> **Dica para P→Q:** lembre que a implicação só é **falsa** quando P=V e Q=F (linhas 3 e 4). Em todos os outros casos é verdadeira — inclusive quando P é falso!

Resultado de cima para baixo: **V, V, F, F, V, V, V, F**

✅ **Resposta: C — V, V, F, F, V, V, V e F**

---

## Questão 3 — Álgebra Booleana: S = A + B·C

**O que a questão pede?**
Saber em qual ordem realizar as operações na expressão booleana S = A + B·C.

### A regra de precedência:

Na álgebra booleana, assim como na matemática comum, existe uma **hierarquia de operações**:

```
Matemática comum:   × e ÷  têm prioridade sobre  + e −
Álgebra booleana:   · (AND) tem prioridade sobre  + (OR)
```

Pensa assim: o ponto (·) é o "multiplication" do mundo booleano, e o mais (+) é a "addition". A regra é a mesma!

### Aplicando na expressão:

```
S = A + B · C
         ↑
    Isso é feito PRIMEIRO (AND)

S = A + (B · C)
     ↑
  Isso é feito DEPOIS (OR)
```

**Passo 1:** Calcula B · C (AND)
**Passo 2:** Calcula A + resultado (OR)

✅ **Resposta: A — Em primeiro lugar, deve-se realizar a operação AND para depois realizar a operação OR.**

---

## Questão 4 — Sentença aberta

**O que a questão pede?**
Identificar qual das alternativas é uma **sentença aberta**.

### O que é sentença aberta?

| Tipo | Definição | Exemplo |
|------|-----------|---------|
| **Proposição fechada** | Tem valor verdade definido (V ou F) | "2 + 2 = 4" → sempre V |
| **Sentença aberta** | Contém um elemento indefinido — **não dá para dizer V ou F sem mais informação** | "Alguma cidade X está com crise" → depende de qual cidade |

### Analisando as alternativas:

- **A:** "Porto Alegre é capital da região sul..." → fala de lugar específico, dá para verificar → **proposição fechada**
- **B:** "**Alguma** cidade da região sul do Brasil está com surto de sarampo" → depende de *qual* cidade estamos avaliando, não dá para dizer V ou F sem essa informação → **sentença aberta** ✅
- **C:** "Antônio é o engenheiro responsável..." → fala de pessoa específica, dá para verificar → **proposição fechada**
- **D:** "Carlos e Antônio são os farmacêuticos..." → idem → **proposição fechada**
- **E:** "Gramado tem cobertura total..." → fala de lugar específico → **proposição fechada**

> O "alguma" na alternativa B funciona como uma variável disfarçada — o valor verdade depende de qual cidade estamos considerando, tornando-a uma sentença aberta.

✅ **Resposta: B**

---

## Questão 5 — Conjunto-verdade de p(x) ∨ q(x)

**O que a questão pede?**
Encontrar todos os valores de x que tornam **p(x) OU q(x)** verdadeira.

### O que é conjunto-verdade?

É o conjunto de todos os valores de x que tornam a sentença verdadeira. Como é um OU (∨), basta que **uma das duas** equações seja satisfeita.

### Passo 1 — Resolver p(x): x² − 6x + 5 = 0

Usando Bhaskara:
```
a=1, b=-6, c=5
Δ = (-6)² - 4·1·5 = 36 - 20 = 16
√Δ = 4

x = (6 + 4)/2 = 5
x = (6 - 4)/2 = 1
```
Conjunto-verdade de p(x) = **{1, 5}**

### Passo 2 — Resolver q(x): x² − 13x + 36 = 0

```
a=1, b=-13, c=36
Δ = (-13)² - 4·1·36 = 169 - 144 = 25
√Δ = 5

x = (13 + 5)/2 = 9
x = (13 - 5)/2 = 4
```
Conjunto-verdade de q(x) = **{4, 9}**

### Passo 3 — Aplicar o OU (∨)

Como é OU, o conjunto-verdade final é a **união** dos dois conjuntos:
```
{1, 5} ∪ {4, 9} = {1, 4, 5, 9}
```

✅ **Resposta: E — {1, 4, 5, 9}**

---

## Questão 6 — Tabela-verdade (R→T)↔R

**O que a questão pede?**
Preencher a última coluna da tabela para **(R→T)↔R**.

### Revisando o bicondicional (↔):

O bicondicional é verdadeiro quando **os dois lados têm o mesmo valor**:

| Lado esquerdo | Lado direito | Resultado ↔ |
|---------------|--------------|-------------|
| V | V | **V** |
| V | F | **F** |
| F | V | **F** |
| F | F | **V** |

### Calculando linha por linha:

**Linha 1: R=V, T=V**
```
R→T = V→V = V
(R→T)↔R = V↔V = V ✅
```

**Linha 2: R=V, T=F**
```
R→T = V→F = F
(R→T)↔R = F↔V = F ❌
```

**Linha 3: R=F, T=V**
```
R→T = F→V = V
(R→T)↔R = V↔F = F ❌
```

**Linha 4: R=F, T=F**
```
R→T = F→F = V
(R→T)↔R = V↔F = F ❌
```

Resultado de cima para baixo: **V, F, F, F**

✅ **Resposta: B — V, F, F e F**

---

## Questão 7 — Lógica de predicados (Prolog)

**O que a questão pede?**
Traduzir a pergunta *"Será que Laura gosta de sorvete e Carlos gosta de torta?"* para a notação de lógica de predicados (estilo Prolog).

### Como funciona a notação de predicados?

Um predicado é escrito como: `nome_do_predicado(argumento1, argumento2)`

Então:
```
"Laura gosta de sorvete" → gosta(laura, sorvete)
"Carlos gosta de torta"  → gosta(carlos, torta)
```

### O "e" e a pergunta:

- Em Prolog, o **"e"** (conjunção) é representado por uma **vírgula** `,`
- Uma **pergunta** começa com `?-`

Juntando tudo:
```
?- gosta(laura, sorvete), gosta(carlos, torta)
```

> **Por que a vírgula e não "e"?** Porque em Prolog a vírgula significa "e também precisa ser verdade que...". É a notação padrão da linguagem.

✅ **Resposta: C — ?- gosta(laura, sorvete), gosta(carlos, torta)**

---

## Questão 8 — Gestão de equipe sob pressão

**O que a questão pede?**
Qual a melhor abordagem para João ajudar uma equipe que **trava** diante de situações inesperadas e age de forma defensiva?

### Entendendo o problema da equipe:

O enunciado diz que a equipe tem **dois problemas centrais**:
1. **Paralisa** diante de situações inesperadas
2. Age de maneira **defensiva**

Esses dois comportamentos têm uma raiz em comum: **estresse e ansiedade**. Quando uma pessoa (ou equipe) está sob estresse elevado, o cérebro entra em modo de "luta ou fuga" — e é exatamente isso que provoca o travamento e a postura defensiva.

### Por que Mindfulness resolve?

O mindfulness ataca essa **raiz do problema**:

```
Problema:  Equipe trava + age defensivamente
    ↓
Causa:     Estresse e ansiedade elevados
    ↓
Solução:   Mindfulness → reduz estresse → mente mais calma
    ↓
Resultado: Pensamento criativo + abertura → resolve problemas complexos
```

- **Reduz o estresse** → a equipe para de travar diante do inesperado
- **Acalma a mente** → abre espaço para o pensamento criativo, essencial para problemas complexos
- **Diminui a defensividade** → equipe menos ansiosa age com mais abertura e colaboração

### Por que as outras alternativas não funcionam?

- **B:** Delegar para inexperientes não trata a causa — o problema é emocional, não de distribuição de tarefas ❌
- **C:** Sistema de penalidades **aumentaria** o estresse e a defensividade, piorando exatamente o que se quer resolver ❌
- **D:** Simular crises em uma equipe que **já trava sob pressão** seria contraproducente — jogaria mais estresse sobre quem já não consegue lidar com ele. Além disso, "sem pensar nos sentimentos dos outros" ignora justamente o componente emocional que é a raiz do problema ❌
- **E:** Reuniões só para discutir erros sem focar em soluções reforçaria a ansiedade e o comportamento defensivo ❌

✅ **Resposta: A — Ensinar a equipe a usar técnicas de mindfulness para reduzir o estresse e estimular a criatividade.**

---

## Questão 9 — Mentalidade de crescimento

**O que a questão pede?**
Como Carlos pode aplicar a **mentalidade de crescimento** para lidar com um colega inflexível num conflito?

### O que é mentalidade de crescimento?

É a crença de que habilidades e inteligência podem ser desenvolvidas com esforço e aprendizado. Quem tem essa mentalidade enxerga **erros e conflitos como oportunidades de aprender**, não como ameaças.

### Analisando as alternativas:

- **A:** Desafiar o colega para provar que está errado → postura combativa, sem aprendizado ❌
- **B:** Usar o conflito para refletir sobre como o erro pode ser uma chance de aprendizado → isso é exatamente a mentalidade de crescimento ✅
- **C:** Ignorar o conflito → não resolve nem aprende nada ❌
- **D:** Impor a própria opinião → postura de mentalidade fixa ❌
- **E:** Pedir que todos guardem suas opiniões → evita o conflito mas não promove crescimento ❌

✅ **Resposta: B**

---

## Questão 10 — Inteligência emocional na tomada de decisão

**O que a questão pede?**
Qual estratégia Fernanda pode usar para **reduzir a influência da ansiedade** e tomar uma decisão mais racional?

### O problema:

Fernanda está ansiosa e teme que suas emoções prejudiquem a decisão. Emoções intensas "turvam" o julgamento porque nos fazem focar no que sentimos agora em vez do que é objetivamente melhor.

### Analisando as alternativas:

- **A:** Tomar a decisão imediatamente → decide sob o pico da ansiedade, pior momento ❌
- **B:** Distanciamento emocional, pensando como aconselharia um amigo → técnica comprovada: quando imaginamos que estamos aconselhando outra pessoa, nos distanciamos emocionalmente e pensamos com mais clareza ✅
- **C:** Buscar consenso de todos → pode atrasar demais e diluir a responsabilidade ❌
- **D:** Focar apenas em benefícios imediatos → ignora impactos futuros, decisão míope ❌
- **E:** Confiar só na intuição → quando ansioso, a intuição está distorcida pelas emoções ❌

> O distanciamento emocional ("como eu aconselharia um amigo nessa situação?") é uma técnica clássica da psicologia cognitiva, conhecida como "Solomon's Paradox" — somos mais sábios ao aconselhar os outros do que a nós mesmos.

✅ **Resposta: B**

---

*Documento gerado como material de estudo e revisão.*
