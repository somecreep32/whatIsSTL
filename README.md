# What Is STL?

**STL:**
Standard Template Library, or known as STL, is a collection of includes used in C++ to provide the programmer with data structures and functions. STL contain 4 template classes, algorithms, containers, functions and iterators. 

**Vectors in STL:**
In STL, vectors are concidered to be a sequence container which are data structures that can be accessed in a sequence type of manner.

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
