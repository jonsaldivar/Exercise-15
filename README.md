# Exercise-15

/*
*Jonathan Saldivar
*ITSE 1302-011
*Exercise 15
*puts out all the even intergers between 2 and the player selected number.
*/

public class Integers {
private int intInput;
private int intSum;
private int intMinInt = 2;
private int intMaxUserInt = 250;

   public Integers(){
    GetUserInt();
    }
    
    
    private int CounterReset(){
    intSum = 0;
    return intSum;
    }
    
    private int GetUserInt() {
    Scanner objInput = new Scanner(System.in);
    System.out.println();
    System.out.println("Type in a positvie number above 2 but less then 250.");
    intInput = objInput.nextInt();
    CounterReset();
    CheckIntInput();
    return intInput;
    }
    
    
    private void CheckIntInput() {
    if (intInput < intMinInt) {
    ToLowInt();
    }
    else if (intInput > intMaxUserInt) {
    
    
    MaxUserInt();
    }
    else {
    
    
    HighEnoughIntToProcess();
    }
 }
    
    private void ToLowInt() {
    System.err.println("Please type in a POSITVE number above between 2 and 250");
    GetUserInt();
    }
    
    private void MaxUserInt(){
    System.err.println("Please type in a number below 250 ");
    GetUserInt();
    }
    
   
    private void HighEnoughIntToProcess() {
    System.out.println("Even intergers: ");
    for (int intValue = intMinInt; intValue <= intInput; intValue++) {
    switch (intValue % 2) {
    case 0:
    
    System.out.print(intValue + ", ");
    intSum = intSum + intValue;
    }
    }
    PrintValue();
    }
    
    
    private void PrintValue() {
    System.out.println("Sum: " + intSum + ".");
    GetUserInt();
    
    }
    }
