# JustStart
package com.company;

import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter roof height");
        int roof = sc.nextInt();
        System.out.println("Enter base height");
        int base = sc.nextInt();

        for(int i=1; i<=roof; i++){
            for(int j=1; j<=roof-i; j++){
                System.out.print(" ");
            }
            System.out.print("/");
            for(int j=1; j<=2*(i-1); j++){
                if(i==roof && j!=0 && j!=2*roof){
                    System.out.print("_");
                }else{
                    System.out.print(" ");
                }
            }
            System.out.print("\\");
            System.out.println();
        }

        for(int i=1; i<=base; i++){
            for(int j=1; j<=2*roof; j++){
                if(i == base){
                    if(j==1 || j==2*roof){
                        System.out.print("|");
                    }else{
                        System.out.print("_");
                    }

                }else{
                    if(j==1 || j==2*roof){
                        System.out.print("|");
                    }else{
                        System.out.print(" ");
                    }
                }
            }
            System.out.println();
        }
    }
}
