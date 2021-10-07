# lab-3
Array and Vector manipulation 

#include <iostream>
#include <array>
#include <vector>
using namespace std;

int main()
{
//Question 1: 

    //declaring the two arrays 
    array<int,10> arr1= {1,2,3,4,5,6,7,8,9,10};
    array<int,10> arr2= {11,12,13,14,15,16,17,18,19,20};
    
    //prints the first and last element of array 1: 
    cout << "The first element in array 1 is:: " << arr1.front() << endl;
    cout << "The last element in array 1 is:: " << arr1.back() << endl; 
    
    //swap array 1 and array 2 values 
    arr1.swap(arr2);
    
    //prints the size of the arrays 
    cout << "\nThe size of the first array is: " << arr1.size() << endl;
    cout << "\nThe size of the second array is: " << arr2.size() << endl;
    
//Question 2: 
    int size, response;
    vector <int> ogVector;
    vector <int> copyVector;
    cout<< "What is the size of your vector? ";
    cin >> size;
    
    cout<< "\nEnter " << size << " variables  ";
    for(int i= 0; i <= size-1; i++)
    {
        cin >> response;
        ogVector.push_back(response); 
        copyVector.push_back(response);
    }
    
    sort(copyVector.begin(), copyVector.end());
    
    cout << "The unsorted vector is: ";
    for (int i=0; i <=size-1; i++)
    {
        cout << ogVector.at(i);
    }
    cout << endl;
    
    cout<< "The sorted vector is: ";
    for (int i=0; i <= size-1; i++)
    {
        cout << copyVector.at(i);
    }
    cout << endl;
    

    //Part B: 
    int newSize= 100;
    int minSize= 10;
    vector<int> vector1;
    vector<int> vector2= {10,13,60,43,55,20,17,80,33,28};
    
    for(int i=0; i<= newSize -1; i++)
    {
        vector1.push_back(i*2);
    }
    
    int coutIn= 0;
    int coutOut= 0;
    double contained, notContained; 
    
    for(int j=0; j< 10; j++)
    {
        if(count(vector1.begin(),vector1.end(), vector2.at(j)))
        {
            coutIn++;
        }
        else
        {
            coutOut++;
        }
    }

    contained= 100/coutIn;
    cout << "The percent of elements from vector 2 that are in vector 1 is: " << contained << "%" << endl;
    
    notContained= 100/coutOut;
    cout << "The percent of elements from vector 2 that are not in vector 1 is: " << notContained << "%" << endl;
    
    //Part C
    vector<int> vector3= {1,2,3,4,5};
    vector<int> vector4= {6,7,8,9,10};
    
    if(vector3 == vector4)
    {
        cout << "\nBoth vectors are equal!" << endl;
    }
    else
    {
        cout << "The vectors are not equal!" << endl; 
    }

    //Part D
    vector<int>vector5={3,5,4,3,6,4,3,6,8};
    int repeat= 3;
    int myCount=0;
    
    myCount= count(vector5.begin(),vector5.end(),3);

    cout << "The amount of times " << repeat << " occures is: " << myCount <<endl;
    
    //Part E

    
    return 0;
}
