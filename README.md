# JAVA-DICE-ROLL
"An interactive dice roller built in Java, allowing users to roll multiple dice and instantly see the individual rolls and their cumulative total."


    import java.util.Random;
    import java.util.Scanner;

    public class Main 
    {
    public static void main(String[] args)
    {
    Scanner scan = new Scanner(System.in);
    Random rand = new Random();

    int numOfDice;
    int total = 0;
    int roll;

    System.out.print("Enter # of dice : ");
    numOfDice = scan.nextInt();

    if(numOfDice > 0)
    {

    for(int i = 0; i < numOfDice; i++)
    {
      roll = rand.nextInt(1,7);
      printDie(roll);
      System.out.println("You rolled : " + roll);
      total += roll;
    }
        System.out.println("Total: " + total);

    }
    else
    {
        System.out.println("please enter the dice greater than 0");
     }
     scan.close();
    
    }

    static void printDie(int roll)
    {

        String dice1 = """
                 -------
                |       |
                |   ●   |
                |       |
                 -------
                """;

        String dice2 = """
                  -------
                | ●       |
                |         |
                |      ●  |
                  -------
                """;

        String dice3 = """
                  -------
                | ●      |
                |   ●    |
                |     ●  |
                  -------
                """;

        String dice4 = """
                  -------
                | ●    ● |
                |        |
                | ●    ● |
                  -------
                """;

        String dice5 = """
                 -------
                | ●   ● |
                |   ●   |
                | ●   ● |
                 -------
                """;

        String dice6 = """
                  -------
                | ●    ●  |
                | ●    ●  |
                | ●    ●  |
                  -------
                """;


    
    switch(roll){
        case 1 -> System.out.println(dice1);
        case 2 -> System.out.println(dice2);
        case 3 -> System.out.println(dice3);
        case 4 -> System.out.println(dice4);
        case 5 -> System.out.println(dice5);
        case 6 -> System.out.println(dice6);
        default -> System.out.println(" Invalid Number");
    }
    }
    }
