# Ponderada Requisitos não funcionais
## Requisitos:

Os requisitos de um sistema são divididos em duas categorias principais: **Requisitos Funcionais** e **Requisitos Não Funcionais**.

- **Requisitos Funcionais (RF):** São aqueles que definem o que o sistema deve fazer. Eles descrevem comportamentos ou funcionalidades específicas do sistema.
- **Requisitos Não Funcionais (RNF):** São aqueles que definem as qualidades do sistema, como desempenho, segurança, usabilidade, etc. Eles detalham como o sistema deve operar.

## Requisitos Funcionais (RF)

Os requisitos abaixo foram elaborados em conjunto com o grupo e descrevem as funcionalidades do sistema e suas métricas de desempenho.


| **Identificador** | **Requisito** | **Classificação** |
|-------------------|---------------|-------------------|
| RF01 | O sistema deve identificar e classificar as fissuras. | Essencial |
| RF02 | O sistema deve permitir o upload de arquivos para a identificação e classificação. | Essencial |
| RF03 | O sistema deve fazer análise das imagens de forma síncrona. | Desejável |
| RF04 | O sistema deve guardar o histórico de todas as expedições. | Essencial |
| RF05 | O sistema deve mostrar as estatísticas sobre as expedições. | Importante |
| RF06 | O sistema deve relacionar as fissuras detectadas com suas possíveis causas. | Desejável |
| RF07 | O sistema deve identificar a espessura da fissura. | Desejável |
| RF08 | O sistema deve ter um mecanismo de login. | Importante |

## Requisitos Não Funcionais (RNF)

Abaixo estão os requisitos não funcionais, feitos de forma individual, os quais descrevem as características esperadas para o funcionamento do sistema, com base nos requisitos funcionais definidos:

| **Identificador** | **Requisito Funcional Associado** | **Descrição** | **Métrica** |
|-------------------|-----------------------------------|---------------|-------------|
| RNF01 | RF01 | O sistema deve identificar fissuras com acurácia mínima de 80%. | Acurácia ≥ 80% |
| RNF02 | RF01 | O sistema deve apresentar taxa de falso positivo inferior a 10%. | Falsos positivos ≤ 10% |
| RNF03 | RF01 | O sistema deve apresentar taxa de falso negativo inferior a 5%. | Falsos negativos ≤ 5% |
| RNF04 | RF02 | O sistema deve suportar o upload de arquivos com tamanho máximo de 100MB. | Tamanho máximo do arquivo ≤ 100MB |
| RNF05 | RF03 | O sistema deve identificar as fissuras em até 10 segundos por imagem. | Tempo de processamento ≤ 10 segundos |
| RNF06 | RF04 | O sistema deve armazenar o histórico de expedições por pelo menos 1 ano. | Armazenamento ≥ 1 ano |
| RNF07 | RF06 | O sistema deve apresentar causas relacionadas às fissuras detectadas com acurácia mínima de 70%. | Acurácia ≥ 70% |
| RNF08 | RF07 | O sistema deve medir a espessura da fissura com precisão de até 1 mm. | Precisão ≤ 1 mm |
| RNF09 | RF08 | O sistema deve realizar login com tempo de resposta inferior a 5 segundos. | Tempo de resposta ≤ 5 segundos |
