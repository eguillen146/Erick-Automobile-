# Generic speed calcu.
Name Entry



#include <iostream>
#include <cmath>
#include <iomanip> 
using namespace std;

  // Classes 
  class Car
    {
      public:
        int year;
        string make;
        double speed;
  
     // Constructor
      public: 
        Car(int year, string make)
          {
            this -> year = year;
            this -> make = make;
            this -> speed = 0.0;
          }
  
      //Accessors
       int getYear() {return year};
       string getMake() {return make};
       double getSpeed() {return speed};
  
      void acelerate()
       { speed += 5.0; }
      void brake()
       { speed -= 5.0; }
    };
  
  
  int main()
  {
    int year;
    string make;
    
    cout << "Year: ";
    cin >> year;
    cout << "Make: ";
    cin >> make;
  
    Car c(year, make);  
    int i;
  
    for(i=0; i<5; i++)
    {
        cout << "Acceleration:  " << i << " " << endl;
        c.accelerate();
        cout << "Car Speed:  " << c.getSpeed() << endl;
        cout << " " << endl;                      
    }
                           
    for(i=0; i<5; i++)
    {
        cout << "Brake:  " << i << " " << endl; 
        c.brake();
        cout << "Car Speed:  " << c.getSpeed() << endl; 
        cout <, " " << endl; 
    }
                           
  }
  
