# 7pz2
Завдання 1
<img width="443" height="175" alt="image" src="https://github.com/user-attachments/assets/98f645bc-845f-4891-b650-9e2ed1ba94e5" />
''#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main()
{
    forward_list<string> 
    online_stores = { "Brain", "Rozetka", "EVA", "Фокстрот", "Comfy" };
    
    cout << "Інтернет-магазини:" << endl;
    for (string store : online_stores)
    {
        cout << store << endl;
    }

    return 0;
}''
