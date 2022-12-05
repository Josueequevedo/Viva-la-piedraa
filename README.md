namespace Viva_la_piedra
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Random Compu = new Random();
            int benigod = 1, turno;
            string Tiro, Maquina;
            string[] jugadas = { "Piedra", "Papel", "Tijeras" };
            while (benigod == 1)
            {
                Console.WriteLine("Beni por favor elije:\n1.-Piedra\n2.-Papel\n3.-Tijeras");
                turno = int.Parse(Console.ReadLine());
                Tiro = jugadas[turno - 1];
                Maquina = jugadas[Compu.Next(0, 2)];
                Console.Clear();
                if ((Tiro == "Piedra") && (Maquina == "Tijeras"))

                    Console.Write("Awebo Beni, Ganaste!!, la maquina saco___" + Maquina + "\n");
          
                else if ((Tiro == "Papel") && (Maquina == "Piedra"))

                    Console.Write("Awebo Beni, Ganaste!!,la maquina saco___" + Maquina + "\n");
                
                else if ((Tiro == "Tijeras") && (Maquina == "Papel"))

                    Console.Write("Awebo Beni, Ganaste!!" + Maquina + "\n");

                if ((Maquina == "Piedra") && (Tiro == "Tijeras"))

                    Console.Write("Yyyy te chingo la maquina, ella tiro___" + Maquina + "\n");

                else if ((Maquina == "Papel") && (Tiro == "Piedra"))

                    Console.Write("Yyyy te chingo la maquina, ella tiro___" + Maquina + "\n");

                else if ((Maquina == "Tijeras") && (Tiro == "Papel")) ;

                if (((Maquina == "Piedra") && (Tiro == "Piedra")) || ((Maquina == "Papel") && (Tiro == "Papel"))

                    || ((Maquina == "Tijeras") && (Tiro == "Tijeras")))

                    Console.WriteLine("Se dieron al chile, pero quedo en empate\n");

                Console.WriteLine("\nQuieres continuar Beni?______ 1:Si o 0: No");

                benigod = int.Parse(Console.ReadLine());
            }
            Console.ReadKey();
        }
    }
}
