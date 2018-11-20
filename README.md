# ReportTrackingSystem
My offering is : create an application that  allows parents  to check on their children’s reports
Program:
    /*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package cs101project;

import java.io.FileNotFoundException;
import java.io.PrintWriter;
import java.util.Scanner;
/* the program produce the student reports for parents
name :Adla sror Al-shihry
Contact information:minomy_8@hotmail.com
Date 2014/12/23
section: 30
*/
public class Cs101Project {
     enum Rating{A, B, C};
     public static int IDENT1=212410293;
     public static int IDENT=0;
     public static String email;
     public static  String phone;
     public static int ask;
     public static int index;
     public static String filename="project.txt";
     public static  PrintWriter outStream=null;

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        welcome();
        inter();
        student();
        
        do
        { 
            System.out.println();
        System.out.println("Sorry the identity you have entered is wrong\nPlease insert correct number and try again ");
   
         student();
        }  
       while(IDENT!=IDENT1);
          }
    public static void welcome(){
              
         try
                      {
                     outStream= new PrintWriter(filename);
                    }
              catch(FileNotFoundException e)
             {
              System.out.println("Error opening the file ."+filename);
                 System.exit(0);
             }
        
             System.out.println("******Welcome you in PSU this page for students reports******");
        outStream.println("******Welcome you in Prince sultan unvirctiy ******");
        outStream.println();
         }

    public static void inter(){
             System.out.println("\n\nPlease insert student \"ID Card\" or \"identity card\" number should not be more than 9 digits.");}
    public static void student(){
           
             Scanner keyboard=new Scanner(System.in);
             Scanner input=new Scanner(System.in);
        
       IDENT=keyboard.nextInt();
       while(IDENT==IDENT1)
            
        
         {System.out.println("=====================================");
         outStream.println("=============================================");
             System.out.println("Student Name:Adla sror AL-Shihry ");
             System.out.println("");
            outStream.println("Student Name : Adla sror AL-Shihry");
             System.out.println("Student ID number:"+IDENT);
             outStream.println("Student ID number:"+IDENT);
            
             outStream.println("");
             System.out.println("The subject she has taken this semester are:");
             outStream.println("The subject she has taken this semester are: ");
         String[] item={" ","CS101","MATH113","ISC103","ARB105","ENG101","HP111"};
         int[] item2=new int[6];
         int[] hour={0,4,3,2,2,3,2,2,3};
         for(int i=1;i<item2.length;i++)

         {System.out.print( i+". "  +item[i]+  "  "+"  "+hour[i]+"  "+((hour[i]> 1) ?   " hours\n": "hour"));
         outStream.println(i+". "  +item[i]+  "  "+"  "+hour[i]+"  "+((hour[i]> 1) ?   " hours\n": "hour"));
             }
         System.out.println("");
             outStream.println();
         double grade=3.0;
         System.out.println("Last total grade is:"+(grade));
         outStream.println("Last total grade is:"+(grade));
         outStream.println();
                 grade=3.0/4.0*100;
                 
             System.out.printf("The student average is %6.2f %%.",grade);
              outStream.println("The student average %"+(grade));
              outStream.println();
              
            Rating grad;
             grad=Rating.B;
  
             

             switch(grad)
             
             {
                 
                case A:
                    
              System.out.println("Excellent");
                   break;
                 case B:
                     
              System.out.println("Average");
               break;
               case C:
              System.out.println("Skip it!");
                    default:
         System.out.println("FILUR");
                       
              }
                
             System.out.println("The grade is :"+(grad)+"");
             outStream.println("The grade is :"+(grad));
             System.out.println("========================================================");
             outStream.println("========================================================");
            
             System.out.println("If you want to recive the last report about student please \n\"1\" for yes \"or\" \"2\" for No");
           ask=keyboard.nextInt();
             if(ask==1)
             {
               System.out.println("\nPlease Enter your praivet email to send any update about your daughter:");
               System.out.println("");
           
         email=input.nextLine();
         
         int index = email.indexOf('@');//checking
            index = email.indexOf("mail");
            index = email.indexOf(".com");
         while ( index <0 )
         {
             System.out.println("\nPlease Enter your praivet email correctly :");
             System.out.println("");
            
         email=input.next();
         index = email.indexOf('@');//checking
         index = email.indexOf("mail");
         index = email.indexOf(".com");
         
         }
         
         email=email.toUpperCase();

         
             System.out.println("Please Enter your phone number:");
          phone= keyboard.next();
          
     while ( phone.length() > 10 || phone.length()< 10  )
     {
     System.out.println("Please Enter the correct phone number:");
          phone= keyboard.next();
     }
                 System.out.println("");
         
         System.out.println("Thank youe we will send you any new update about your daughter by an email you have entered. "
                 +(email)+"."+"\nand phone number "+(phone)+".");
         outStream.println("Thank you for visiting psu we are glad for serving you.");
              System.out.println("\" The file has been printed in\" "+filename+".");
                     outStream.close();
                     System.exit(0);
             }
              while(ask==2)
          {
                     System.out.println("Thank you for visiting psu we are glad for serving you");
                     outStream.println("Thank you for visiting psu we are glad for serving you");
                     outStream.close();
                     outStream.println();
                     System.out.println("\" The file has been printed in\" "+filename+".");
                     System.exit(0);
             }
         }}}
        // TODO code application logic here
    
    


 
