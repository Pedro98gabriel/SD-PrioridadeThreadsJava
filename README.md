# SD-PrioridadeThreadsJava

## Análise da execução:
O código ``LancadorPrioridade.java`` cria e executa duas threads em Java: uma de alta prioridade, que imprime 5 mensagens com um pequeno atraso entre elas, e outra de baixa prioridade, que imprime mensagens continuamente, sem pausa. Ambas são iniciadas no método main(). O programa simula a execução concorrente das threads por um período definido e, ao final, gera um log com os resultados dessa execução.


## Passos para execução:
- Compile o arquivo LancadorPrioridade.java
  - `` javac LancadorPrioridade.java ``
  
- Digite o seguinte comando no terminal:
  - ``java LancadorPrioridade > LancadorPrioridade_$(date +%Y%m%d_%H%M%S).log &``
  - Isso executa o programa em segundo plano e salva as mensagens de saída no arquivo de log gerado com um timestamp único.
  


## Analise do log:
No log gerado pela execução, é possível observar a alternância entre as mensagens das duas threads. Cada thread imprime suas mensagens conforme sua prioridade. Devido ao uso do sleep(10) na thread de alta prioridade, ela tende a ser executada menos vezes, já que fica "dormindo". 


## Considerações finais:
O código mostra como o gerenciamento de prioridades e o comportamento do escalonador de threads em Java podem influenciar a execução das threads. Mesmo com prioridades diferentes, o tempo de execução de cada thread pode ser impactado por coisas como o sleep() ou até mesmo pela forma como o sistema decide qual thread deve rodar, o que nem sempre faz com que as threads de maior prioridade sejam executadas mais vezes.