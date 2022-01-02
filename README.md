# Currency-Converter
@@ -19,20 +19,18 @@ public static void main(String[] args) {
        		Currency.userChoice();
        		break;
        	case 2:
        		convertDistance();
        		Distance.userChoice();
        		break;
        	case 3:
        		convertTime();
        		Time.userChoice();
        		break;
        	case 4:
        		break;
        	default:
        		System.out.println("Please choose valid option");
        		break;
        	}
        }
        System.out.println("Thank You !!!!");
    }

    public static void convertDistance(){

    }
    public static void convertTime() {

    }
}
  28  src/com/raja/oopslab/converters/Currency.java 
@@ -41,19 +41,39 @@ public static void userChoice(){
        	currency_choice = input.nextInt();
        	switch(currency_choice){
        	case 1:
        		System.out.println("Enter in DOLLERS");
        		System.out.println("Enter in DOLLER");
        		money = input.nextDouble();
        		System.out.println(money+" DOLLERS is equal to "+Currency.convertDOLLARtoINR(money)+" INDIAN RUPEES");
        		System.out.println(money+" DOLLER is equal to "+Currency.convertDOLLARtoINR(money)+" INR");
        		break;
        	case 2:
        		System.out.println("Enter in EURO");
        		money = input.nextDouble();
        		System.out.println(money+" EURO is equal to "+Currency.covertEUROtoINR(money)+" INDIAN RUPEES");
        		System.out.println(money+" EURO is equal to "+Currency.covertEUROtoINR(money)+" INR");
        		break;
        	case 3:
        		System.out.println("Enter in YEN");
        		money = input.nextDouble();
        		System.out.println(money+" YEN is equal to "+Currency.convertYENtoINR(money)+" INDIAN RUPEES");
        		System.out.println(money+" YEN is equal to "+Currency.convertYENtoINR(money)+" INR");
        		break;
        	case 4:
        		System.out.println("Enter in INR");
        		money = input.nextDouble();
        		System.out.println(money+" INR is equal to "+Currency.convertINRtoDOLLAR(money)+" DOLLORS");
        		break;
        	case 5:
        		System.out.println("Enter in INR");
        		money = input.nextDouble();
        		System.out.println(money+" INR is equal to "+Currency.covertINRtoEURO(money)+" EURO");
        		break;
        	case 6:
        		System.out.println("Enter in INR");
        		money = input.nextDouble();
        		System.out.println(money+" INR is equal to "+Currency.convertINRtoYEN(money)+" YEN");
        		break;
        	case 7:
        		break;
        	default:
        		System.out.println("Please choose valid option");
        		break;
        	}
        }
  43  src/com/raja/oopslab/converters/Distance.java 
@@ -1,5 +1,7 @@
package com.raja.oopslab.converters;

import java.util.Scanner;

public class Distance {
	public static double convertMeterToKiloMeter(double meter) {
		return meter / 1000;
@@ -16,4 +18,45 @@ public static double convertKiloMetertoMeter(double kilometer) {
	public static double convertKiloMeterToMiles(double kilometer) {
		return kilometer / 1.60934;
	}

	public static void userChoice(){
    	Scanner input = new Scanner(System.in);
        int distance_choice = 0;
        double distance = 0;
        while(distance_choice != 5){
        	System.out.println("\nDistance Converter");
        	System.out.println("------------------");
        	System.out.println("1. METER to KILOMETER\n2. MILES to KILOMETER\n"
        					 + "3. KILOMETER to METER\n4. KILOMETER to MILES\n"
        					 + "5.Exit\n\nEnter Your Choice");
        	distance_choice = input.nextInt();
        	switch(distance_choice){
        	case 1:
        		System.out.println("Enter in METERS");
        		distance = input.nextDouble();
        		System.out.println(distance+" METERS is equal to "+Distance.convertMeterToKiloMeter(distance)+" KILOMETER");
        		break;
        	case 2:
        		System.out.println("Enter in MILES");
        		distance = input.nextDouble();
        		System.out.println(distance+" MILES is equal to "+Distance.convertMilesToKiloMeter(distance)+" KILOMETER");
        		break;
        	case 3:
        		System.out.println("Enter in KILOMETER");
        		distance = input.nextDouble();
        		System.out.println(distance+" KILOMETER is equal to "+Distance.convertKiloMetertoMeter(distance)+" METER");
        		break;
        	case 4:
        		System.out.println("Enter in KILOMETER");
        		distance = input.nextDouble();
        		System.out.println(distance+" KILOMETER is equal to "+Distance.convertKiloMeterToMiles(distance)+" MILES");
        		break;
        	case 5:
        		break;
        	default:
        		System.out.println("Please choose valid option");
        		break;
        	}
        }
    }
}
 51  src/com/raja/oopslab/converters/Time.java 
@@ -1,19 +1,62 @@
package com.raja.oopslab.converters;

import java.util.Scanner;

public class Time {
	public static int convertHoursToMinutes(int hours) {
	public static double convertHoursToMinutes(double hours) {
		return hours * 60;
	}

	public static int convertHoursToSeconds(int hours) {
	public static double convertHoursToSeconds(double hours) {
		return hours * 60 * 60;
	}

	public static double convertMinutesToHours(int minutes) {
	public static double convertMinutesToHours(double minutes) {
		return minutes / 60;
	}

	public static double convertSecondsToHours(int seconds) {
	public static double convertSecondsToHours(double seconds) {
		return seconds / 60 / 60;
	}

	public static void userChoice(){
    	Scanner input = new Scanner(System.in);
        int time_choice = 0;
        double time = 0;
        while(time_choice != 5){
        	System.out.println("\nTime Converter");
        	System.out.println("-----------------");
        	System.out.println("1. HOURS to MINUTES\n2. HOURS to SECONDS\n"
        					 + "3. MINUTES to HOURS\n4. SECONDS to HOURS\n"
        					 + "5.Exit\n\nEnter Your Choice");
        	time_choice = input.nextInt();
        	switch(time_choice){
        	case 1:
        		System.out.println("Enter in HOURS");
        		time = input.nextDouble();
        		System.out.println(time+" HOURS is equal to "+Time.convertHoursToMinutes(time)+" MINUTES");
        		break;
        	case 2:
        		System.out.println("Enter in HOURS");
        		time = input.nextDouble();
        		System.out.println(time+" HOURS is equal to "+Time.convertHoursToSeconds(time)+" SECONDS");
        		break;
        	case 3:
        		System.out.println("Enter in MINUTES");
        		time = input.nextDouble();
        		System.out.println(time+" MINUTES is equal to "+Time.convertMinutesToHours(time)+" HOURS");
        		break;
        	case 4:
        		System.out.println("Enter in SECONDS");
        		time = input.nextDouble();
        		System.out.println(time+" SECONDS is equal to "+Time.convertSecondsToHours(time)+" HOURS");
        		break;
        	case 5:
        		break;
        	default:
        		System.out.println("Please choose valid option");
        		break;
        	}
        }
    }
}
