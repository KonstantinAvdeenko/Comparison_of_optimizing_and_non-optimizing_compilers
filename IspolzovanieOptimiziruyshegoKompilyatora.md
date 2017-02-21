#include <iostream>
#include <cstdlib>
#include <ctime>
#include <stdlib.h>
#include <cmath>                 
using namespace std;
 
int main(int argc, char* argv[])
	
{   srand (time(0)); // засекается время начала выполнения программы
	
    double  f, i, N, y, x;
	
    N = 100000000; // количество раз выполнения цикла для функции
	x = rand() % 1 +10; // рандомное число от 1 до 10 для задания переменной «х»
    y=0;
	i = 1;
             for (i=1; i<=(N); i++) { 
                     y+= (cos(x+i)) * pow(x,(1/i)); } 

    cout << "y=" << y << endl; //результат выполнения функции
    cout << "runtime = " << clock()/1000.0 << endl; // останавливается и выводится время выполнения программы в микросекундах                 
    system("pause");
    return EXIT_SUCCESS;
    
}
