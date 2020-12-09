# OwOifier
An OwOifier programmed in dotnet core 3.1 for all of your OwOifying needs :3

# Implementation
Just create a new dotnet console project and replace the default `Program.cs` code with this:
```cs
using System;
using System.Text;

namespace owoify
{
    class Program
    {
        static void Main(string[] args)
        {
            string Input = string.Join(" ", args);

            string NewText = string.Empty;
            var Builder = new StringBuilder();

            foreach (char c in Input)
            {
                if (c == 'l' || c == 'r')
                    Builder.Append("w");
                else if (c == 'L' || c == 'R')
                    Builder.Append('W');
                else if (c == 'y' || c == 'Y')
                    Builder.Append("Wy");
                else if (c == 'u' || c == 'U')
                    Builder.Append("Wu");
                else if (char.IsWhiteSpace(c))
                    Builder.Append(" ");
                else
                    Builder.Append($"{c}");
            }

            NewText = Builder.ToString();

            Console.WriteLine("");

            Console.WriteLine("This is your OwOified text:");

            Console.WriteLine("----");

            Console.WriteLine(NewText);

            Console.WriteLine("----");

            Console.WriteLine("");
        }
    }
}
```

# Compilation
Now just run and compile the project, and in a shell, run the project with passing a string as a parameter, for example, on Windows, run `./owoify.exe "this is my super cool text!"`.


Enjoy OwO
