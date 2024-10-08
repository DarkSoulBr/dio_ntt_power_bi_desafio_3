
<h2 align="center">
  Criação de Relatório corporativo com integração com MySQL e Azure
</h2>

Este é um desafio da formação NTT DATA - Engenharia de Dados com Python

# Descritivo do Desafio

Neste desafio será a sua vez de aplicar as etapas de coleta, obtenção e transformação de dados com Power BI e MySQL na Azure. 

# Tecnologias utilizadas

  - Power BI
  - MySQL
  - Git

# Detalhamento do Desafio

Descrição do desafio módulo 3 – Processamento de Dados Simplificado com Power BI

1. Criação de uma instância na Azure para MySQL  
    OK

2. Criar o Banco de dados com base disponível no github  
    Houveram alguns problemas ao inserir os dados, mas foram resolvidos ao inverter a ordem dos registros. 

3. Integração do Power BI com MySQL no Azure  
    Houveram alguns problemas na conexão que foram resolvidos com a atulização do Driver do MySQL

4. Verificar problemas na base a fim de realizar a transformação dos dados  
    Segue descrição abaixo.

Diretrizes para transformação dos dados

1. Verifique os cabeçalhos e tipos de dados  
    Fiz a Exclusão de campos dos tipos Table e Value de todas as tabelas

2. Modifique os valores monetários para o tipo double preciso  
    Alterei o campo Salary da tabela employee para decimal fixo

3. Verifique a existência dos nulos e analise a remoção  
    Encontrei apenas 1 campo nulo na coluna Super_ssn da tabela Employee como ele era um supervisor conclusão deixei a coluna como 0

4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente  
    Não existe nenhum colaborador sem gerente

5. Verifique se há algum departamento sem gerente  
    Não havia nenhum departamento sem gerentes

6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas  
    Não havia nenhum departamento sem gerentes

7. Verifique o número de horas dos projetos  
    Verifiquei as horas de projetos e não encontrei nada de anormal

8. Separar colunas complexas  
    Fiz a separação do campo Address em Number, street, City e State Ums das linhas tive que ajustar pois dividiu em 5 colunas

9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção  
    Criei uma mescla das tabelas employee e departament numa nova tabela chamada employee_departament que tem todas as colunas de employee mais a coluna com o nome do departamento

10. Neste processo elimine as colunas desnecessárias.  
    Eliminei as colunas do departamento menos o nome 

11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.  
    Fiz a Mescla criando uma nota consulta com uma coluna a mais com o nome e sobrenome do supervisor

12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores  
    Fiz a mescla das Colunas Nome e Sobrenome

13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.  
    Fiz a mescla das tabelas dept_locations e departaments

14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.  
    Foi utilizado a mescla porque o objetivo era combinar as colunas de tabelas diferentes.

15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente  
    Foi feito e incluído em um gráfico no relatório

16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela  
    Excluídas
    