package util.Scanner;

import java.util.Scanner;

public class Email {
	private String firstName;
	private String lastName;
	private String password;
	private int mailboxCapacity=600;
	private String alternateEmail;
	
	public Email(String firstName, String lastName, String password, int mailboxCapacity, String alternateEmail) {
		super();
		this.firstName = firstName;
		this.lastName = lastName;
		this.password = password;
		this.mailboxCapacity = mailboxCapacity;
		this.alternateEmail = alternateEmail;
	}

	public String getFirstName() {
		return firstName;
	}

	public void setFirstName(String firstName) {
		this.firstName = firstName;
	}

	public String getLastName() {
		return lastName;
	}

	public void setLastName(String lastName) {
		this.lastName = lastName;
	}

	public String getPassword() {
		return password;
	}

	public void setPassword(String password) {
		this.password = password;
	}

	public int getMailboxCapacity() {
		return mailboxCapacity;
	}

	public void setMailboxCapacity(int mailboxCapacity) {
		this.mailboxCapacity = mailboxCapacity;
	}
	

	public String getAlternateEmail() {
		return alternateEmail;
	}

	public void setAlternateEmail(String alternateEmail) {
		this.alternateEmail = alternateEmail;
	}

	public String generatepassword(int length) {
		String characters ="abdfhfndbgb@234";
		String password="";
		
		for (int i=0; i<length;i++) {
		int index =(int)(Math.random() *characters.length());
		password+=(characters.charAt(index));
		}
		return password;
	}
	public String info() {
		return "Name: "+firstName+" "+"\nlastName:"+lastName + "\npassword:"+password +"\nmailbox Capacity:"+mailboxCapacity +"\nAlternateEmail:"+alternateEmail ;
}
    @Override
    public String toString() {
        return info();
    }
		public static void main(String[] args) {
			Scanner sc = new Scanner(System.in);

	        System.out.print("Enter your name: ");
	        String name = sc.nextLine();

	        System.out.print("Enter your last name: ");
	        String lastName = sc.nextLine();

	        System.out.print("Enter your password: ");
	        String password = sc.nextLine();

	        System.out.print("Enter your mailbox capacity: ");
	        int mailboxCapacity = sc.nextInt();
	        sc.nextLine(); 
	        System.out.print("Enter your alternate email: ");
	        String alternateEmail = sc.nextLine();

	        
	        System.out.println("\nUser Details:");
	        System.out.println("Name:- " + name);
	        System.out.println("Last Name:- " + lastName);
	        System.out.println("Password:- " + password); 
	        System.out.println("Mailbox Capacity:- " + mailboxCapacity);
	        System.out.println("Alternate Email:- " + alternateEmail);

	        sc.close(); 
	    }
	
		}
