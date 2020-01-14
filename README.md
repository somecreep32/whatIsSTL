# What Is STL?

**STL:**
Standard Template Library, or known as STL, is a collection of includes used in C++ to provide the programmer with data structures and functions. STL contain 4 template classes, algorithms, containers, functions and iterators. 

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
        std::cout << *i << " "; 

}
```

This means that if needed, the vector can hold more than 5 values or less than 5 values if necessary. In the example above, it displays how many species of bear fight over 1 single twinkie. Vectors are much more useful in situations where outputs are not guarenteed to be exactly fitting for the array. Think of vectors as saftey netting, if the main system doesn't work, then the saftey net can prevent it from breaking and keep the system functioning.

**Maps in STL:**
Maps within STL are associative containers that 'map' data and store in an order.
```cpp
#include <iostream>
#include <map>
#include <iterator>


```

**Sets in STL:**
Sets are described as associative containers
```cpp
#include <iostream>

```
