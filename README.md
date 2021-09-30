# Java-Random-Number-Generator
A code that makes you guess a number between 1 and 100 within a select amount of attempts. 

import java.util.Scanner;
import java.util.ArrayList; 
import java.util.Random; 

    public class CSlab3 {
        
        public static void main(String[]args)
        {
            ArrayList<Integer> takes = new ArrayList<>(); 
            Scanner input = new Scanner(System.in); 
            Random lnput = new Random(); 
            
            int num1 = lnput.nextInt(100); 
            int num3 = 15; 
            int num2; 
            
            System.out.println("I'm thinking of a number between 1 and 100...");
            System.out.println("You have 15 tries."); 
            
            do {
                System.out.println("Please enter a number: ");
                num2 = input.nextInt(); 
                takes.add(num2); 
                
                if (num2 > num1 && num2 <= 100)
                {
                    System.out.println(num2 + " was too high.");
                    num3--; 
                    System.out.println(num3 + " Tries remaining.");
                }
                else if (num2 < num1 && num2 >= 1)
                {
                    System.out.println(num2 + " was too low.");
                    num3--; 
                    System.out.println(num3 + " Tries remaining.");
                }
                else if (num2 > 100) 
                {
                    System.out.println(num2 + " was out of the number range.");
                    num3--; 
                    System.out.println(num3 + " Tries remaining.");
                }
                else if (num2 < 1)
                {
                    System.out.println(num2 + " was out of the number range.");
                    num3--; 
                    System.out.println(num3 + " Tries remaining.");
                }
                else 
                {
                    System.out.println(num2 + " was correct!");
                }
            } while (num2 != num1 && num3 !=0);    
            
            if (num3 == 0)
            {
                System.out.println("The Number was " +num1 + ". Better luck next time!");
            }
            else
            {
                System.out.println("Congratulations! It took you "+ takes.size()
            + " time(s)!");
            }
            System.out.println(takes); 
        }
    } 

