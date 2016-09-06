# pagseguro-aspnetcore
Uma implementação da biblioteca do PagSeguro para .Net (https://github.com/pagseguro/dotnet) portada para .net core.

Como utilizar
========

Adicione o arquivo "PagSeguroConfig.xml" na raiz da sua aplicação, configure suas credenciais, e na inicialização da dua aplicação aspnetcore inclua os seguintes comandos:

```cs
public class Startup
{
    public void Configure(IApplicationBuilder app, IHostingEnvironment env, ILoggerFactory loggerFactory)
    {
      //...
      
      //Configuracao do PagSeguro de acordo com o ambiente em uso
      PagSeguroConfiguration.UrlXmlConfiguration = System.IO.Path.Combine(env.ContentRootPath, "PagSeguroConfig.xml");
      EnvironmentConfiguration.ChangeEnvironment(env.IsDevelopment());
    }
}
```
