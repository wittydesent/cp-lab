
//program 1
#include<iostream>
using namespace std;

int main()
{
	int choice;
	cout << "Select one option: ";
	cout << "\n1. Find prime numbers in a given range.";
	cout << "\n2. Check if a specific number is prime."<<endl;
	cin >> choice;

	if (choice == 1)
	{
		int start, end;
    cout << "\nEnter the first number of the range = ";
    cin >> start;
    cout << "\nEnter the last number of the range = ";
    cin >> end;
    
    if (start >= 0 && end > start)
    {
        cout << "\nPrime numbers in the given range are:" << endl;
        for (int n = start; n <= end; n++)
        {
            bool prime_num = true;
            if (n == 0 || n == 1)
            {
                prime_num = false;
            }
            else
            {
                for (int i = 2; i <= n / 2; i++)
                {
                    if (n % i == 0)
                    {
                        prime_num = false;
                        break;
                    }
                }
            }
            if (prime_num)
            {
                cout << n << " ";
            }
        }
        cout << endl;
    }
    else
    {
        cout << "\nInvalid Range. ";
    }
	}
	else if (choice == 2)
	{
		int n;
		bool prime_num = true;
		cout << "Enter a positive number = ";
		cin >> n;

		if (n == 0 || n == 1)
		{
			prime_num = false;
		}
		else if (n > 1)
		{
			for (int i = 2; i <= n/2; i++)
			{
				if (n % i == 0)
					prime_num = false;
			}
		}
		else
		{
			cout << "Invalid data.";
		}

		if (prime_num)
		{
			cout << "It is a prime number.";
		}
		else
		{
			cout << "It is not a prime number.";
		}
	}
	else
	{
		cout << "Invalid choice.";
	}

	return 0;
}
