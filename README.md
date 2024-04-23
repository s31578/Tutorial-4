#tutorial 4


public class Main {
    public static void main(String[] args) {
        class User {
            private String name;
            private String lastName;
            private String email;
            private String password;
            private boolean isGuest;
            public User(String email) {
                this.email = email;
                this.isGuest = true;
            }
            public User(String name, String lastName, String email, String password) {
                this.name = name;
                this.lastName = lastName;
                this.email = email;
                this.password = password;
                this.isGuest = false;
            }
            public void convertToUser(String name, String lastName, String password) {
                if (isGuest) {
                    this.name = name;
                    this.lastName = lastName;
                    this.password = password;
                    this.isGuest = false;
                } else {
                    System.out.println("This is already a user account.");
                }
            }
        }
        class Product {
            private String name;
            private double price;
            private String productCode;
            private int numOfPieces;
            public Product(String name, double price, String productCode) {
                this.name = name;
                this.price = price;
                this.productCode = productCode;
                this.numOfPieces = 0;
            }
            public Product(String name, double price, String productCode, int numOfPieces) {
            this.name = name;
                this.price = price;
                this.productCode = productCode;
                this.numOfPieces = numOfPieces;
            }
            public void changePrice(double newPrice) {
                this.price = newPrice;
            }
            public void changeNumOfPieces(int newNumOfPieces) {
                if (newNumOfPieces >= 0) {
                    this.numOfPieces = newNumOfPieces;
                } else {
                    System.out.println("Number of pieces cannot be negative.");
                }
            }
            public String getAllParameters() {
                return "Name: " + name + ", Price: " + price + ", Product Code: " + productCode + ", Number of Pieces: " + numOfPieces;
            }
        }
        class main {
            public static void main(String[] args) {
                User guest1 = new User("guest1@example.com");
                User guest2 = new User("guest2@example.com");
                guest1.convertToUser("John", "Doe", "password123");
                User user = new User("Jane", "Smith", "jane@example.com", "password456");

                Product product1 = new Product("Phone", 500.00, "PHN123");
                Product product2 = new Product("Laptop", 1000.00, "LPT456", 5);
                Product product3 = new Product("Headphones", 50.00, "HPH789");
                product1.changePrice(50.0);

                product3.changeNumOfPieces(10);
                System.out.println("Product 1: " + product1.getAllParameters());
                System.out.println("Product 2: " + product2.getAllParameters());
                System.out.println("Product 3: " + product3.getAllParameters());
            }
        }
        }
    }
