```C#
using System;
using System.Runtime.CompilerServices;

namespace ConsoleApp0
{
    class Program
    {
        static void Main(string[] args)
        {
            int num1;
            int num2;
            
            while (true)
            {
                Console.Write("Enter num1: ");
                num1 = Convert.ToInt32(Console.ReadLine());
                Console.Write("Enter num2: ");
                num2 = Convert.ToInt32(Console.ReadLine());
                

                if ( num1 < 0 || num1 > 10 || num2 < 0 || num2 > 10)
                {
                    Console.WriteLine("Invalid data");
                }
                else
                {
                    Console.Write($"{num1} * {num2} = {num1 * num2}");
                    break;
                }
            }
            Console.ReadKey();
        }
    }
}
```
