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

| **Identificador** | **Requisito Funcional Associado** | **Descrição** | **Métrica** | **Método de Teste** |
|-------------------|-----------------------------------|---------------|-------------|---------------------|
| RNF01 | RF01 | O sistema deve identificar fissuras com acurácia mínima de 80%. | Acurácia ≥ 80% | Realizar um conjunto de testes com imagens de fissuras conhecidas, mínimo de 30 imagens, e comparar os resultados com a classificação manual.|
| RNF02 | RF01 | O sistema deve apresentar taxa de falso positivo inferior a 10%. | Falsos positivos ≤ 10% | Utilizar um conjunto de imagens que contenham falhas inexistentes ou não-fissuras, mínimo de 20 imagens. Contabilizar o número de vezes que o sistema erroneamente classifica uma área como fissura.|
| RNF03 | RF01 | O sistema deve apresentar taxa de falso negativo inferior a 5%. | Falsos negativos ≤ 5% | Testar com um conjunto de imagens contendo fissuras de diferentes tipos e severidades. Calcular o número de fissuras que o sistema não identificou corretamente, minimo de 25 imagens. |
| RNF04 | RF02 | O sistema deve suportar o upload de arquivos com tamanho máximo de 100MB. | Tamanho máximo do arquivo ≤ 100MB | Realizar o teste de upload de arquivos com diferentes tamanhos, variando de 1MB a 100MB e arquivos de 101MB ou mais. O sistema deve aceitar arquivos de até 100MB e rejeitar arquivos acima deste tamanho. |
| RNF05 | RF03 | O sistema deve identificar as fissuras em até 10 segundos por imagem. | Tempo de processamento ≤ 10 segundos | Submeter ao sistema 50 imagens e medir o tempo total de processamento para cada imagem. O tempo total de processamento de cada imagem deve ser inferior ou igual a 10 segundos. Utilizar ferramentas de monitoramento de desempenho para capturar o tempo de processamento. |
| RNF06 | RF04 | O sistema deve armazenar o histórico de expedições por pelo menos 1 ano. | Armazenamento ≥ 1 ano | Realizar o teste de armazenamento de dados por um período superior a 1 ano, simulando uma expedição por dia. Verificar se o histórico está acessível após esse período e garantir que os dados não foram corrompidos ou apagados. |
| RNF07 | RF06 | O sistema deve apresentar causas relacionadas às fissuras detectadas com acurácia mínima de 70%. | Acurácia ≥ 70% | Realizar testes com um conjunto de imagens que contenham fissuras com causas previamente conhecidas. O sistema deve relacionar as fissuras com as causas corretas em pelo menos 70% dos casos. |
| RNF08 | RF07 | O sistema deve medir a espessura da fissura com precisão de até 1 mm. | Precisão ≤ 1 mm | Submeter o sistema a uma série de imagens de fissuras de espessura conhecida. A discrepância entre a espessura detectada pelo sistema e a espessura real deve ser de no máximo 1mm. Realizar a medição e calcular a margem de erro. |
| RNF09 | RF08 | O sistema deve realizar login com tempo de resposta inferior a 5 segundos. | Tempo de resposta ≤ 5 segundos | Testar o tempo de resposta do sistema durante o processo de login. Medir o tempo desde o início do login até a autenticação bem-sucedida usando ferramentas de monitoramento de desempenho. O tempo de resposta deve ser inferior a 5 segundos. |
