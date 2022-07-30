# Calculadora-C-
Calculadora C#


namespace Calculadora
{
    internal class Programa
    {
        private static void Main(string[] args)
        {
            menu();
        }

        static void menu()
        {
            Console.Clear();

            Console.WriteLine("-----------------------------------------");
            Console.WriteLine("Qual a operação que você deseja realizar?");
            Console.WriteLine("");
            Console.WriteLine("1 - Soma");
            Console.WriteLine("2 - Subtração");
            Console.WriteLine("3 - Multiplicação");
            Console.WriteLine("4 - Divisão");
            Console.WriteLine("5 - Sair");
            Console.WriteLine("");
            Console.WriteLine("-----------------------------------------");

            short escolha = short.Parse(Console.ReadLine());

            switch (escolha)
            {
                case 1: soma(); break;
                case 2: subtrair(); break;
                case 3: multiplicacao(); break;
                case 4: divisao(); break;
                case 5: System.Environment.Exit(0); break;
                default: menu(); break;
            }


        }
        static void soma()
        {
            Console.Clear();
            Console.WriteLine("Primeiro valor: ");
            float v1 = float.Parse(Console.ReadLine());

            Console.WriteLine("Segundo valor");
            float v2 = float.Parse(Console.ReadLine());

            Console.WriteLine("");

            float resultado = v1 + v2;
            Console.WriteLine("O resultado da soma entre o primeiro e segundo valor é: " + resultado);
            // Console.WriteLine($"O resultado da soma entre o primeiro e segundo numero é {resultado}");
            // Console.WriteLine("O resultado da soma entre o primeiro e segundo numero é: " + (v1 + v2));
            // Console.WriteLine($"O resultado da soma entre o primeiro e segundo numero é {v1 + v2}");
            Console.ReadKey();
            menu();
        }
        static void subtrair()
        {
            Console.Clear();

            Console.WriteLine("Digite o priemiro valor:");
            float v1 = float.Parse(Console.ReadLine());


            Console.WriteLine("Digite o segundo valor:");
            float v2 = float.Parse(Console.ReadLine());

            Console.WriteLine("");

            float resultada = v1 - v2;
            Console.WriteLine("O resultada da subtração entre os dois numeros é: " + (v1 - v2));
            Console.ReadKey();
            menu();
        }
        static void multiplicacao()
        {
            Console.Clear();

            Console.WriteLine("Digite o primeiro valor: ");
            float v1 = float.Parse(Console.ReadLine());

            Console.WriteLine("Valor multiplicador: ");
            float v2 = float.Parse(Console.ReadLine());

            Console.WriteLine("");

            float resultado = v2 * v1;
            Console.WriteLine("O resultado da multiplicação é: " + resultado);
            Console.ReadKey();
            menu();

        }
        static void divisao()
        {
            Console.Clear();

            Console.WriteLine("Digite o primeiro valor:");
            float v1 = float.Parse(Console.ReadLine());

            Console.WriteLine("Digite o segundo valor:");
            float v2 = float.Parse(Console.ReadLine());

            Console.WriteLine("");

            float resultado = v1 / v2;
            Console.WriteLine("O resultado da divisão é: " + resultado);
            Console.ReadKey();
            menu();

        }
    }
}
