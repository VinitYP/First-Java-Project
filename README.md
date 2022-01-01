# First-Java-Project

Just wanted to clear concept of calling static / nostatic function from main , calling return values reading them, etc stuff to get command on them.
package MethodsPractice;

import java.util.Scanner;

public class Vaccination
{
    Scanner scanner = new Scanner(System.in);

    public int UserId()
    {
        Scanner scanner = new Scanner(System.in);
        int id,idpre,pass;
        System.out.println("Enter Your Id");
        idpre = scanner.nextInt();
        System.out.println("Enter Your Password");
        pass = scanner.nextInt();

        id = 12345;
        if(id == idpre)
        {
            int pincode;
            System.out.println("Enter Your Pin Code");
            pincode = scanner.nextInt();
            return pincode;
        }
        else
        {
            System.out.println("Wrong Id & Passowrd ");

        }
        return 0;
    }

    public String date()
    {
        Scanner scanner = new Scanner(System.in);
        String dae;
        System.out.println("Enter date do you want. ");
        dae = scanner.next();
       return dae;
    }
    public String VaccinrType()
    {
        System.out.println("Which vaccine do you want ?");
        System.out.println("1. COVID-SHIELD\n2. COVACCINE\n3. SPUTNIK");
        int n = scanner.nextInt();
        if (n==1)
        {
            String type;
            type= "COVID-SHIELD";
            return type;
        }
        else if (n==2)
        {
            String type;
            type= "COVACCINE";
            return type;
        }
        else
        {
            String type;
            type= "SPUTNIK";
            return type;
        }
    }


    public  void Location(int pincode ,String date ,String type )
    {
        Scanner scanner = new Scanner(System.in);
        int n;
        if (pincode == 440016 )
        {
            System.out.println("1.CRPF GATE\n2.PHC IC CHOWK\n3.ZP SCHOOL");
            n = scanner.nextInt();
            if (n==1)
            {
                String place;
                place = "CRPF GATE";
                System.out.println("Your Vacctination drive for dose 1 was succesfully regesrted at Location "+ place);
                System.out.println("Your vaccine is "+type);
                System.out.println("Your date is "+date);
                System.out.println("FOR MORE DETAIL CONTACT 999999999 .");
            }
            else if (n==2)
            {
                String place1;
                place1 = "PHC IC CHOWK";
                System.out.println("Your Vacctination drive for dose 1 was succesfully regesrted at Location "+ place1);
                System.out.println("Your vaccine is "+type);
                System.out.println("Your date is "+date);
                System.out.println("FOR MORE DETAIL CONTACT 999999999 .");
            }
            else if (n==3)
            {
                String place1;
                place1 = "ZP SCHOOL";
                System.out.println("Your Vacctination drive for dose 1 was succesfully regesrted at Location "+ place1);
                System.out.println("Your vaccine is "+type);
                System.out.println("Your date is "+date);
                System.out.println("FOR MORE DETAIL CONTACT 999999999 .");
            }

        }
        else
        {
            System.out.println("Sorry only 440016 pincode area have vaccination drive. plz contact 9999999999 for more details. Thanks you ");
        }
    }

    public static void main(String[] args)
    {
        Vaccination vacc = new Vaccination();
       int pincode = vacc.UserId();
       String date = vacc.date();
       String type = vacc.VaccinrType();
       vacc.Location(pincode,date,type);
    }

}
