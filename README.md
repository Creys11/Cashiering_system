import java.util.Scanner;
public class Main {
	
	public static void main(String[] args) {
		
        Scanner s = new Scanner(System.in);



        System.out.println("==========  SIGN UP TO REGISTER ==========\n");
	    System.out.print("Enter your username : ");
		String username = s.next();
		System.out.print("Enter your password : ");
		String password = s.next();
		System.out.println("\n======= Successfully registered Mr/Ms." + username + "!  =======");
		System.out.println("\n==========  LOG IN TO YOUR ACCOUNT  ==========");

        boolean login = true;
		while (login) {
		    System.out.print("\nEnter your username : ");
			String user = s.next();
			System.out.print("Enter your password : ");
			String pass = s.next();

			if ((!user.equals(username)) && (!pass.equals(password))) {
				System. out.print("\n=====  Incorrect username or password. Try again!  =====\n");
			} else if ((user.equals(username)) && (pass.equals(password))) {
				System.out.print("\n==========  Sucessful log in!  ==========\n");
				login = false ;
			} else if ((!user.equals(username))) {
				System.out.print("\n==========  Incorrect username!  ==========\n");
			} else if ((!pass.equals(password))) {
				System.out.print("\n==========  Incorrect password!  ==========\n");
			}
		}

        System.out.println("\n=======================================================");
		System.out.println("|      ^^^^^  Welcome to AYSON BAKERY ^^^^^           |\n|             ••• This is our MENU •••                |");
		System.out.println("=======================================================");

					
        try (Scanner input = new Scanner(System.in)) {
int x=1;
int Costumer = 0;
char choice;

do {
    Costumer++;
    String[] Menu = {" DoubleBody", "Monay", "Starbread", "Pandesal", "CocoBread", "Frances", "LoafBread", "SliceBread", "ChiffonCake", "Binangkal "};
    double[] MenuPrice = {10.00, 10.00, 10.00, 2.00, 10.00, 10.00, 45.00, 35.00, 65.00, 10.00};

    int[] quant= new int[10];
    boolean DONE = false;
{

System.out.print("Welcome to Ayson Bakery! \nTake your time to choose from our Menu. ");
System.out.println("");

}
    System.out.println("CODE  NAME OF PRODUCT  PRICE");
    for (int i = 0; i < Menu.length; i++) {
        System.out.println("["+(i + 1) + "] " + Menu[i] + " - PHP " + MenuPrice[i]);
    }
       while (!DONE) {

        System.out.print("\nPlease Enter the code of your Order, \nType 0 if you're done Ordering: ");
        int MenuCode = s.nextInt();

        if (MenuCode == 0) {
            DONE = true;
        } else if (MenuCode < 1 || MenuCode > Menu.length) {
            System.out.println("Invalid Input!");
            System.out.println("-------------------------------------------");
        } else {
            System.out.print("Enter the number of Quantity: ");
            int quantity= s.nextInt();
            quant [MenuCode - 1] += quantity;
            System.out.println("-------------------------------------------");
        }
    }

    double total = 0;

    System.out.println("-------------------------------------------");
    System.out.println("------------------------");
    System.out.println("\nHere is the list of your Order. \nKindly Check before proceeding.\n");
    for (int i = 0; i < Menu.length; i++) {
        if (quant[i] > 0) {
            double subtotal = quant [i] * MenuPrice[i];
            System.out.println(Menu[i] + "  x " + '('+quant[i]+')' + " - PHP " + subtotal);
            total += subtotal;
        }
    }

    System.out.println("\nTotal: Php " + total);
    
        
    do {
        System.out.print("\nPlease enter your payment : " );
        double pay =s.nextDouble();
        if (pay >= total) {
            pay -= total;
            System.out.println("Change: Php "+pay);
            System.out.println("\nThank  you! Successful Transaction ");
            System.out.println("--------------------");
            System.out.println("-------------------------------------------");

            break;
        } else {
            System.out.println("-------------------------------------------");
            System.out.println("Not Enough Amount");
            System.out.println("-------------------------------------------");
        }
    } while (x==1);

    System.out.println("------------------------------------------");
    System.out.println("New Customer? Yes(1)No(2) ");
    choice = s.next().charAt(0);

} while (choice =='1');

System.out.print("Today, we have a total of " + Costumer + " transaction.");
        }
    }

     
 }
# Cashiering_system
