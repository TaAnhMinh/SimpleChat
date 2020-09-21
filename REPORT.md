
Placeholder for your answers to Assignment #2
Part 1, Question 2:
a.
![image](https://user-images.githubusercontent.com/47424577/67612189-4229a700-f76e-11e9-8b8a-165f43c15aab.png)
16 threads are currently running.

b. 
![image](https://user-images.githubusercontent.com/47424577/67611070-f1618080-f764-11e9-9d26-ba74e1793f69.png)

Part 2, Question 1 Class diagram:
class Driver {

  name;

  int employeeNumber;

  seniority;

  int experienceLevels; 

  String trainOrBus; 

}

class BusRoute{

  int busRouteNumber;

  String startingLocation;

  String endingLocation;
 
  public void assignRoute(Driver a, Vihicle b){}
  //assign busRoute to the driver
 
  	* -- 1 Driver AssignTo;
}

class TrainRoute{

  int trainRouteNumber;

  boolean passRequirement;

  String startingLocation;

  String endingLocation;

   String[] location;
 
  public void requirementPassed(Driver a){}

  //check if the driver pass the requirement or not
 
  public void assignRoute(Driver a, Train b){}

  //if driver pass then assignRoute to the driver
 
 	 * -- * Driver AssignTo;

}

class Train{

  Driver a;
 
  	* -- * TrainRoute AssignTo;

}

class GlobalSystem{
}

class IndividualSystem{

  int accidents;

  int majorAcc;

  int numberOfFines;

  double fineValue;

  public int numberOfAccidents(){}

  public int majorAccidents(){}

  public String driverInvoled (){} 

  public double fines(){}

  	1 Control -- 1 Driver;

  	* -- 1 GlobalSystem Control;

}

class WorkHour{

  double workShift;

  double overTime;

  double workHourToday;

  double payment;

  public double calculateOvertime(Driver a){}

  public double getWorkingHour(){};
 
  public double paymentIs(Driver a){}

  	* -- * Driver Work;

}

class Vihicle{

  Driver a;

  	* -- * BusRoute AssignTo;

}

class DoubleDecker{

  isA Vihicle;

}

class ExtendedBus{isA Vihicle;}

class NormalBus{  isA Vihicle;}

class Passenger{

  name;

  int customerNumber;

  String destination;
 
  private BusRoute CheckRouteForBus(Location a){}

  private TrainRoute CheckRouteForTrain(Location a){}
   
  	1 Pay -- * PaymentMethod;
 
}

class Location{

 destination;

  	* -- 1..* BusRoute goTo;

  	* -- * TrainRoute ;

 	 * -- * Passenger;

}

class PaymentMethod{}

class Ticket{isA PaymentMethod;}

class Presto { isA PaymentMethod;}

class Pass { isA PaymentMethod;}

class Payment{ 

  	* -- 1 Presto;

}



class Debit
{

  double balance;

  isA Payment;

}

class Credit
{

  double balance;

  public void getMoney (Bank a){}
  
  isA Payment;

}

class Bank
{

  double balance;

  public void notifyUser(Bank a){
  }

  	1 -- 1 Credit;

  	1 -- 1 Passenger Own;

}


![image](https://user-images.githubusercontent.com/47424577/67612255-07743e80-f76f-11e9-8218-dd02720279c3.png)


Part 2 Question 2 Object Diagram
![image](https://user-images.githubusercontent.com/47424577/67612010-cd09a200-f76c-11e9-8e73-53d07f8b20fd.png)