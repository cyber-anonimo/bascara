# bascara

#include<iostream>
#include<cmath>
using namespace std;
int main (){
	
	float a, b, c, delta, x1, x2;

    cout << "Coeficiente a: ";
    cin >> a;

    cout << "Coeficiente b: ";
    cin >> b;

    cout << "Coeficiente c: ";
    cin >> c;

    if(a != 0){
        delta = (b*b) - (4*a*c);

        if(delta<0){
            cout <<"Nao tem raizes reais\n";
        }
        else if (delta==0){
            x1=(-b)/(2*a);
            cout << "Possui apenas uma raiz real: "<< x1 << "\n";
        }else{
            x1=(-b - sqrt(delta))/(2*a);
            x2=(-b + sqrt(delta))/(2*a);
            cout << "Raiz 1: "<< x1 << "\n";
            cout << "Raiz 2: "<< x2 << "\n";
        }
    }else{
        cout <<"a=0, não é uma equação do segundo grau\n";
    }
	
	return 0;
}
//https://www.cmmprogressivo.net/2019/10/Equacao-2-grau-Cpp-Bhaskara-Como-resolver.html
