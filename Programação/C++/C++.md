
Print

```cpp
#include <iostream>
#define NUM 10
int main()
{
	int y;
	int x;
	float z;
	char letter = 'A';
	
	std::string name = "Raissa";
	std::cout << name << "\\n" << letter << "\\n" << NUM << "\\n";
	
	x = 5;
	y = 6;
	z = 6.12;
	std::cout << x << "\\n" << y << "\\n" << z;
	
	return 0;
}
```

NameSpace

```cpp
namespace first {
    int x = 1;
}

namespace second {
    int x = 2;
}

int main()
{
    int x = 2;

    std::cout << x << "\n" << first::x << "\n" << second::x;

}
```

Using NameSpace

```cpp
namespace first {
    int x = 1;
}

namespace second {
    int x = 2;
}

int main()
{
    using namespace first;

    std::cout << x << "\n";

}
```

- Só pode um using namespace por função

```cpp
namespace first {
    int x = 1;
}

namespace second {
    int x = 2;
}

int main()
{
    using namespace std;
    
    int x = 1;

    cout << x << "\n";

}               
```

Pode se usar name space std para cortar o std, não é indicado, std pode possui muitos elementos pode causar conflito

Solução mais segura:

```cpp
namespace first {
    int x = 1;
}

namespace second {
    int x = 2;
}

int main()
{
    using  std::cout;
    using  std::string;

    int x = 1;
    string y = " Hello";

    
    cout << x << y << "\n";

}
```

Typedef

```cpp

#include <iostream>

typedef std::string text_t; 
typedef int number_t;

int main()
{
    text_t text = "Hello";
    number_t num = 3;

    std::cout << text << num;
}
```

Typedef using

```cpp
#include <iostream>

using text_t = std::string;
using number_t = int; 

int main()
{
		text_t text = "Hello";
		number_t num = 3;
		std::cout << text << num;
}
```

Implicit Declaration

```cpp
#include <iostream>

int main()
{
    int num = 3.14;

    std::cout << num;
}
```

Explicit Declaration

```cpp

#include <iostream>

int main()
{
    float num = (int) 3.14;

    std::cout << num;
}
```

Lendo input

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "What is your name?: ";
    std::cin >> name;

    std::cout << "Hello " << name << "\n";
    
}
```

Lendo input com espaços

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "What is your name?: ";
    std::getline(std::cin, name);

    std::cout << "Hello " << name << "\n";
    
}
```

Lendo input após o enter 

```cpp
#include <iostream>

int main()
{
    std::string name;
    int age;

    std::cout << "What is your age: ";
    std::cin >> age;

    std::cout << "What is your name?: ";
    std::getline(std::cin >> std::ws, name);

    std::cout << "Hello " << name << "\n";
    
}
```

Funções matemáticas

```cpp
#include <iostream>
#include <cmath>

int main()
{
    float x = 3.13;
    float y = 4;
    float z;

    z = std::max(x, y);
    z = std::min(x, y);
    z = pow(2, 4);
    z = sqrt(9);
    z = abs(-3);
    z = round(x);
    z = ceil(x);
    z = floor(x);
    

    return 0;
}
```

If

```cpp
int main()
{
    int age;

    std::cout << "Please enter your age: ";
    std::cin >> age;

    if (age >= 18) {
        std::cout << "Fell free to enter" << "\n";
    }
    else {
        std::cout << "Get out baby" << "\n";
    }

    return 0;
}
```

Switch

```cpp
#include <iostream>
#include <cmath>

int main()
{

    int month;
    std::string monthName;
    std::cout << "Please enter the number of a month: ";
    std::cin >> month;

    switch(month){

        case(1):
            monthName = "January";
            break;
        case(2):
            monthName = "February";
            break;
        case(3):
            monthName = "March";
            break;
        default:
            monthName = "Invalid";
    }

    std::cout << "Your month is " << monthName << "\n";

}
```

Terminary Operators

```cpp
int main()
{
    //int grade;

    //std::cout << "Please entre your grade: ";
    //std::cin >> grade;

    //grade >= 60 ? std::cout << "You Pass \n" : std::cout << "You fail \n";

    int num;

    std::cout << "Give me a number: ";
    std::cin >> num;

    num % 2 == 0? std::cout << "Is even \n" : std::cout << "Is odd \n";

    return 0;

}
```

Forma mais legível

```cpp
int main()
{
    //int grade;

    //std::cout << "Please entre your grade: ";
    //std::cin >> grade;

    //grade >= 60 ? std::cout << "You Pass \n" : std::cout << "You fail \n";

    int num;

    std::cout << "Give me a number: ";
    std::cin >> num;

    std::cout << (num % 2 == 0? "Is even" : "Is odd") << "\n";
    return 0;

}
```

Métodos Strings

length()

```cpp
#include <iostream>

int main()
{
    
    std::cout << "Say your name: ";
    std::getline(std::cin, name);

    std::cout << name.length() << "\n";

}
```

empty()

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "Say your name: ";
    std::getline(std::cin, name);

    std::cout << name.length() << "\n";

    if (name.empty()) {
        std::cout << "Voce não inseriu um nome \n";
    }

}
```

clear()

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "Say your name: ";
    std::getline(std::cin, name);

    name.clear();

    std::cout << "Your name is: " << name << "\n";
}
```

append()

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "Say your name: ";
    std::getline(std::cin, name);

    name.append(" Feia");

    std::cout << "Name: " << name << "\n";
}
```

at()

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "Say your name: ";
    std::getline(std::cin, name);

    std::cout << name.at(0) << "\n";
}
```

insert() - insere um antes do index selecionado

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "Say your name: ";
    std::getline(std::cin, name);
    
    name.insert(0, "@");

    std::cout << name << "\n";
}
```

find() - Retorna o index da primeira ocorrência do caractere

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "Say your name: ";
    std::getline(std::cin, name);
    
    std::cout << name.find(' ') << "\n";   

}
```

erase() - Deleta os caracteres entre o index inicial e o final (não inclusivo)

```cpp
#include <iostream>

int main()
{
    std::string name;

    std::cout << "Say your name: ";
    std::getline(std::cin, name);
    
    name.erase(0, 3);

    std::cout << name << "\n";   

}
```

while empty 

```cpp
#include <iostream>

int main()
{
    std::string name;

    while(name.empty()) {
        std::cout << "Say your name: ";
        std::getline(std::cin, name);
    }

    std::cout << "Your name is: " << name << "\n";
}
```

Overloading Functions, funções com mesmo nome

```cpp
#include <iostream>

void bakePizza();
void bakePizza(std::string topping1);

int main()
{
    bakePizza();
    bakePizza("Peperroni");
}

void bakePizza()
{
    std::cout << "The pizza was baked \n";

}

void bakePizza(std::string topping1)
{
    std::cout << "The " << topping1 << " pizza was baked \n";
}

```

Usando funções do escopo global com mesmo nome do escopo local

```cpp
#include <iostream>

int num = 2;

int main()
{

    int num = 3;

    std::cout << ::num << "\n";

    return 0;

}

```

Alterando o output de floats para duas casas decimais

```cpp

#include <iostream>
#include <iomanip>

int main()
{
    std::cout << std::fixed << std::setprecision(2);
}
```

Verificando se o output é do tipo correto

```cpp
#include <iostream>
#include <iomanip>
#include <cmath>

int main()
{

    do{
        
        if (!std::cin >> choice) {
            std::cin.clear();
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        }

        displayMenuOptions();
        handleMenuOption(&choice, &balance);
    } while(choice != 4);

    return 0;
}

```

std::cin vai ler os caracteres do buffer e jogar pro choice

Se for números, converte pra int, e tudo certo

Se for letras, não converte, liga a flag de erro

Se tem flag de erro não consegue passar da stream pra variável

Limpa flags

Limpa buffer

for each loop

```cpp
#include <iostream>

int main()
{
    std::string students[] = {"Raissa","Isadora","Pedro"};

    for(std::string student : students){
        std::cout << student << '\n';
    }
}
```

fill()

```cpp

#include <iostream>

int main()
{
    std::string names[100];

    fill(names, names + 100, "Raissa");

    for (std::string name : names) {
        std::cout << name << "\n";
    }
}
```

Passing by reference

Referencia não pode ser Nula, e referencia não pode mudar de alvo

```cpp

#include <iostream>
    

int main()
{
    int x = 0;

    int& y = x;

    x++;
    y++;

    std::cout << x << "\n";
    std::cout << y << "\n";

}
```

Equivalência em ponteiros

```cpp
#include <iostream>
    

int main()
{
    int x = 0;

    int *y = &x;

    x++;
    (*y)++;

    std::cout << x << "\n";
    std::cout << *y << "\n";

}
```

```cpp
#include <iostream>
    
void add(int &baseValue, int addValue);

int main()
{
    int x = 10;

    add(x, 1);

    std::cout << x << "\n";

    return 0;
}

void add(int &baseValue, int addValue)
{
    baseValue += addValue;
}
```

Const em parâmetros

```cpp

#include <iostream>
    
void add(int &baseValue, const int addValue);

int main()
{
    int x = 10;

    add(x, 1);

    std::cout << x << "\n";

    return 0;
}

void add(int &baseValue, const int addValue)
{
    baseValue += addValue;
}
```

Evita LDA extras

Null pointer

```cpp

#include <iostream>
    
int main()
{
    int *pointer = nullptr;

    if(pointer == nullptr) {
        std::cout << "Address was not assigned!\n";
    }
    else {
        std::cout << "Address was assigned!\n";
    }

    return 0;
}
```

Ao usar new é obrigatório usar delete, o delete envolve mais coisas que apenas liberação de memória do sistema 

```cpp
#include <iostream>
    
int main()
{
    char *grades = NULL;
    int size;

    std::cout << "How many grades would you like to enter: ";
    std::cin >> size;

    grades = new char[size];

    for (int i = 0; i < size; i++) {
        std::cout << "Enter grade # " << i + 1 << ": ";
        std::cin >> grades[i];
    }

    for (int i = 0; i < size; i++) {
        std::cout << grades[i] << "\n";
    }

    delete[] grades;

    return 0;
}
```

Function Template

```cpp
#include <iostream>

template <typename T>

T max(T x, U y) {
    return (x > y)? x : y;
}
    
int main()
{

    std::cout << max(1, 2) << '\n';
    

    return 0;
}
```

Tipos diferentes vão precisar de templates diferentes e usar auto para retornar dependendo

```cpp
#include <iostream>

template <typename T, typename U>

auto max(T x, U y) {
    return (x > y)? x : y;
}
    
int main()
{

    std::cout << max(1, 2.1) << '\n';
    

    return 0;
}
```

Em C++ ENUMS não precisam de typdef

Class

```cpp
#include <iostream>
    
class Human {
    public:
        std::string name;
        std::string occupation;
        int age;

        void eat() {
            std::cout << name << "This person is eating\n";
        }
};

int main()
{   
    Human human1;

    human1.name = "Raissa";
    human1.occupation = "Desempregrada";
    human1.age = 18;

    human1.eat();

    return 0;
}
```

Construtores

```cpp
#include <iostream>
    
class Student {
    public:
        std::string name;
        int age;
        double gpa;

    Student(std::string name, int age, double gpa) {
        this->name = name;
        this->age = age;
        this->gpa = gpa;
    }
};

int main()
{
    Student student1("Raissa", 19, 0.01);

    std::cout << student1.name << "\n";
    std::cout << student1.age << "\n";
    std::cout << student1.gpa << "\n";
}
```

This é obrigatório se parâmetro do construtor tiver nome igual a atributos da classe

Se não for o caso pode se ocultar o this

```cpp

#include <iostream>
    
class Student {
    public:
        std::string name;
        int age;
        double gpa;

    Student(std::string x, int y, double z) {
        name = x;
        age = y;
        gpa = z;
    }
};

int main()
{
    Student student1("Raissa", 19, 0.01);

    std::cout << student1.name << "\n";
    std::cout << student1.age << "\n";
    std::cout << student1.gpa << "\n";
}
```

Overload Constructors

```cpp
#include <iostream>
 
class Pizza {
    public:
        std::string topping1;
        std::string topping2;

    Pizza() {

    }
    Pizza(std::string topping1) {
        this->topping1 = topping1;
    }
    Pizza(std::string topping1, std::string topping2) {
        this->topping1 = topping1;
        this->topping2 = topping2;
    }
};

int main() {

    Pizza pizza1("Pepperoni");
    Pizza pizza2("Pepperoni", "Mushrooms");
    Pizza pizza3;

    return 0;
}
```

Private: pode ser acessado só de dentro da classe

Public: pode ser acessado de qualquer lugar

Protected: pode ser acessado de dentro da classe e pelo seus filhos

Lidamos com private usando getters e setters

```cpp

#include <iostream>
 
class Stove {
    private:
        int temperature;

    public:
    Stove(int temperature) {
        setTemperature(temperature);
    }

    int getTemperature() {
        return temperature;
    }

    void setTemperature(int temperature) {
        if (temperature > 100) return;

        if (temperature < 0) return;

        this->temperature = temperature;
    }
};

int main() {
    Stove stove1(10);

    std::cout << stove1.getTemperature() << "\n"; 

    return 0;
}
```

Inheritance

```cpp
#include <iostream>
 
class Animal {
    public:
        bool alive = true;
    void eat() {
        std::cout << "HUMMMMMMMMM\n";
    }
};

class Dog : public Animal {
    public:

    void bark() {
        std::cout << "Eattttttt\n";
    }
};

class Cat : public Animal {
    public:

    void meow() {
        std::cout << "Meowwwwwwwww\n";
    }
};

int main() 
{
    Dog dog;

    dog.eat();
    dog.bark();

    return 0;
}

```