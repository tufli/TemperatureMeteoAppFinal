# TemperatureMeteoAppFinal
package com.company;
import java.util.Random;

class Main {
    public static void main(String[] args){
        OpenMeteoProvider.getCurrentTemperature(4);
        PrivateMeteoProvider.getCurrentHumidity(4);

    }
}

class OpenMeteoProvider {

    static double max = 50.0;
    Random random = new Random();
    static double rand = -50.0 + new Random().nextInt(100);

    static double getCurrentTemperature( int countryCode ){
if ((countryCode == 4) ||(countryCode == 8)||(countryCode == 12)||(countryCode == 16)||(countryCode == 20)) {
    System.out.println("In this country, current temperature is :"+ rand +" degrees. " );
} else{
        System.out.println("err: Can't provide data for this country!");
        }
        return 0;
    }
}

class PrivateMeteoProvider extends OpenMeteoProvider{
    static double max = 100;
    Random random = new Random();
    static double rand = 0 + new Random().nextInt(100);
    static byte getCurrentHumidity (int countryCode){
        if ((countryCode == 4) ||(countryCode == 8)||(countryCode == 12)||(countryCode == 16)||(countryCode == 20)) {
            System.out.println("Cureent humidity is :"+ rand+ "%");
        } else{
            System.out.println("err: Can't provide data for this country!");
        }
        return 0;
    }


}