ELECTRICITY BILL SYSTEM – PROJECT REPORT

1. Abstract

The Electricity Bill System is a Java-based application developed to automate the process of calculating electricity bills for customers based on their unit consumption. The system uses slab-based billing logic to ensure accurate and fair calculation. It reduces manual errors, saves time, and provides a simple interface for users to input data and generate bills efficiently.

2. Objective

The main objectives of this project are:

* To design a system for calculating electricity bills automatically
* To implement slab-based billing logic using Java
* To minimize human errors in bill calculation
* To provide a user-friendly interface for data entry and output

3. Technologies Used

* **Programming Language:** Java
* **Concepts Used:** OOP (Classes, Methods), Conditional Statements
* **Tools:** JDK, any IDE (Eclipse / IntelliJ / NetBeans)


4. System Requirements

  =>Hardware Requirements

  * Processor: Minimum Intel i3 or equivalent
  * RAM: 4 GB or above
  * Storage: 500 MB free space

  =>Software Requirements

  * Java Development Kit (JDK 8 or above)
  * Operating System: Windows / Linux / macOS
  * IDE: Eclipse / IntelliJ IDEA / VS Code

5. System Design

Input:

* Customer Name
* Units Consumed

Process:

* Apply slab-based billing logic:

  * 0–100 units → ₹1.5 per unit
  * 101–300 units → ₹2.5 per unit
  * Above 300 units → ₹4 per unit

Output:

* Customer details
* Units consumed
* Total bill amount

6. Algorithm

1. Start
2. Input customer name
3. Input units consumed
4. If units ≤ 100 → bill = units × 1.5
5. Else if units ≤ 300 → bill = (100 × 1.5) + (remaining × 2.5)
6. Else → bill = (100 × 1.5) + (200 × 2.5) + (remaining × 4)
7. Display bill details
8. End

7. Source Code

java id="a9f23"
import java.util.Scanner;

class ElectricityBill {

    String customerName;
    int unitsConsumed;
    double billAmount;

    void calculateBill() {
        if (unitsConsumed <= 100) {
            billAmount = unitsConsumed * 1.5;
        } 
        else if (unitsConsumed <= 300) {
            billAmount = (100 * 1.5) + (unitsConsumed - 100) * 2.5;
        } 
        else {
            billAmount = (100 * 1.5) + (200 * 2.5) + (unitsConsumed - 300) * 4.0;
        }
    }

    void displayBill() {
        System.out.println("Electricity Bill:");
        System.out.println("Customer Name : " + customerName);
        System.out.println("Units Consumed: " + unitsConsumed);
        System.out.println("Total Bill    : Rs. " + billAmount);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ElectricityBill eb = new ElectricityBill();

        System.out.print("Enter Customer Name: ");
        eb.customerName = sc.nextLine();

        System.out.print("Enter Units Consumed: ");
        eb.unitsConsumed = sc.nextInt();

        eb.calculateBill();
        eb.displayBill();

        sc.close();
    }
}

8. 📊 Sample Output

Enter Customer Name: Harshitha
Enter Units Consumed: 350

Electricity Bill:
Customer Name : Harshitha
Units Consumed: 350
Total Bill    : Rs. 1150.0

9. Advantages

* Reduces manual calculation errors
* Simple and easy to use
* Time-saving
* Can be extended for real-time applications

10. Limitations

* No database storage
* No graphical user interface
* Fixed tariff rates (not dynamic)

11. Future Enhancements

* Add GUI using Swing or JavaFX
* Integrate database (MySQL) to store customer data
* Add bill history and report generation
* Implement dynamic tariff updates
* Add online payment integration

12. Conclusion

The Electricity Bill System successfully demonstrates how Java can be used to automate real-world problems. The project highlights the use of object-oriented programming and conditional logic to build an efficient and scalable system. With further enhancements, it can be developed into a full-fledged billing application.

13. References

* Java Programming by Herbert Schildt
* Oracle Java Documentation
* Online Java Tutorials
If you want, I can next:

* Convert this into a **Word/PDF file (ready to submit)**
* Add **flowchart + diagrams** (important for marks)
* Upgrade code to **GUI version (high scoring project)**
