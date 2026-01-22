import java.util.*;
import java.io.*;
import java.io.File;
class Book
{
    String bn,an;
    int bid;
    boolean sts;
    void getBook(Scanner sc,int bid)
    {
        System.out.print("Enter Book Name : ");
        this.bn=sc.next();
        System.out.print("Enter Author Name : ");
        this.an=sc.next();
        this.bid=bid;
        System.out.println("Book ID : "+bid);
        this.sts=true;
    }
}
class Student
{
    String sn,pw;
    int sid;
    void getStudent(Scanner sc,int sid)
    {
        System.out.print("Enter Student Name : ");
        this.sn=sc.next();
        this.sid=sid;
        System.out.print("Enter Password : ");
        this.pw=sc.next();
        System.out.println("Student ID : "+sid);
    }
}
class Main 
{
    static void viewBooks(Book bk[],int bkt)
    {
        System.out.println("Book Name \t\t Author \t\tBook ID");
        for(int i=0;i<bkt;i++)
        {
            if(bk[i].sts)
            
            System.out.println(bk[i].bn+"  \t\t\t"+bk[i].an+"\t\t\t"+bk[i].bid);
        }
    }
    public static void main(String[] args)
    {
        Book bk[]=new Book[100];
        Student sk[]=new Student[100];
        Scanner sc=new Scanner(System.in);
        int bkt=0,stk=0,sid=1001,bid=100;
        System.out.println("\t\t\t*******WELCOME TO BOOKWORMS LIBRARY*******");
        while(true)
        {
            System.out.println("1. Admin");
            System.out.println("2. Student");
            System.out.println("3. Exit");
            System.out.print("Enter your choice : ");
            int op=sc.nextInt();
            if(op==3)
            {
                System.out.println("\t\t\t*******Thank You For Using*******");
                break;
            }
            else if(op==1)
            {
                System.out.print("Enter Admin ID : ");
                String aid=sc.next();
                System.out.print("Enter Admin Password : ");
                String ap=sc.next();
                if(aid.equals("1234")&&ap.equals("123"))
                {
                    System.out.println("Login Successful!!!");
                    while(true)
                    {
                        System.out.println("1. Add Book"); 
                        System.out.println("2. View Books");
                        System.out.println("3. Exit");
                        System.out.print("Enter Your Choice : ");
                        int x=sc.nextInt();
                        if(x==1)
                        {
                            System.out.print("Enter The Number Of Books To Be Added : ");
                            int numbooks=sc.nextInt();
                            for(int i=0;i<numbooks;i++)
                            {
                                bk[bkt]=new Book();
                                bk[bkt].getBook(sc,bid);
                                bkt++;
                                bid++;
                            }
                        }

                        else if(x==2)
                        {
                            viewBooks(bk,bkt);
                        }
                        else if(x==3)
                        {
                            System.out.println("Logout Successful!!!");
                            break;
                        }
                        else
                        {
                            System.out.println("Invalid ID/Password!!! Please Try Again!!!");
                        }
                    }
                } 
            }
                else if(op==2)
                {
                    System.out.println("\n1.Signup");
                    System.out.println("2.Login");
                    System.out.println("3.Exit");
                    System.out.print("Enter your choice : ");
                    int tid=sc.nextInt();
                     if(tid==1)
                    {
                     System.out.print("Enter Number Of Students To Be Added : ");
                            int st=sc.nextInt();
                            for(int i=0;i<st;i++,System.out.println())
                            {
                                sk[stk]=new Student();
                                sk[stk].getStudent(sc,sid);
                                stk++;
                                sid++;
                            }   
                    }
                    else if(tid==2)
                     {
                    System.out.print("Enter Student ID : ");
                    int Id=sc.nextInt();
                    System.out.print("Enter Password : ");
                    String pwd=sc.next();
                    try 
                    {
                        if(sk[Id-1001].pw.equals(pwd))
                        {
                            System.out.println("Login Successful!!!");
                            while(true)
                            {
                                System.out.println("1. View Books");
                                System.out.println("2. Lend Books");
                                System.out.println("3. Return Book");
                                System.out.println("4. Exit");
                                System.out.print("Enter Your Choice : ");
                                int x=sc.nextInt();
                                if(x==1)
                                {
                                    viewBooks(bk,bkt);
                                }
                                
                                else if(x==2)
                                {
                                    System.out.print("Enter Book Name : ");
                                    String bn=sc.next();
                                    System.out.print("Enter Book ID : ");
                                    int tbid=sc.nextInt();
                                    if(bk[tbid-100].bn.equals(bn))
                                    {
                                        bk[tbid-100].sts=false;
                                        System.out.println("Lended Successfully!!!");
                                    }
                                    else
                                        System.out.println("Invalid Details!!!");
                                }
                                else if(x==3)
                                {
                                    System.out.print("Enter Book Name : ");
                                    String bn=sc.next();
                                    System.out.print("Enter Book ID : ");
                                    int tbid=sc.nextInt();
                                    if(bk[tbid-100].bn.equals(bn)&&bk[tbid-100].sts==false)
                                    {
                                        bk[tbid-100].sts=true;
                                        System.out.println("Returned Successfully!!!");
                                    }
                                    else
                                        System.out.println("Invalid Details!!!");
                                }
                                else if(x==4)
                                {
                                    System.out.println("Logout Successful!!!");
                                    break;
                                }
                                else
                                    System.out.println("Invalid Choice!!!");
                            }
                        }
                        else
                            System.out.println("Invalid ID/Password!!!");
                    }
                    catch(Exception e)
                    {
                        System.out.println("Student Not Found!!!");
                    }
                }
            
            else
                System.out.println("Invalid Choice!!!");
        }
     }
    }
}
