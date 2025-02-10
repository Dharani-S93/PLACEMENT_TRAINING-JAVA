## 10TH FEBRUARY 2025
## MAJORITY ELEMENT

You are working for a Survey Analysis company, and your team has been given the task of analyzing survey responses. The survey asks participants to select their favorite color from a list of options, and you are provided with an array of integers where each integer represents the choice of a color. The goal is to find the majority color — the color that has been selected by more than half of the participants.

A majority element in the array is defined as an element that appears more than n/2 times, where n is the length of the array.

Requirements:

You need to write a function findMajorityColor that takes in an array of integers representing survey results and returns the majority element (if it exists), or -1 if there is no majority element.

Input:

An array of integers, colors[], where each integer represents a survey response corresponding to a particular color.
If the length of the array is n, then the function should find the element that occurs more than n/2 times.

Output:

The majority element (integer) if it exists.
If no majority element exists, return -1.

Constraints:

The array can have at most 10^5 elements.
Array elements are non-negative integers.


Example 01  :

int[] surveyResponses = {2, 3, 3, 2, 2, 3, 2, 2};

Example 02  :

int[] surveyResponses = {1, 3, 3, 2, 2};

## CODE
````
import java.util.Scanner;

public class Main {

    public static int Majority(int[] colors) {
        int n = colors.length;
        for (int i = 0; i < n; i++) {
            int count = 0;
            for (int j = 0; j < n; j++) {
                if (colors[j] == colors[i]) {
                    count++;
                }
            }
            if (count > n / 2) {
                return colors[i];
            }
        }
        return -1;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("ENTER N:");
        int n = sc.nextInt();
        System.out.println("ENTER THE VALUES:");
        int[] sr = new int[n];
        for (int i = 0; i < n; i++) {
            sr[i] = sc.nextInt();
        }
        System.out.println(Majority(sr));

    }
}
````
## OUTPUT
````
ENTER N:
5
ENTER THE VALUES:
1
3
3
2
2
MAJORITY ELEMENT IS -1
````


