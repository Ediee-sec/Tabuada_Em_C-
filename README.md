## Programa de Tabuada

> **Programa escrito em C# que retorna a tabuada com base na entrada de dados do usuário.**

* **Mapa do Código**

~~~c#
using System;

namespace Tab
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int j;

            // Interação no numero maximo que um usuário pode consultar as tabuadas
            for (j = 1; j <= 3; j++)
            {
                int Numero;
                int Cont = 0;

                // Tratamento de erros
                try
                {
                    // Entrada de dados do usuário
                    Console.Write("Qual Tabuada Deseja Consultar: ");
                    Numero = int.Parse(Console.ReadLine());

                    // Loop enquanto a variavel Cont for menor ou igual a 10
                    while (Cont <= 10)
                    {
                        // Exibe o retorno da tabuada na tela
                        Console.WriteLine(Math.Abs(Numero) + " X " + Cont + " = " + Tabuada(Numero, Cont));
                        Cont++; // Incremento a variavel
                    }
                }
                // Se houver erro
                catch (Exception)
                { Console.WriteLine("É permitido apenas números"); }

                if(j == 3)
                { Console.WriteLine("\n\nVocê já realizou o maximo de operações"); }       
            }
          
        }

        //Funcao que realiza o calculo da tabuada
        static int Tabuada(int a,int b)
        {
            int resultado = Math.Abs(a * b);
            return resultado;
        }
    }
}
~~~
<img src = img/img.png>