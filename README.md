# Leela-s-XY-String-Transformation

In a mystical land, a wizard named Leela has an empty string s and a magical operation she can perform. This operation allows her to insert an "XY string" at any position in s. An "XY string" is defined as a string of at least 2 characters where all the characters are 'X' except the last one, which is 'Y'.
Leela is given a target string t, made up of only 'X's and 'Y's, and she wonders if she can transform the empty string s into t using her special operation any number of times.
Can you help Leela determine if it is possible to create t from s by inserting XY strings?

import java.io.*; // for handling input/output
import java.util.*; // contains Collections framework

// don't change the name of this class
// you can add inner classes if needed
class Main {
 public static void main (String[] args) {
 // Your code here
 Scanner sc = new Scanner(System.in);
 int n = sc.nextInt();
 String xy = sc.next();
 int xC=0, yC=0;
 for(int i=0; i<n; i++) {
 char ch = xy.charAt(i);
 if(ch=='X') {
 xC++;
 }
 else {
 yC++;
 }
 }
 if(xC >= yC && xy.endsWith("Y")) {
 System.out.println("YES");
 }
 else {
 System.out.println("NO");
 }
 }
}
