# FunPlayMovie
Aplicação desenvolvida com back-end em C#, e front-end desenvolvido em asp.net, HTML, CSS e Javscript

Diagrama de banco de dados feito no SQL Management Studio 18, aplicação desenvolvida em Visual Studio 2012 > ASPNET MVC 4 Web Application em .Net 4.5

Requisitos:
Visual Studio 2012 ou superior

Microsoft SQLServer 2008 ou superior (ou algum outro gerenciador de banco de dados que permita atachar base de dados em formato .mdf

Net framework 4.5 ou superior

ASP e Asp.net ativados nos recursos adicionais do Windows

Instalação (validação do sistema)
1 - Atachar a base de dados "FunPlayMovie.mdf", localizado na pasta Databases em uma instância do SQLServer (no meu caso é (localdb)\Projects e estou usando autenticação do Windows para conexão com o SQL). Observação, o arquivo "FunPlayMovie_log.ldf" precisa ser mantido no mesmo diretório no momento de atachar. 

2 - Abrir no Visual Studio o arquivo "FunPlayMovie.sln" localizado na pasta "FunPlayMovie"

3 - Com a solução aberta no visualStudio expandir o Projeto "FunPlayMovie" e localizar e abrir para editar o arquivo "Web.config". Agora será inserido o caminho do banco de dados para que a aplicação possa fazer as consultas e alterações desejadas.
Na tag "<connectionString>" inserir a instancia do SQLServer onde foi atachada a base:
<connectionString><add name="DefaultConnection" connectionString="data source=Caminho Sua Instância; initial catalog=Nome do banco de dados;Integrated Security=True" providerName="System.Data.SqlClient" /></connectionString>
No meu caso: <add name="DefaultConnection" connectionString="Data Source=(LocalDb)\v11.0;Initial Catalog=aspnet-FunPlayMovie-20211205233130;Integrated Security=SSPI;AttachDBFilename=|DataDirectory|\aspnet-FunPlayMovie-20211205233130.mdf" providerName="System.Data.SqlClient" />
Sendo que a instância é "(LocalDb)\" e o banco de dados "aspnet-FunPlayMovie-20211205233130" (está utilizando o cache)
  
4 - Após ajustar a conexão é possível abrir a aplicação utilizando "CTRL + F5" ou somente "F5"
  
5 - Será necessário criar um login na aba superior "Cadastrar-se" e em seguida logar para utilizar o cadastro de Filmes e Sessões.
  
Observação: no meu caso eu utilizo o endereço "http://localhost:49914/" no navegador pois não foi setado um domínio para a aplicação.  
  
  
  
