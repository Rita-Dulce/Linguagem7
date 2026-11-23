
using System;

class Program
{
    static void Main()
    {
        string[] nomes;
        decimal[] compras;
        decimal[] descontos;
        decimal[] totais;
        bool[] prioridade;

        int quantidade;

        Console.WriteLine("SISTEMA DE FATURACAO");

        Console.Write("Quantidade de clientes: ");
        quantidade = int.Parse(Console.ReadLine());

        nomes = new string[quantidade];
        compras = new decimal[quantidade];
        descontos = new decimal[quantidade];
        totais = new decimal[quantidade];
        prioridade = new bool[quantidade];

        // Registar os clientes
        for (int i = 0; i < quantidade; i++)
        {
            Console.WriteLine("\nCLIENTE " + (i + 1));

            Console.Write("Nome: ");
            nomes[i] = Console.ReadLine();

            Console.Write("Genero: ");
            string genero = Console.ReadLine();

            Console.Write("Valor das compras: ");
            compras[i] = decimal.Parse(Console.ReadLine());

            Console.Write("E gravida? (S/N): ");
            string gravida = Console.ReadLine().ToUpper();

            Console.Write("E idoso? (S/N): ");
            string idoso = Console.ReadLine().ToUpper();

            Console.Write("Tem deficiencia? (S/N): ");
            string deficiencia = Console.ReadLine().ToUpper();

            // Calcular desconto
            descontos[i] = 0;

            if (compras[i] > 100000)
            {
                descontos[i] = compras[i] * 0.10m;
            }

            totais[i] = compras[i] - descontos[i];

            // Verificar prioridade
            prioridade[i] = false;

            if (gravida == "S" || idoso == "S" ||
                deficiencia == "S")
            {
                prioridade[i] = true;
            }

            // Apresentar fatura
            Console.WriteLine("\n--- FATURA ---");
            Console.WriteLine("Cliente: " + nomes[i]);
            Console.WriteLine("Compras: " + compras[i] + " Kz");
            Console.WriteLine("Desconto: " + descontos[i] + " Kz");
            Console.WriteLine("Total a pagar: " + totais[i] + " Kz");
        }

        // Organizar atendimento
        Console.WriteLine("\nORDEM DE ATENDIMENTO");

        // Primeiro os clientes prioritarios
        for (int i = 0; i < quantidade; i++)
        {
            if (prioridade[i] == true)
            {
                Console.WriteLine(nomes[i] + " - Prioridade");
            }
        }

        // Depois os clientes normais
        for (int i = 0; i < quantidade; i++)
        {
            if (prioridade[i] == false)
            {
                Console.WriteLine(nomes[i] + " - Normal");
            }
        }

        Console.WriteLine("\nFim do programa.");
    }
}
