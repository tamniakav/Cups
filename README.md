using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam_2
{
    class Program
    {
        static void Main(string[] args)
        {
            double cupsNeeded = double.Parse(Console.ReadLine());
            int workers = int.Parse(Console.ReadLine());
            int days = int.Parse(Console.ReadLine());

            int workingHours = workers * days * 8;
            double cups = workingHours / 5;
            cups = Math.Floor(cups);

            if (cups >= cupsNeeded)
            {
                cups -= cupsNeeded;
                double profit = cups * 4.2;
                Console.WriteLine("{0:f2} extra money", profit);
            }
            else
            {
                cupsNeeded -= cups;
                double loss = cupsNeeded * 4.2;
                Console.WriteLine("Losses: {0:f2}", loss);
            }
        }
    }
}
