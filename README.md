# 🎬 Recomendador de Filmes com Matemática para Inteligência Artificial

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RonildoNascimento/recomendador-de-filmes/blob/main/Recomendador_de_Filmes.ipynb)

<br>

Projeto desenvolvido em **Python** no **Google Colab** com o objetivo de explorar conceitos matemáticos fundamentais utilizados em Inteligência Artificial por meio da construção e análise de um sistema de recomendação de filmes.
O projeto combina conceitos de **Álgebra Linear, Cálculo e Métodos Numéricos**, mostrando na prática como ferramentas matemáticas podem ser utilizadas em sistemas de recomendação e modelos de Machine Learning.

## 🎯 Objetivo do Projeto

Construir um recomendador de filmes didático e, ao mesmo tempo, compreender alguns dos principais fundamentos matemáticos utilizados em Inteligência Artificial.

Ao longo do notebook são explorados conceitos como:

- Vetores e matrizes
- Produto interno
- Similaridade por cosseno
- Transformações lineares
- Decomposição em Valores Singulares (SVD)
- Redução de dimensionalidade
- Derivadas
- Gradiente descendente
- Métodos numéricos
- Integração numérica

## 🧠 Como funciona o recomendador

O sistema utiliza uma **matriz de avaliações**, na qual:

- cada linha representa um usuário;
- cada coluna representa um filme;
- cada valor representa uma nota de **0 a 5**;
- o valor `0` representa um filme ainda não assistido.

A partir dessas informações, diferentes técnicas matemáticas são aplicadas para analisar preferências e compreender como recomendações podem ser produzidas.

## 🤝 Similaridade entre usuários

Uma das primeiras técnicas utilizadas é a **similaridade por cosseno**.

Cada usuário é representado como um vetor contendo suas avaliações de filmes.

A similaridade é calculada por:

\[
sim(u,v)=\frac{u \cdot v}{||u||\,||v||}
\]

Valores próximos de **1** indicam usuários com padrões de avaliação mais semelhantes.

Essa abordagem permite analisar usuários com gostos parecidos e utilizar suas avaliações como referência para uma possível recomendação.

O notebook também discute uma limitação importante: utilizar `0` para representar um filme não assistido pode fazer o algoritmo interpretar esse valor como uma avaliação negativa.

## 🌀 Transformações Lineares

O projeto também demonstra como matrizes podem funcionar como **transformações de vetores**.

São utilizados exemplos gráficos para visualizar operações como:

- rotação;
- alongamento;
- compressão.

Essa etapa ajuda a compreender a matemática utilizada em diversos modelos de Machine Learning e redes neurais.

## 🔍 SVD — Decomposição em Valores Singulares

Uma das principais técnicas estudadas é a **Singular Value Decomposition (SVD)**.

A decomposição é representada por:

\[
R = U\Sigma V^T
\]

No contexto do recomendador, a SVD permite investigar **características latentes** existentes na matriz de avaliações.

O notebook trabalha com uma matriz de avaliações sintética contendo usuários e filmes associados principalmente a dois padrões de preferência:

**Ação** e **Drama**.

A análise dos valores singulares permite estudar quais componentes carregam mais informação e como reconstruir a matriz utilizando apenas parte desses componentes.

## 📉 Compressão da matriz

Após realizar a SVD, o projeto reconstrói a matriz utilizando diferentes quantidades de componentes.

\[
R_k = U_k\Sigma_kV_k^T
\]

O erro de reconstrução é analisado para compreender o equilíbrio entre:

**quantidade de componentes × informação preservada × redução de dimensionalidade.**

Essa técnica está diretamente relacionada a aplicações de compressão, redução de dimensionalidade e sistemas de recomendação.

## 📈 Gradiente Descendente

O projeto apresenta também um dos algoritmos fundamentais do aprendizado de máquina: o **Gradiente Descendente**.

A atualização de um parâmetro segue a ideia:

\[
x_{novo}=x_{atual}-\alpha f'(x_{atual})
\]

onde `α` representa a taxa de aprendizado.

São realizados experimentos com diferentes taxas para observar situações de:

- convergência;
- aprendizagem lenta;
- oscilações;
- divergência.

## 🤖 Treinamento de um modelo simples

O gradiente descendente também é utilizado para ajustar um modelo:

\[
y=w \cdot x
\]

O objetivo é aprender automaticamente o parâmetro `w` minimizando o **Erro Quadrático Médio**.

Esse experimento demonstra, de maneira simplificada, o princípio utilizado por algoritmos de Machine Learning para ajustar parâmetros a partir dos dados.

## 🧮 Métodos Numéricos

O notebook explora ainda a aproximação numérica de derivadas utilizando **diferenças finitas**:

\[
f'(x)\approx\frac{f(x+h)-f(x)}{h}
\]

O experimento permite observar um conceito importante da computação científica: valores extremamente pequenos de `h` podem provocar problemas relacionados à precisão numérica e ao arredondamento em ponto flutuante.

## 📐 Integração Numérica

Também é explorada a aproximação de integrais utilizando o **Método dos Trapézios**.

Essa etapa demonstra como computadores podem aproximar áreas e valores acumulados numericamente quando uma solução analítica não está disponível ou não é conveniente.

## 🛠️ Tecnologias utilizadas

- Python
- NumPy
- Matplotlib
- Google Colab
- Jupyter Notebook
- Git
- GitHub

## 📚 Principais conceitos estudados

| Área | Conceitos |
|---|---|
| Álgebra Linear | Vetores, matrizes e produto interno |
| Recomendação | Similaridade por cosseno |
| Transformações | Transformações lineares |
| Fatoração | SVD |
| Dimensionalidade | Compressão e reconstrução de matrizes |
| Cálculo | Derivadas e integrais |
| Machine Learning | Gradiente descendente |
| Otimização | Taxa de aprendizado e convergência |
| Métodos Numéricos | Diferenças finitas e regra dos trapézios |

## 📁 Estrutura do repositório

```text
recomendador-de-filmes/
│
├── Recomendador_de_Filmes.ipynb
├── README.md
├── LICENSE
└── .gitattributes
```

## ▶️ Como executar

O projeto pode ser executado utilizando:

**Google Colab** ou **Jupyter Notebook**.

Para executar localmente, é necessário ter Python e as bibliotecas utilizadas no projeto instaladas.

O notebook deve ser executado sequencialmente para acompanhar os experimentos, gráficos e análises.

## 🎓 Aprendizados

Este projeto demonstra como conceitos matemáticos que muitas vezes são estudados de maneira abstrata possuem aplicações diretas em Inteligência Artificial.

A construção do recomendador permite relacionar:

**Matemática → Dados → Algoritmos → Machine Learning → Sistemas de Recomendação**

Além da implementação em Python, o projeto enfatiza a interpretação dos resultados e a compreensão matemática por trás dos algoritmos.

## 👨‍💻 Autor

**Ronildo Batista do Nascimento**

Consultor Comercial | Desenvolvedor de Sistemas | Inteligência Artificial & Automação | Tecnologia aplicada a negócios

Projeto desenvolvido como parte dos estudos de **Matemática para Inteligência Artificial**.
