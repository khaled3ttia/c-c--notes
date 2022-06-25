## C++ : Functions with varying parameters

### Initializer List

Better used when all arguments have the same type. 

Example:

```
    #include <initializer_list>

    // Function definition
    // initializer_list type takes a template arg 
    //                      for the type of params
    int add(std::initializer_list<int> params){
        int sum = 0;
        for (auto param: params){
            sum += param;
        }
        return sum;
    }

    int main(){
        
        // Calling the function (notice the curly braces)
        int sum = add({1,2,3,4,10});
        std::cout << "Sum=" << sum << std::endl;

        sum = add({5,13});
        std::cout << "Sum=" << sum << std::endl;
    }

```
