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
       }
       void inputMoney(double money, int ch)
       {
          double cost = drink[ch-1]->price;
          string name = drinks[ch-1]->name;
          int q=drinks[ch-1]->quan;
          char cho;
  
          if(money >= cost)
          {
            if (q == 0)
               {
                   cout<< name <<" is sold out!!";
               }
               else
               {
                   cout<<"\nDo you want to buy "<< name <<" for :"<<cost<<" (y / n) : ";
                   cin>>cho;
                  
                   if (cho != 'n' && cho != 'N')
                   {
                       cout<<"Beevrage Dispensed : "<< name <<endl;
                      
                       drinks[ch - 1]->quantity--;
                       moneyCollected += cost;
                      
                       if (money-cost != 0)
                       cout << "Change: " << money - cost << "\n\n";
                   }
                   else
                   {
                       cout << "Money returned: " << endl;
                   }
      
               }
           }
           else
           {
               cout<<"\n  Need more money" << endl;
               cout<<"Here is your money back!\n\n";
           }
       }
      
       void dailyReport()
       {
           cout<<" Daily Report : \n\n";
           for (int i = 0; i < numOfDrinks; i++)
           {
               int q = drinks[i]->quantity;
               if (q > 0)
                   cout<<drinks[i]->name<<" left : "<< q <<endl;
           }
           cout<<"\nMoney collected : "<< moneyCollected <<"\n\n";
       }
      
  };
  
  
  int main()
  {
    BevMachine machine;
  
    machine.displayChoices():
    machine.displayChoices();
    machine.displayChoices
    machine.dailyReport();
  
    return 0;
  }
  
  
