# Revisao-Projeto-EntreLinhas

### Revisão Geral e Exercícios:

Na aula de Hoje, Vamos Revisar tudo o que vimos até agorá


 * Variaveis

 * Operadores

 * Entrada e Saída de dados

 * Estruturas condicionais

 * Estruturas de repetição


------------------------------------------------------------------

Você se lembra de todas essas estruturas? porque hoje você vai precisar de todas elas! 

Reservamos 5 Exercícios onde vocês vão aplicar tudo o que foi ensinado até o momento.


# Exercício de Numero 1 (IMC)

O IMC (Índice de Massa Corporal) é calculado com a seguinte formula:
            IMC = peso/(altura * altura)
            Crie um programa que receba o peso e a altura do usuário, calcule o IMC e mostre sua classificação conforme a tabela abaixo:
            IMC em adultos Classificação
            Abaixo de 18,5 Abaixo do peso
            Entre 18,5 e 24,9 Peso normal
            Entre 25,0 e 29,9 Acima do peso
            Maior que 30,0 Obeso
     
     namespace Aula_06
     {
         public class Exercicio_01
         {
             public static void Executar()
             {


            double peso, altura;
            Console.Write("Digite seu peso (kg): ");
            peso = double.Parse(Console.ReadLine());
            Console.Write("Digite sua altura (m): ");
            altura = double.Parse(Console.ReadLine());


            //esta faltando uma variavel para armazenar o valor, e a conta esta incompleta. declare ela e complete a conta.


            = peso / ();


            //Qual condicao precisa atender pra ele ser Abaixo do peso?
            if (imc)
            {
                Console.WriteLine("Seu IMC é {0:F2}. Classificação: Abaixo do peso.", imc);
            }
            //Qual condicao precisa atender pra ele ser Peso Normal?
            else if (imc && imc)
            {
                Console.WriteLine("Seu IMC é {0:F2}. Classificação: Peso normal.", imc);
            }
            //Qual condicao precisa atender pra ele ser Acima do Peso?
            else if (imc  && imc )
            {
                Console.WriteLine("Seu IMC é {0:F2}. Classificação: Acima do peso.", imc);
            }
            else
            {
                Console.WriteLine("Seu IMC é {0:F2}. Classificação: Obeso.", imc);
            }


        }


    }
    }

# Exercício de Numero 2 (ler numeros positivos, negativos e zeros)

Fazer um programa leia uma sequência de valores inteiros fornecida pelo usuário em uma
linha de entrada e conte o número de valores positivos, negativos e zeros
 
    using System.Security.AccessControl;
 
    namespace Aula_06
         {

 
    public class Exercicio_02
    {
        public static void Executar()
        {
            int quantidade;
            int countPositivos = 0;
            int countNegativos = 0;
            int countZeros = 0;
 
            //Qual variavel deve ser usada para armazenar a quantidade de numeros que o usuario quer inserir?
            Console.WriteLine("Digite a quantidade de numeros inteiros que voce deseja inserir:");
             = int.Parse(Console.ReadLine());
            //Digite a condicao para que o loop pare na hora certa  ( i < )
            for (int i = 0; i < ; i++)
            {
                Console.WriteLine("Digite o {0}º numero:", i + 1);
                int numero = int.Parse(Console.ReadLine());
 
                //Qual a condicao para que o algoritmo conte os positivos?
                if (numero)
                {
                    countPositivos++;
                }
                //Qual a condicao para que o algoritmo conte os negativos?
                else if (numero)
                {
                    countNegativos++;
                }
                else
                {
                    countZeros++;
                }
            }
            // Exiba os resultados
            Console.WriteLine("Quantidade de numeros positivos: " );
            Console.WriteLine("Quantidade de numeros negativos: " );
            Console.WriteLine("Quantidade de zeros: ");
       
 
        }
    }
    }

 # Exercício 3 (RPG)  

 Você é um guerreiro que precisa recuperar o tesouro em um calabouço
você se depara com um dragão enorme, e logo atraz dele, muitas moedas de ouro,
diamantes e rubys. O dragão se posiciona para iniciar o combate.

Regras do jogo:

A cada turno você escolhe uma ação para fazer

você pode atacar o dragão com a espada, causando 5 de dano no dragão
você pode defender, evitado metade do dano caso o dragão ataque
você pode usar um pergaminho de luz, que causa 40 de dano no dragão mas você possui 5 pergaminhos
você Pode prever um golpe e esquivar, evitando tomar dano do dragão caso ele ataque, porem se o dragão não atacar, você perde 2 de dano de ataque de sua espada
você pode meditar para aumentar o dano da sua espada em +5 permanentemente

o dragão toma uma iniciativa junto com você, ele pode escolher as seguintes ações

ele pode te atacar, causando 8 de dano
ele pode carregar uma bola de fogo, caso ele te acerte ele causa 20 de dano, caso ele erre, ele toma o dobro de dano permanentemente (pode ser aplicado inumeras vezes)
ele pode descançar para recuperar 10 de vida
ele pode ele pode se defender, evitando metade do dano 
ele tem uma pequena chance de fugir de medo (10% de chance)

A partir daqui a escolha é sua, tem coragem de enfrentar o dragão? 

     Console.WriteLine("DRAGON MANIA!");
     Console.WriteLine("");
     Console.WriteLine("Você ousa enfrentar o dragão feroz");

     // vida e ataques do jogador e dragão
     int suavida = 100, seudano = 5, vidadragao = 300, danodragao = 8;

     // multiplicado de dano no dragão
     int multiplicadorDanoDragao = 1;

     // ação do dragão (aleatoria)
     Random rnd = new Random();

     // ação do jogador
     string action = "";

     // mais ações
     int actiondragão, seuataque = 0, ataquedragao = 0, contadorpergaminho = 5, danopergaminho = 40;

     // ações do turno
     bool voceatacou = false, vocedefendeu = false, voceesquivou = false, voceMeditou = false;
     bool dragaoatacou = false, dragaodefendeu = false, dragaoCarregouFogo = false, dragaoFugiu = false;

     // sua ação inicial
     Console.WriteLine("digite 1 para enfrentar o dragão");
     Console.WriteLine("digite 2 fugir");
     
     // primeira escolha
     int escolhainicial = int.Parse(Console.ReadLine());

     // se for digitar 1 (enfrentar o dragão) iniciar a batalha
     if (escolhainicial == 1)
     {
         Console.WriteLine("Vá em frente guerreiro! enfrente o temivel dragão");
     }
     else // caso o contrario, o dragão evita sua fuga e te ataca 
     {
         Console.WriteLine("Neste momento, o dragão percebe que você não quer enfrenta-lo. Inconformado ele parte para cima, te atacando");
         Console.WriteLine("Você tomou 8 de dano");
         suavida -= danodragao;
     }
     
     // loop para a batalha
     do
     {
         // --- INÍCIO DO TURNO ---
         // Resetar todas as ações do turno anterior
         seuataque = 0;
         ataquedragao = 0;
         voceatacou = false;
         vocedefendeu = false;
         voceesquivou = false;
         voceMeditou = false;
         dragaoatacou = false;
         dragaodefendeu = false;
         dragaoCarregouFogo = false;
     
         Console.WriteLine("======================================");
         Console.WriteLine("Escolha sua ação:\n1 = Atacar com espada\n2 = Defender\n3 = Usar Pergaminho ({0} restantes)\n4 = Esquivar\nQualquer outra tecla = Meditar", contadorpergaminho);
         Console.WriteLine("--------------------------------------");
         Console.WriteLine("Status do Guerreiro: \nDano Espada = {0}\nVida = {1}", seudano, suavida);
         Console.WriteLine("--------------------------------------");
         Console.WriteLine("Status do Dragão: \nVida = {0}\n(Dano recebido atual: x{1})", vidadragao, multiplicadorDanoDragao);
         Console.WriteLine("======================================");

         // sua escolha
         action = Console.ReadLine();

         // escolha do dragão
         actiondragão = rnd.Next(1, 11);

         // --- AÇÃO DO JOGADOR ---
         switch (action)
         {
             case : // qual o primeiro caso? (formato de texto)
                 seuataque = seudano;
                 voceatacou = true;
                 Console.WriteLine("Você prepara sua ESPADA!");
                 break;
             case : // qual o segundo caso? (formato de texto)
            vocedefendeu = true;
            Console.WriteLine("Você se prepara para DEFENDER!");
            break;
        case "3": // Pergaminho
            if (contadorpergaminho) // o que precisa pra ele usar os pergaminhos?
            {
                seuataque = danopergaminho;
                voceatacou = true; 
                Console.WriteLine("Você usa um PERGAMINHO DE LUZ!");
                contadorpergaminho--;
            }
            else
            {
                Console.WriteLine("Sem pergaminhos! Você se DEFENDE por reflexo!");
                vocedefendeu = true;
            }
            break;
        case "4": // Esquivar
            voceesquivou = true;
            Console.WriteLine("Você tenta prever o golpe e ESQUIVAR!");
            break;
        default: // Meditar
            voceMeditou = true; // Usaremos essa flag
            Console.WriteLine("Você MEDITA para focar seu poder...");
            break;
    }

    // --- AÇÃO DO DRAGÃO ---
    // Agora 'Fugir' (case 5) só tem 1 chance em 10 (10%)
    switch (actiondragão)
    {
        case 1: 
        case 6: 
        case 7: 
            ataquedragao = danodragao;
            dragaoatacou = true;
            Console.WriteLine("O dragão te ATACA com suas garras!");
            break;
        case 2: 
        case 8: 
            ataquedragao = 20; 
            dragaoatacou = true;
            dragaoCarregouFogo = true; 
            Console.WriteLine("O dragão prepara uma BOLA DE FOGO!");
            break;
        case 3: 
        case 9:
            vidadragao += 10;
            Console.WriteLine("O dragão DESCANSA e recupera 10 de vida.");
            break;
        case 4: 
        case 10: 
            dragaodefendeu = true;
            Console.WriteLine("O dragão se encolhe para DEFENDER.");
            break;
        case 5: 
            dragaoFugiu = true;
            Console.WriteLine("O dragão se assusta e FOGE!");
            break;
    }
    Console.WriteLine("--- RESOLUÇÃO DO TURNO ---");

    // --- Lógica de Dano (JOGADOR CAUSA DANO) ---
    if (voceatacou == )// qual tipo de variavel de "voceatacou"? 
    {
        int danoRealCausado = seuataque * multiplicadorDanoDragao;
        if (== true)// qual ação deve ser aqui (dica, preste atenção no codigo dentro do bloco)
        {
            danoRealCausado /= 2;
            Console.WriteLine("O dragão defendeu! Você causou {0} de dano.", danoRealCausado);
        }
        else
        {
            Console.WriteLine("Você acertou! Você causou {0} de dano.", danoRealCausado);
        }
        vidadragao -= danoRealCausado;
    }

    // --- Lógica de Dano (DRAGÃO CAUSA DANO) ---
    if (dragaoatacou)
    {
        if (vocedefendeu == true)
        {
            ataquedragao /= 2;
            Console.WriteLine("Você defendeu! O dragão causou {0} de dano.", ataquedragao);
            suavida -= ataquedragao;
        }
        else if (voceesquivou == true)
        {
            Console.WriteLine("Você esquivou! O ataque do dragão falhou!");

            if (dragaoCarregouFogo == true)
            {
                Console.WriteLine("O dragão errou a bola de fogo e está vulnerável! Ele tomará o dobro de dano!");
                multiplicadorDanoDragao // qual o calculo deve ser aplicado caso o guerreiro esquive da bola de fogo do dragão
            }
        }
        else
        {
            // Se você meditou ou atacou, você toma o dano cheio
            Console.WriteLine("Você foi atingido! O dragão causou {0} de dano.", ataquedragao);
            suavida -= ataquedragao;
        }
    }

    // --- Lógica das Ações Especiais (Meditar / Penalidades) ---

    // REGRA ESPECIAL: Meditar
    if (voceMeditou == true)
    {
        seudano// o que acontece com seu dano caso você medite?
        Console.WriteLine("Sua meditação aumentou o dano da sua espada para {0}.", seudano);
    }

    // REGRA ESPECIAL: Penalidade da Esquiva
    if (voceesquivou && !dragaoatacou)
    {
        Console.WriteLine("Você tentou esquivar de um ataque que não veio! Sua espada perde 2 de dano.");
        seudano -= 2;
        if (seudano < 0) seudano = 0; // Não deixa o dano ficar negativo
    }


    // --- Checagem de Fim de Jogo ---
    if (dragaoFugiu)
    {
        // Força a saída do loop
        break;
    }

    Console.WriteLine("Pressione Enter para o próximo turno...");
    Console.ReadLine();

     } while (); // quais as condições para continuar a batalha? (dica: os dois devem permanecer vivos)

     // --- FIM DE JOGO ---
     Console.WriteLine("======================================");
     Console.WriteLine("A BATALHA TERMINOU!");
     if (suavida <= 0)
     {
    Console.WriteLine("Você foi derrotado pelo dragão... O tesouro continua perdido.");
     }
     else if (dragaoFugiu)
     {
    Console.WriteLine("O dragão fugiu de medo de você! O tesouro é seu!");
     }
     else if (vidadragao <= 0)
     {
         Console.WriteLine("Você derrotou o dragão! O tesouro é seu!");
     }
     Console.WriteLine("======================================");



