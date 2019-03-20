# ch6-case1
# drew and miranda
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using static System.Console;
namespace GreenvilleRevenue
{
    class Program
    {
        static void Main(string[] args)
        {
            string ThisYear;
            int This_Number1;
            string LastYear;
            int This_Number2;
            int fee;
            int total_revenue;
            string inputString = "";
            int totalContest = 0;
            int dance = 0;
            int sing = 0;
            int musical = 0;
            int other = 0;
            int number;
            string letter;
            
            Write("The amount of contestants in last years competition: ");
            LastYear = ReadLine();
            Write("The amount of contestants in this years competition: ");
            ThisYear = ReadLine();
            fee = 25;
            This_Number1 = Convert.ToInt16(ThisYear);
            This_Number2 = Convert.ToInt16(LastYear);
            total_revenue = fee * This_Number1;
            
            while (totalContest < This_Number1)
            {
                Write("How many contestants: ");
                number = Convert.ToInt32(ReadLine());
                Write("Dance, Sing, Musical, or Other: ");
                letter = Convert.ToString(ReadLine());
                if (letter == "d" || letter == "D")
                {
                    dance += number;
                    totalContest += number;
                    number = 0;
                }
                else if (letter == "s" || letter == "S")
                {
                    sing += number;
                    totalContest += number;
                    number = 0;
                }
                else if (letter == "m" || letter == "M")
                {
                    musical += number;
                    totalContest += number;
                    number = 0;

                }
                else if (letter == "o" || letter == "O")
                {
                    other += number;
                    totalContest += number;
                    number = 0;
                }
            }
            WriteLine("number of contestants for dance: {0}", dance);
            WriteLine("number of contestants for singing: {0}", sing);
            WriteLine("number of contestants for musical: {0}", musical);
            WriteLine("number of contestants for other: {0}", other);
            if (This_Number1 > This_Number2)
                {
                WriteLine("This year has more contestants than last year.");
                }
            else
                {
                WriteLine("Last year had more contestants than this year.");
            }
        }
    }
}
