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

## Problem Solving - 10.02.2025

Find the kth largest and smallest number in an array

Task 1: Find the kth smallest score

You need to find the 3rd smallest score in this list.

Task 2: Find the kth largest score

You also need to find the 2nd largest score in this list.

You have the following scores recorded for 10 participants:

scores = [65, 89, 45, 72, 54, 91, 32, 77, 60, 82]

## CODE
`````

import java.util.*;
public class Main{
    public static void main (String[] args){
        Scanner s=new Scanner(System.in);
        System.out.println("enter n");
        int n=s.nextInt();
        System.out.println("enter ks");
        int ks=s.nextInt();
        System.out.println("enter kl");
        int kl=s.nextInt();
        System.out.println("enter the elements");
        int a[]=new int [n];
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }
        Arrays.sort(a);
        System.out.println("THE THIRD Smallest IS "+a[ks-1]);
        System.out.println("THE 2ND LARGEST IS  "+a[n-kl]);
    }
}

`````
### OUTPUT
````
enter n
6
enter ks
3
enter kl
2
enter the elements
9
8
7
6
5
4
THE THIRD Smallest IS 6
THE 2ND LARGEST IS  8
````
