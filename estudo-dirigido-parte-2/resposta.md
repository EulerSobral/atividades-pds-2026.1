# Cálculo de Convolução Discreta

Respostas da segunda parte do estudo dirigido da disciplina de Processamento Digital de Sinais

## 1. Definição das Sequências
Considerando:
* $x[n] = \{1, 2, 1\}$
* $h[n] = \{1, 1\}$

Assumindo que ambas as sequências iniciam em $n=0$.

## 2. Cálculo Manual da Convolução
A fórmula da convolução discreta é:
$$y[n] = \sum_{k=-\infty}^{\infty} x[k] \cdot h[n-k]$$

O comprimento da sequência resultante $y[n]$ é dado por $L = N_x + N_h - 1 = 3 + 2 - 1 = 4$.

**Cálculos:**

* **Para $n = 0$:**
    $$y[0] = x[0]h[0] = 1 \cdot 1 = 1$$

* **Para $n = 1$:**
    $$y[1] = x[0]h[1] + x[1]h[0] = (1 \cdot 1) + (2 \cdot 1) = 1 + 2 = 3$$

* **Para $n = 2$:**
    $$y[2] = x[1]h[1] + x[2]h[0] = (2 \cdot 1) + (1 \cdot 1) = 2 + 1 = 3$$

* **Para $n = 3$:**
    $$y[3] = x[2]h[1] = 1 \cdot 1 = 1$$

## 3. Resultado em Forma de Sequência
A sequência resultante da convolução é:

**$y[n] = \{1, 3, 3, 1\}$**

## 4. Significado do Resultado Obtido

Significado do resultado da convolução obtido nas questões anteriores:

1.  **Resposta de um Sistema LIT:** Se $x[n]$ for a entrada e $h[n]$ a resposta ao impulso de um sistema Linear e Invariante no Tempo (LIT), $y[n]$ representa a saída do sistema.
2.  **Filtragem:** A sequência $h[n] = \{1, 1\}$ atua como um filtro que soma a amostra atual com a anterior. Isso é uma forma básica de filtro passa-baixas, que tende a suavizar o sinal de entrada.
3.  **Propriedade Polinomial:** A convolução de sequências é matematicamente equivalente à multiplicação de polinômios. Neste caso, $(1 + 2z^{-1} + z^{-2}) \cdot (1 + z^{-1}) = 1 + 3z^{-1} + 3z^{-2} + z^{-3}$.
4.  **Triângulo de Pascal:** A convolução entre os coeficientes de $(a+b)^2$, que são $\{1, 2, 1\}$, e os coeficientes de $(a+b)^1$, que são $\{1, 1\}$, resulta nos coeficientes de $(a+b)^3$, que são $\{1, 3, 3, 1\}$.