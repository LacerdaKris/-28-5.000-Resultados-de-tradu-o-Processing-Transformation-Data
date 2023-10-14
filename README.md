#Desafio Bootcamp DIO – Processamento de Dados com Power BI

1. Criação de uma instância na Azure para MySQL: desafio-projeto-bootcamp
2. Criar o Banco de dados com script base disponível no github:

    Comando p/ conectar ao banco sql pelo cloud shell...
    mysql -h desafio-projeto-bootcamp.mysql.database.azure.com -u lacerdakris -p;
    use azure_company;
    demais comandos de query do mysql...
   ![image](https://github.com/LacerdaKris/-28-5.000-Resultados-de-tradu-o-Processing-Transformation-Data/assets/107269748/2441b797-43b3-42af-b9c2-653d70ed6151)

4. Integração do Power BI com MySQL no Azure
5. Verificar problemas na base a fim de realizar a transformação dos dados
 ![image](https://github.com/LacerdaKris/-28-5.000-Resultados-de-tradu-o-Processing-Transformation-Data/assets/107269748/2b6db8e5-0742-4b88-a1a9-6a190dfa16d7)


Diretrizes para transformação dos dados

1. Verifique os cabeçalhos e tipos de dados
2. Modifique os valores monetários para o tipo double preciso
3. Verifique a existência dos nulos e analise a remoção
4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente
5. Verifique se há algum departamento sem gerente
6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas
7. Verifique o número de horas dos projetos
8. Separar colunas complexas
9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção
10. Neste processo elimine as colunas desnecessárias.
11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Feito com mescla de tabelas do Power BI.
12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores
Utilizado este comando em “criar nova coluna personalizada”: [First Name] & " " & [Last Name]
13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.
14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.                                                                                       

     O mesclar combina as tabelas com base em uma coluna de junção (como o comando join no SQL), neste caso a atribuição não seria útil em
     juntar as informações de duas colunas de tabelas diferentes, só se o objetivo fosse empilhar tabelas verticalmente (ou seja,
     adicionar mais linhas na tabela indiferente das colunas, o que é útil ao incluir mais dados que advém da mesma estrutura de colunas).
15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente
 ![image](https://github.com/LacerdaKris/-28-5.000-Resultados-de-tradu-o-Processing-Transformation-Data/assets/107269748/da1a524f-2e46-4793-a850-92f218f1e18a)

16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela
