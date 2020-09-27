# #include<bits/stdc++.h>
using namespace std;
class bank{ 
			private:
				char nm[20];
				int accno;
				char actype[10];
				float bal;
			public:
				bank(int acc_no,char*name,char*acc_type,float balance)
				{
					accno=acc_no;
					strcpy(nm,name);
					strcpy(actype,acc_type);
					bal=balance;
				}
				void Deposit();
				void Withdraw();
				void display();				
};
void bank::Deposit()
{
	int damt1;
	cout<<"Enter deposit amount: ";
	cin>>damt1;
	bal+=damt1;
}
void bank::Withdraw()
{
	int wamt1;
	cout<<"Enter Withdrawal Amount: ";
	cin>>wamt1;
	if(wamt1>bal)
	{
		cout<<"Withdrawal not possible !!!";
	}
	else{
		bal-=wamt1;
	}
}
void bank::display()
{
	cout<<"\n-----------------------";
	cout<<"\n Account Number: "<<accno;
	cout<<"\n Name: "<<nm;
	cout<<"\n Account Type: "<<actype;
	cout<<"\n Balannce: "<<bal;
}
int main()
{
	int acc_no;
	char name[100],acc_type[100];
	float balance;
	cout<<"\n Enter Details \n";
	cout<<"\n";
	cout<<"-------------------";
	cout<<"\n";
	cout<<"Account Number:  ";
	cin>>acc_no;
	cout<<"\n";
	cout<<"Name: ";
	cin>>name;
	cout<<"\n";
	cout<<"Account Type: ";
	cin>>acc_type;
	cout<<"\n";
	cout<<" Balance ";
	cin>>balance;
	cout<<"\n";
	bank b1(acc_no,name,acc_type,balance);
	b1.Deposit();
	b1.Withdraw();
	b1.display();
	return 0;
}
