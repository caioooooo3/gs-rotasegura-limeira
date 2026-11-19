# RotaSegura Limeira

Análise de dados dos acidentes de trânsito com motociclistas em Limeira (SP), feita para a Global Solution 2026/2 da FIAP (CitizenTech).

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/caioooooo3/gs-rotasegura-limeira/blob/main/RotaSegura_Limeira.ipynb)

## O problema

Em Limeira a moto é ferramenta de trabalho para entregadores, motoboys e muita gente que vai trabalhar de moto. Usamos os dados oficiais do Infosiga SP para entender quem se machuca no trânsito da cidade, quando, onde e com que gravidade, e para propor um alerta de trechos e horários perigosos para motociclistas.

## Principais resultados

| Indicador | Valor |
|---|---|
| Mortes no trânsito por ano (média 2015-2025) | 48,6 (16,7 por 100 mil hab.) |
| Motociclistas entre as vítimas (2019-2024) | 59% |
| Motociclistas feridos em 2024 | 677, o maior número da série |
| Chance de morte ou lesão grave para motociclista ferido | 13,5% (10,2% para quem está de carro) |
| Mesma chance de madrugada | 29% |
| Pontos críticos encontrados com DBSCAN | 14, com 23,5% dos acidentes urbanos com moto |

## Estrutura

```
RotaSegura_Limeira.ipynb    notebook com toda a análise, já executado
dados/
  sinistros_limeira.csv     acidentes em Limeira (Infosiga SP, 2015 a set/2026)
  pessoas_limeira.csv       pessoas envolvidas nesses acidentes
requirements.txt            bibliotecas usadas
```

## Como rodar

**No Google Colab**
1. Clique no botão "Abrir no Colab" acima.
2. Na primeira célula de código, rode o comando abaixo para baixar os dados do repositório:
   ```
   !git clone https://github.com/caioooooo3/gs-rotasegura-limeira.git
   %cd gs-rotasegura-limeira
   ```
3. Menu Ambiente de execução > Executar tudo.

**No computador**
```
git clone https://github.com/caioooooo3/gs-rotasegura-limeira.git
cd gs-rotasegura-limeira
pip install -r requirements.txt
jupyter notebook RotaSegura_Limeira.ipynb
```

O notebook usa caminhos relativos (`dados/...`), então precisa ser aberto de dentro da pasta do projeto.

## Fontes

- Infosiga SP, Detran-SP: https://infosiga.detran.sp.gov.br/ (versão de 17/10/2026, filtrada pelo código IBGE de Limeira, 3526902)
- IBGE, Censo 2022: população de Limeira, 291.869 habitantes

## Integrantes

- Caio Vinicius Paes da Silva (RM 570571)
- Guilherme Augusto Zanelato de Paiva
- Henrique de Araújo Leão
