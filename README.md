# Name:        TASK-1. NUMBER-GAME-in-Java-Developer
# Purpose:     Cod Soft TASK-1 (C++)
#  1. Generate a random number within a specified range, such as 1 to 100.
   2. Prompt the user to enter their guess for the generated number.
   3. Compare the user's guess with the generated number and provide feedback on whether the guess is correct, too high, or too low.
   4. Repeat steps 2 and 3 until the user guesses the correct number. You can incorporate additional details as follows:
   5. Limit the number of attempts the user has to guess the number.
   6. Add the option for multiple rounds, allowing the user to play again.
   7. Display the user's score, which can be based on the number of attempts taken or rounds won.
# Author:      NURFUL SHAIKH
# Created:     31-05-2024

import java.util.Scanner;
public class GFG {
public static void
guessingNumberGame()
{
Scanner sc = new Scanner(System.in);
int number = 1 + (int)(100
* Math.random());
int K = 5;
int i, guess;
System.out.println(
"A number is chosen"
+ " between 1 to 100."
+ "Guess the number"
+ " within 5 trials.");
for (i = 0; i < K; i++) {
System.out.println(
"Guess the number:");
guess = sc.nextInt();
if (number == guess) {
System.out.println(
"Congratulations!"
+ " You guessed the number.");
break;
}
else if (number > guess
&& i != K - 1) {
System.out.println(
"The number is "
+ "greater than " + guess);
}
else if (number < guess
&& i != K - 1) {
System.out.println(
"The number is"
+ " less than " + guess);
}
}
if (i == K) {
System.out.println(
"You have exhausted"
+ " K trials.");
System.out.println(
"The number was " + number);
}
}
public static void
main(String arg[])
{
guessingNumberGame();
}
}
