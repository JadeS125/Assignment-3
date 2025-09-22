debug 3


import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
                Scanner sc = new Scanner(System.in);



        //P1: This one only prints 0-9, can you fix it so it prints 1-10?
        System.out.println("Problem 1");
        for (int i = 1; i <= 10; i++){
            System.out.println(i);
        }

        //P2: Ask the user for a number. Create a loop to find the factorial of it
        //(factorial = X!, X being the user input, Factorials are every digit before X multiplied together)
        System.out.println("Problem 2");
        System.out.println("Enter a number and I will tell you the factorial: ");
        int input = sc.nextInt();
        long factorial = 1;
       
        for (int i = 1; i <= input; i++){
            factorial = factorial * i;

        }
        System.out.println(input + "! = " + factorial);

       
        //P3: Ask the user for a number, and then add together every OTHER digit (starting from 1)
        System.out.println("Problem 3");
        System.out.println("Enter a number and I will tell you the sum of every other number: ");
        int input2 = sc.nextInt();
        int sum = 0;
        for (int i = 1; i <= input2; i+= 2){
            sum += i;
        }
        System.out.println("The sum of every other number up to " + input2 + " is: " + sum);
        //what do you need to complete this task? - a way to get a number from the user and a loop to go through every other number.






        //P4: Why does this loop never stop -  
        //Run is always true. So the while loop keeps running as long as run is true. Since the run inside the loop is never changed, it will print forever.
        //what can you do to break out of the loop after it prints once? - It needs a False!!
        System.out.println("Problem 4");
        boolean run = true;
        while (run == true){
            System.out.println("I printed once!");
            run = false;
        }

        //P5: Take a string from the user and print them the reverse!
        sc.nextLine(); // consume leftover newline from previous input

        System.out.println("Problem 5");
        System.out.println("Enter a string and I will reverse it: ");
        String text = sc.nextLine();  // use a new variable name
        String reverse = "";

        for (int i = text.length() - 1; i >= 0; i--) {
             reverse += text.substring(i, i + 1);
        }


        System.out.println("Reversed string: " + reverse);
    }
}


import java.util.Scanner;
 public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a word: ");
        String input = sc.nextLine();

        for (int i = 0; i < input.length(); i++) { // input.charAt(i) pulls out the character at position i
            // The i = 0 means the output will start at the first letter of the string
            //The i < input.length() means the program would stop when it reachs the end of the string
            //and then the i++ means the program will move to the next letter each time
            System.out.println(input.charAt(i)); // the input.charAt(i) will pull out the character at the position i
            
        }
    }
}
//I figured this out from our previous lessons by knowing how to use the Scanner class to take input from the user 
//and then i used a for loop to go through the string from the users input. The loop starts at 0 because strings 
//in Java begin from zero. SO the program keeps going until it reaches the length of the string.
// The i++ makes the loop move to the next letter each time it like with the numbers but intead of a int its a string so it will not do math.
//The input.charAt(i) pulls out one letter from the string at a time so it can be printed on its own line.


