#  7pz2 Практична робота 2
Варіант 15
<img width="660" height="55" alt="image" src="https://github.com/user-attachments/assets/02982f58-efdb-4468-b85e-33ad6f8853be" />

# 😉Завдання 1
## <img width="443" height="175" alt="image" src="https://github.com/user-attachments/assets/98f645bc-845f-4891-b650-9e2ed1ba94e5" />
```cpp
#include <iostream>
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
}
```
# 😘 Завдання 2
## <img width="470" height="196" alt="image" src="https://github.com/user-attachments/assets/6c17be83-f7c9-4cb2-aa96-06505bad91c0" />

```cpp
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main()
{
    forward_list<string> 
    online_stores = { "Brain" };
    online_stores.push_front("EVA");
    online_stores.push_front("Rozetka");
    
    cout << "Список інтернет-магазинів:" << endl;
    for (string store : online_stores)
    {
        cout << store << endl;
    }
    
    online_stores.pop_front();
    
    cout << endl; 
    
    cout << "Після видалення першого елемента:" << endl;
    for (string store : online_stores)
    {
        cout << store << endl;
    }

    return 0;
}
```
# 😎 Завдання 3
## <img width="1772" height="471" alt="image" src="https://github.com/user-attachments/assets/6277864d-401f-4484-8843-cd99bb8fe3fb" />

```cpp
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main()
{
    forward_list<string> online_stores = {
        "Brain",
        "Rozetka",
        "EVA",
        "Фокстрот",
        "Comfy"
    };
    
    string searchStore;
    cout << "Введіть назву інтернет-магазину для пошуку:" << endl;
    cin >> searchStore;
    
    auto it = online_stores.begin();
    while (it != online_stores.end())
    {
        if (*it == searchStore)
        {
            cout << "Елемент знайдено";
            break;
        }
        ++it;
    }
    
    if (it == online_stores.end())
    {
        cout << "Елемент не знайдено";
    }

    return 0;
}
```
#🎄 Завдання 4 
## <img width="1632" height="505" alt="image" src="https://github.com/user-attachments/assets/77ad5a7d-793a-4a33-8a2b-f62b7319256b" />

```cpp
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main()
{
    forward_list<string> online_stores = {
        "Brain",
        "Rozetka",
        "EVA",
        "Фокстрот",
        "Comfy"
    };
    
    int sum = 0;
    
    for (string store : online_stores)
    {
        sum = sum + store.length();
    }
    
    cout << "Загальна кількість символів: " << sum;

    return 0;
}
```
# 🎇 Завдання 5 
## <img width="1756" height="625" alt="image" src="https://github.com/user-attachments/assets/bc161493-5aee-4a5a-8ca0-b5a424aef9ad" />

```cpp
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main()
{
    forward_list<string> online_stores = { "Brain", "Rozetka", "EVA", "Фокстрот", "Comfy" };
    
    string searchElement = "EVA";
    string newElement = "Epicentr";
    
    auto it = online_stores.begin();
    while (it != online_stores.end())
    {
        if (*it == searchElement)
        {
            online_stores.insert_after(it, newElement);
            break;
        }
        ++it;
    }
    
    if (it == online_stores.end())
    {
        cout << "Елемент не знайдено" << endl;
    }
    
    for (auto i = online_stores.begin(); i != online_stores.end(); ++i)
    {
        cout << *i << " ";
    }

    return 0;
}
```
