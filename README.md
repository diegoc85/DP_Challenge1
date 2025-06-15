# SimplIA – Laboratório DASA 

- GRUPO:
    - DIEGO CABRAL - RM 557817
    - DÉBORA IVANOWSKI - RM 555694
    - ARNALDO FILHO - RM 555780
    - PEDRO OLIVEIRA - RM 99943

## Descrição do Projeto  
Este código implementa um pequeno sistema de cadastro e a busca de exames patológicos realizados pelos pacientes, simulando a medição de tecidos nos laboratórios da DASA. Os dados de 12 pacientes (há repetições) já vêm armazenados em dicionários, cada um com valor da medição, intervalo de referência (max e min) e o resultado (“normal” ou “fora do intervalo”). O usuário do sistema interage por menu de texto, listando todos os exames dos pacientes ou buscando apenas pelo **nome** do paciente usando ordenação por **Insertion Sort** e pesquisa por **Busca Binária**.

## Estrutura do Código

1. **Dados de Exames**  
   Uma lista de dicionários do Python chamada `exames` com os seguinte campos abaixo:  
   - `nome`, `sobrenome`, `data`  
   - `medicao`, `ref_min`, `ref_max`  
   - `resultado` (ele é calculado automaticamente)  

2. **Cálculo do Resultado de acordo com a comparação da medição com os dados dos valores de referência**  
   
   for e in exames:
       if e['medicao'] >= e['ref_min'] and e['medicao'] <= e['ref_max']:
           e['resultado'] = 'normal'
       else:
           e['resultado'] = 'fora do intervalo'

    - Esse for é uma iteração sobre cada exame dentro do dicionário `exames` e verifica se a medição realizada está dentro ou fora do intervalo de referência (ref_min e ref_max).

3. **Algoritmos Auxiliares** 
- Insertion Sort: é ideal para listas pequenas como o do código desenvolvido e quase já ordenadas.
- Busca binária

4. **Função do Menu**
- listar(): imprime todos os exames na tela.
- buscar(nome):
    - Ordena exames por nome.
    - Executa busca binária para encontrar a primeira ocorrência.
    - Varre as posições para coletar todos os exames com aquele nome.
    - Ordena os resultados e exibe um novo dicionário enumerado.

5. **Dependências**
- Python 3 (nenhuma biblioteca externa é necessária)
6. **Instruções de Uso**
- a) Abra um Jupyter Notebook ou qualquer console Python.
- b) Copie e cole todo o código em uma célula ou arquivo .py.
- c) Execute o código.
    - Quando aparecer o menu, escolha uma das opções abaixo:
    - 1) para listar todos os exames
    - 2) para buscar por nome (ex.: “Ana”, “Bruno”…)
    - 3) para encerrar

7. **Referências e Notas**
- Este é apenas ume exemplo e serve como base para um sistema maior e com mais funcionalidades, podendo ser estendido com Visão Computacional, Machine Learning, interface gráfica e integração com banco de dados.

