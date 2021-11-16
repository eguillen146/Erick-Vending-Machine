# Erick-Vending-Machine
Drink Vending Machine

  #include <iostream>
  #include <cmath>
  #include <iomanip>
  
  using namespace std;
  
  struct Bev  // Bev = Beverage
  {
    string name;
    double price;
    int quan; // quan = quantity
    
    public: 
      Beverage (string name, double price, int quan)
        {
          this-> name = name;
          this-> price = price;
          this-> quan = quan;
        }
  };
  
  class BevMachine
  {
    private: float moneyCollected;
    protected: Bev*drinks[100];
    protected: int numOfDrinks;
    
    public: 
      BevMachine()
        {
           this-> drinks[0] = new Beverage("Cola", 1.00, 20)
           this-> drinks[1] = new Beverage("root Beer", 1.00, 20)
           this-> drinks[2] = new Beverage("Orange Soda", 1.00, 20) 
           this-> drinks[3] = new Beverage("Grape Soda", 1.00, 20) 
           this-> drinks[4] = new Beverage("Bottled Water", 1.00, 20) 
            
            this-> numOfDrinks = 5;
            this-> moneyCollected = 0.0;
        }
    void displayChoices()
      {
        int ch;
        double money;
  
        cout<<i + 1<<". "<<left<<setw(15)<<drinks[i]->name;
        cout<<"   $ "<<drinks[i]->price;<< endl;
      }
       cout << \n Select Number(1- "numOfDrinks) : "; 
       cin >> ch;
       if (ch >= 1 && ch <= numOfDrinks)
           {
               //asks the user to enter the money
               cout<<" Insert money: " << endl;
               cin>>money;
               inputMoney(money, ch);
           }
           else
           {
               cout<<"\nInvalid choice:" << endl;
           }
  
  
  
  
  
  
  
  int main()
  {
    getBevMachine();
  }
  
  
