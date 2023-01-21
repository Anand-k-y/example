using System.Globalization;
using System.Numerics;
using System.Runtime.Intrinsics.X86;
using System.Runtime.Serialization.Formatters;
using System.Text;
using System.Transactions;

class Myclass
{
    public static void Main(string[] args)
    {
        Console.WriteLine("Enter Rows: ");
        int row = int.Parse(Console.ReadLine());
        Console.WriteLine("Enter Columns: ");
        int col = int.Parse(Console.ReadLine());
        int[,] a = new int[row, col];
        int[] prime = new int[row*col];
        int c=0;
        int n=2;
        do
        {
            
            
           int count = 0;
            for (int i = 2; i <= (n / 2); i++)
            {
                if (n % i == 0)
                {
                    count++;
                }
            }
            if (count == 0 && n != 1)
            {
                prime[c] = n;
                c++;
            }
            n++;
        } while (c!=a.Length);
        int k = 0;
        for(int i=0;i<row;i++)
        {
            for(int j=0;j<col;j++)
            {
                a[i,j] = prime[k];
                k++;
            }
        }

        for (int i = 0; i < row; i++)
        {
            for (int j = 0; j < col; j++)
            {
                Console.Write(a[i,j]+"\t");
            }
            Console.WriteLine();
        }

    }
       
}


