```C#
using System;

namespace ConsoleApp0
{
    class Program
    {
        static void Main(string[] args)
        {
            int[] nums = new int[10];
            for (int i = 1; i < nums.Length; i++)
                nums[i] = i;

            for (int i = 1; i < nums.Length; i++)
            {
                for (int j = 1; j < nums.Length; j++) { }
                Console.WriteLine();
            }
        }
    }
}
```
