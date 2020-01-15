# What Exactly Is STL?

**STL:**
Standard Template Library, or known as STL, is a collection of header files(#include<iostream>) used in C++ to provide the programmer with data structures and functions. STL contain 4 template classes, algorithms, containers, functions and iterators. 

**Vectors in STL:**
In STL, vectors are concidered to be a sequence container which are data structures that can be accessed in a sequence type of manner. Vectors are very similar to arrays; however, arrays can only store a certain amount of data. With vectors, they practically have a yield system built into them, which allows for more or less of a data set.

```cpp
#include <iostream>
#include <vector>

int main(){
    
    std::vector<int> twinkies;
    
    for (int i = 1; i <= 5; i++){
        twinkies.push_back(i);
    }
    
    std::cout << "The bear species fighting for the twinkies: "; 
    for (auto i = twinkies.begin(); i != twinkies.end(); ++i) 
        std::cout<<"Species "<<*i<<", "; 

}
```

This means that if needed, the vector can hold more than 5 values or less than 5 values if necessary. In the example above, it displays how many species of bear fight over 1 single twinkie. Vectors are much more useful in situations where outputs are not guarenteed to be exactly fitting for the array. Think of vectors as saftey netting, if the main system doesn't work, then the saftey net can prevent it from breaking and keep the system functioning.

**Maps in STL:**
Maps within STL are associative containers that 'map' data and store in an order. The way a default map is outputted is similar to those of a table in algebraic equations. An input and an output, and xy table as you may.
```cpp
#include <iostream>
#include <map>
#include <iterator>

std::map<int, double> monthlyProfits;

int main(){
    
    monthlyProfits.insert(std::pair<int, double>(1, 242.24));
    monthlyProfits.insert(std::pair<int, double>(2, 361.63));
    monthlyProfits.insert(std::pair<int, double>(3, 651.96));
    monthlyProfits.insert(std::pair<int, double>(4, 999.99));
    
    std::map<int, double>::iterator it;
    std::cout<<"ADMINISTRATION.SYS\n"
        <<"\tMonth One Profits:\n"
        <<"\t\tWEEK:\t\t\tPROFIT:\n";
    for (it=monthlyProfits.begin(); it!=monthlyProfits.end(); ++it){
        std::cout<<"\t\t"<< it->first
        <<"\t\t\t" << it->second<<"\n";
    }
    return 0;
}
```
Maps have a heavy use of iterators, which are units designed in programming to, as the name implies, "iterate" throughout a dataset or table. The "it->first" is telling the iterator to iterate through the first key, in this case the week number, and "it->second" tells the iterator to iterate through the value, the profit amount. Whenever we are doing 'it->first', we are saying to the system: "Hey let's find the first set of the pairs that we are trying to output", which means in this example we are looking at the key, or in our case the week number. Realitively same thing in this example, except we are looking for the seconds value the element or the weekly sales. Maps are intended as their name, they can 'map' out the data to plot numerous pairs of keys and elements to project data.

**Sets in STL:**
Sets are described as associative containers that identify themselves based on the value of the element. These can be very similar to an array; however, the array organization is rather instant. This can get more in depth from the example procided below.
```cpp
#include <iostream>
#include <iterator>
#include <set>

std::set<long, std::greater <long>> chipsSet;

int main(){
    chipsSet.insert(203);
    chipsSet.insert(441);
    chipsSet.insert(356);
    chipsSet.insert(314);
    chipsSet.insert(314);
    chipsSet.insert(262);
    
    std::set<long, std::greater<long>>::iterator it;
    std::cout<<"Weekly Inventory:\n"<<"\tChips Each Day:";
    for (it = chipsSet.begin(); it != chipsSet.end(); ++it){ 
        std::cout<<"\n\t\t"<<*it; 
    } 
    return 0;
}
```
Sets relate closely to a map or an array. Sets sort all of the values in numerical order, letter order if used strings. If you notice, the value '314' is inserted twice to try and trick the system. Due to set's structure, the sets remember the values they receive via .insert, and recognize if a value is repeated. Therefore, at the output image, 314 is not only in it's chronological order, but also is only within the table once. Sets can be used for what's in the example, an inventory system. In inventory or register counting, values have a high propbablilty of being closely related, having a wide varity of data, and or representing data as a chronological way to overview sales or income.
