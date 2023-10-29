#include<iostream>
using namespace std;
class account
{
private:
    string name;
    int accno;
    string mailid;
public:
    void  getAccountDetails()
    {
        cout<<"\nEnter Customer Name : ";
        cin>>name;
        cout<<"Enter Account Number  : ";
        cin>>accno;
        cout<<"Enter The Mail ID   : ";
        cin>>mailid;
    }
    void displayDetails()
    {
        cout<<"\n\nCustomer Name : "<<name;
        cout<<"\nAccount Number  : "<<accno;
        cout<<"\nThe Mail ID  : "<<mailid;
    }
};

class saving_account : public account
{
private:
    float savebalance = 0;
public:
    void s_display()
    {
        cout<<"\nBalance :  "<<savebalance;
    }
    void s_deposit()
    {
        float deposit,interest;
        cout<<"\nEnter amount to Deposit :  ";
        cin>>deposit;
        savebalance = savebalance + deposit;
        interest=(savebalance*2)/100;
        savebalance=savebalance+interest;
    }
    void s_withdraw()
    {
        float withdraw;
        cout<<"\nBalance :- "<<savebalance;
        cout<<"\nEnter amount to be withdraw : ";
        cin>>withdraw;
        if(savebalance > 500)
        {
            savebalance=savebalance-withdraw;
            cout<<"\nBalance Amount After Withdraw: "<<savebalance;
        }
        else
        {
            cout<<"\n Insufficient Balance and need a neccessary balance of ₹500";
        }
    }
};
int main()
{
    saving_account s1;
    char type;
    cout<<"\nEnter S To Start your Transaction  : ";
    cin>>type;
    int choice;
    if(type=='s' || type=='S')
    {
        s1.getAccountDetails();
        while(1)
        {
            cout<<"\nChoose Your Choice"<<endl;
            cout<<"1)   Deposit"<<endl;
            cout<<"2)   Withdraw"<<endl;
            cout<<"3)   Display Balance"<<endl;
            cout<<"4)   Display with full Details"<<endl;
            cout<<"5)   Exit"<<endl;
            cout<<"Enter Your choice: ";
            cin>>choice;
            switch(choice)
            {
                case 1 :
                    s1.s_deposit();
                    break;
                case 2 :
                    s1.s_withdraw();
                    break;
                case 3 :
                    s1.s_display();
                    break;
                case 4 :
                    s1.displayDetails();
                    s1.s_display();
                    break;
                case 5 :
                    goto end;
                default:
                    cout<<"Entered choice is invalid,TRY AGAIN";
            }
        }
    }
    else
    {
        cout<<"\nERROR OCCURED IN SELECTION";
        end:
        cout<<"\nTHANK YOU FOR USING OUR BANK !!";
    }
    return (0);
}
