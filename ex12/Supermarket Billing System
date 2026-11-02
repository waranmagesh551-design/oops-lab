import java.util.ArrayList;
import java.util.Scanner;
class Product {
 private String name;
 private double price;
 private int quantity;
 public Product(String name, double price, int quantity) {
 this.name = name;
 this.price = price;
 this.quantity = quantity;
 }
 public String getName() {
 return name;
 }
 public double getPrice() {
 return price;
 }
 public int getQuantity() {
 return quantity;
 }
 public double getTotal() {
 return price * quantity;
 }
}
public class SupermarketBillingSystem {
 public static void main(String[] args) {
 Scanner sc = new Scanner(System.in);
 ArrayList<Product> cart = new ArrayList<>();
 System.out.println("Available Products:");
 System.out.println("1. Rice - Rs. 60");
 System.out.println("2. Milk - Rs. 30");
 System.out.println("3. Soap - Rs. 25");
 System.out.print("Enter number of different products: ");
 int n = sc.nextInt();
 for (int i = 0; i < n; i++) {
 System.out.print("Enter product choice (1-3): ");
 int choice = sc.nextInt();
 String name;
 double price;
 switch (choice) {
 case 1:
 name = "Rice";
 price = 60;
 break;
 case 2:
 name = "Milk";
 price = 30;
 break;
 case 3:
 name = "Soap";
 price = 25;
 break;
 default:
 System.out.println("Invalid product choice. Try again.");
 i--;
 continue;
 }
 System.out.print("Enter quantity: ");
 int quantity = sc.nextInt();
 if (quantity <= 0) { System.out.println("Quantity must be greater than zero.");
 i--;
 continue;
 }
 cart.add(new Product(name, price, quantity));
 }
 double subtotal = 0;
 System.out.println("\\n------ SUPERMARKET BILL ------");
 System.out.printf("%-10s %8s %8s %10s%n",
 "Product", "Price", "Qty", "Total");
 for (Product p : cart) {
 System.out.printf("%-10s %8.2f %8d %10.2f%n",
 p.getName(), p.getPrice(), p.getQuantity(), p.getTotal());
 subtotal += p.getTotal();
 }
 double discount = subtotal * 0.10;
 double finalBill = subtotal - discount;
 System.out.printf("%nSubtotal: Rs. %.2f%n", subtotal);
 System.out.printf("Discount (10%%): Rs. %.2f%n", discount);
 System.out.printf("Final Bill: Rs. %.2f%n", finalBill);
 System.out.println("Thank you for shopping!");
 sc.close();
 }
}
