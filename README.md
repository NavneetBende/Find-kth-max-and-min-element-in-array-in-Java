Find kth max and min element in array
Here, in this page we will discuss the program to find the kth max and min element in an array in Java . We use the concept of set in finding the kth maximum and minimum element of the array. We are giving with the size of the array along with array elements and the value of K. We have to print the maximum and the minimum element.

Find kth max and min element in array
Algorithm :
Take a length of the array as an input from the user followed by elements of the array.

Take the value of k from the user.

create a queue

Top elements will be removed if size>k

Top will be printed, and the top element will be the maximum of the array

Run

import java.io.*;
import java.util.*;
public
class Main {
    public
    static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int n, k, i;

        System.out.println("Enter the size of the array: ");
        n = 3;

        System.out.println("Enter the elements for the array: ");
        int arr[] = {1,2,4,5};


        System.out.println("Enter the value of k: ");
        k = 2;

        PriorityQueue queue = new PriorityQueue<>(Collections.reverseOrder());
        System.out.println("Kth smallest element is: ");

        for (i = 0; i < n; i++) { queue.add(arr[i]); if (queue.size() > k) {
                queue.poll();  // top elements will be removed if size>k
            }
        }
        System.out.println(queue.peek());  // top will be printed

        PriorityQueue queue1 = new PriorityQueue<>();
        System.out.println("Kth Largest element is: ");

        for (i = 0; i < n; i++) { queue1.add(arr[i]); if (queue1.size() > k) {
                queue1.poll();  // top elements will be removed if size>k
            }
        }
        System.out.println(queue1.peek());  // top will be printed
    }
}
Output
Enter the size of the array: 
Enter the elements for the array: 
Enter the value of k: 
Kth smallest element is: 
2
Kth Largest element is: 
2
