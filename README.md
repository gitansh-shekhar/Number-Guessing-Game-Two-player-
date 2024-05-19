# Number-Guessing-Game-Two-player-
This is the JAVA code of guessing a number Played between two Player.








import java.util.Scanner;

public class NumberGuessing {
    int random(){
        return (int)(Math.random()*100);
    }

    public static void main(String[] args) {
        NumberGuessing ns=new NumberGuessing();
        Scanner sc=new Scanner(System.in);
        int rand=ns.random();
        System.out.println("Welcome to number Guessing Game between 1 to 100");
        System.out.println("who is the first Player :");
        String p1=sc.next();
        System.out.println("Who is the second player :");
        String p2=sc.next();
        int countP1 =0;
        int countP2=0;
        System.out.println(p1+" Please Guess a number :");

        do{

            int guess=sc.nextInt();
            countP1++;
            if(rand==guess){
                System.out.println("AHH "+p1+" guessed the number in "+countP1+" move");
                break;
            }
         else   if(guess>rand){
                System.out.println("Guess smaller number");
            }
         else{
                System.out.println("Guess Bigger number");
            }
        }
        while(true);
        System.out.println(p2+" Please Guess a number :");

        do{

            int guess=sc.nextInt();
            countP2++;
            if(rand==guess){
                System.out.println("AHH "+p2+" guessed the number in "+countP2+" move");
                break;
            }
            else   if(guess>rand){
                System.out.println("Guess smaller number");
            }
            else{
                System.out.println("Guess Bigger number");
            }
        }
        while(true);
        if(countP2>countP1) {
            System.out.println("And the winner is "+p1.toUpperCase());
        }
      else  if(countP1>countP2){
            System.out.println("And the winner is "+p2.toUpperCase());
        }
      else System.out.println("Match draw");


    }

}
