# STRINGS
//Count the vowels
//SOURCE CODE

import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();       
        int vowels=0,i;        
        for(i=0;i<str.length();i++)
        {
            char vow=str.charAt(i);
            if(vow=='a' || vow=='A' || vow=='e' || vow=='E' || vow=='i' || vow=='I' || vow=='o' || vow=='O' || vow=='u' || vow=='U' )
            {
                vowels++;
            }
        }        
System.out.println("Number of vowels: "+vowels);
        
    } 
}

//Palindrome
//SOURCE CODE

import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner (System.in);
        String str=sc.next();
        String str1="";
        for (int i=str.length()-1;i>=0;i--){
            str1=str1+str.charAt(i);
        }
        str=str.toLowerCase();
        str1=str1.toLowerCase();
        if(str.equals(str1)){
            System.out.println("Palindrome");
        }
        else
            System.out.println("Not a Palindrome");
    }
}

//First Non-repeating Character
//SOURCE CODE

import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();
        int index = -1;
        char fnc = ' ';
        for (char i : str.toCharArray()) {
            if (str.indexOf(i) == str.lastIndexOf(i)) {
                fnc = i;
                break;
            }
            else {
                index += 1;
            }
        }
        if (index == str.length()-1) {
            System.out.println("All the characters are repetitive");
        }
        else {
            System.out.println(fnc);
        }
    }
}
