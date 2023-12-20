# ArrayList
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Project/Maven2/JavaApp/src/main/java/${packagePath}/${mainClassName}.java to edit this template
 */

package com.mycompany.arraylistlesson;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import java.util.Scanner;

/**
 *
 * @author User
 */
public class ArrayListLesson {

    public static void main(String[] args) {
       ArrayList<List> complexArray = new ArrayList<>();
       
       complexArray.add(Arrays.asList("Costas",15,34.12));
       complexArray.add(Arrays.asList("Giannis",850.32,14));
       complexArray.add(Arrays.asList("Elenh",15,32.20));
       
       for(List myRecords : complexArray){
           System.out.println(
           myRecords.get(0)+" "+myRecords.get(1));
       }
   Scanner myKeyboard = new Scanner(System.in);
       
        System.out.println("Enter name to find weight");
        String name=myKeyboard.nextLine();
        
        System.out.println("I'm searching "+name+ " weight");
        
        complexArray.forEach(arrayName->{
            
            if(arrayName.get(0).equals(name)){
                System.out.println("I found the person...");
                System.out.println(name+ " is weighting"+arrayName.get(2)+ " Kg");
                System.exit(0);
            }else{
                System.out.println("This person is not found yet");
            }
            });
    }
}
