

### Bootstrap Template

Open nuget package console and adding the following:
Install-Package Microsoft.VisualStudio.Web.CodeGenerators.Mvc -Version 3.1.1

Or from the command line:
dotnet add package Microsoft.VisualStudio.Web.CodeGenerators.Mvc --version 3.1.1

Update Program.cs

``` csharp
    public class Program
    {
        public static void Main(string[] args)
        {
            var dirName = Directory.GetCurrentDirectory();
            var host = new WebHostBuilder()
                .UseContentRoot(dirName)
                .UseWebRoot("wwwroot")
                .UseIIS()
                .UseStartup<Startup>()
                .Build();

            host.Run();
        }
    }
```
