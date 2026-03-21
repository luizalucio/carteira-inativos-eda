# Carteira de Inativos: Análise Descritiva para Avaliação de Risco

Análise exploratória e descritiva da carteira de participantes inativos de uma seguradora, com foco na compreensão do perfil do grupo e avaliação de risco atuarial.

## Sobre o projeto

> Este projeto foi desenvolvido como atividade prática da disciplina **Consultoria em Estatística I (GES 120)**, do curso de Estatística da **Universidade Federal de Lavras (UFLA)**, 3º semestre de 2026, sob orientação do **Prof. Luiz Otávio Pala**.

A atividade foi: Uma seguradora precisa compreender melhor a composição da sua carteira de participantes inativos (aposentados) para fins de avaliação de risco. Este projeto realiza uma análise descritiva estruturada sobre essa base, investigando o perfil demográfico e econômico dos participantes e de seus cônjuges.

A análise busca responder perguntas como:

- Qual é o perfil de idade dos aposentados e de seus cônjuges?
- Existe diferença salarial entre homens e mulheres na carteira?
- Qual é a composição por sexo dos participantes e dos casais?
- Como os dados faltantes se distribuem e o que eles podem indicar?

## Sobre a base de dados

A base contém **6.000 observações** e **5 variáveis**:

| Variável | Descrição |
|---|---|
| `idade_aposentado` | Idade do participante inativo |
| `salario_aposentado` | Salário/benefício do participante |
| `sexo_aposentado` | Sexo do participante (M/F) |
| `idade_conjuge` | Idade do cônjuge (contém NAs) |
| `sexo_conjuge` | Sexo do cônjuge (contém NAs) |

> As variáveis de cônjuge apresentam valores ausentes (NA), que indicam participantes sem cônjuge cadastrado.

## O que foi analisado

### Mapeamento de dados faltantes
- Contagem e percentual de NAs por variável
- Criação de variável auxiliar `tem_conjuge` (True/False)

### Análise individual de cada variável
- **Idade do aposentado:** mediana, média, mínimo, máximo, desvio padrão, histograma e boxplot
- **Salário:** mediana (preferida por ser mais robusta a outliers), histograma e boxplot
- **Sexo do aposentado:** contagem e percentual por categoria
- **Idade do cônjuge:** mesma abordagem da idade do aposentado
- **Sexo do cônjuge:** contagem e percentual

### Análise cruzada de cada variável
- Salário por sexo: existe diferença salarial entre homens e mulheres?
- Idade do aposentado por sexo: homens se aposentam mais velhos?
- Composição dos casais por combinação de sexo
- Diferença de idade entre aposentado e cônjuge (`idade_aposentado - idade_conjuge`)
- Correlação entre salário e idade

## Tecnologias utilizadas

- Python
- Pandas: usei para manipulação e análise dos dados
- Seaborn: usei para as visualizações estatísticas
- Jupyter Notebook: usei no processo de desenvolvimento e exploração, porque eu podia rodar pedaços do código separado. 
- Quarto (.qmd): é onde criei mais familiaridade, por enquanto, para fazer o relatório final reprodutível

## Caso algém queira executar

Não esqueça de instalar as bibliotecas:
```bash
pip install pandas seaborn matplotlib jupyter
```

## Sobre mim

**Luiza Helena Pereira Lúcio**  

Graduanda em Estatística pela Universidade Federal de Lavras (UFLA).

Essa atividade foi programada para ser entregue no dia 24/03/2026, caso você esteja lendo muito tempo depois, é possível que eu já tenha feito novas análises, fique livre para explorar [meu github](https://github.com/luizalucio) e [meu site](https://luizalucio.github.io/meu-site/) 
