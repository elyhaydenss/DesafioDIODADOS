# Descrição do desafio módulo 3 – Processamento de Dados Simplificado com Power BI

1. **Criação de uma instância na Azure para MySQL**
   - Não foi possível tal instância no Azure, executei localmente.

2. **Criar o Banco de dados com base disponível no GitHub**
   - Diversas queries estavam com os códigos falhando, tive que adaptar. Além disso, algumas constraints estavam erradas, então as removi e inseri os dados.

### Diretrizes para transformação dos dados

1. Verifique os cabeçalhos e tipos de dados.
   - Certifiquei-me de que todos tinham nomes.

2. Modifique os valores monetários para o tipo double preciso.
   - Valor alterado já com as casas decimais.

3. Verifique a existência dos nulos e analise a remoção.
   - Apenas o supervisor geral, como não tem ninguém acima dele, não tem gerente.

4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente.
   - Como dito anteriormente, apenas o James Borg não tem gerente.

5. Verifique se há algum departamento sem gerente.
   - Não existe.

6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas.
   - Já efetuado.

7. Verifique o número de horas dos projetos.
   - Existe um projeto com zero horas, mas ele terá que ser discutido futuramente.

8. Separar colunas complexas.
   - Coluna de endereço separada em número, cidade e estado.

9. Mesclar consultas employee e departamento para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção.
   - Feita a mesclagem das tabelas e efetuada a exclusão das colunas desnecessárias.

   Neste processo, elimine as colunas desnecessárias.

10. Realize a junção dos colaboradores e respectivos nomes dos gerentes. Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.
    - Foi mesclada as colunas SSN e Super_ssn em uma coluna com nome de "employee_gerente".

11. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores.
    - Coluna "nome completo" criada.

12. Mescle os nomes de departamentos e localização. Isso fará com que cada combinação departamento-local seja única. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.
    - Criada a tabela "mesclado_departamento_e_local".

13. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.
    - No caso, usamos mesclar para ter a relação entre departamento e local.
