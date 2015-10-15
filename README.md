// Autor: Oscar Diego Ortiz Borda
// Fecha: 15/10/2015
#include "stdafx.h"
#include <iostream>
#include "conio.h"
#include "stdlib.h"

using namespace std;

void main()
{
	int N, opcion, NUMERO;
	float numero, suma, mayor, menor;
	do{
		cout<<"\t Menu \t\n";
		cout<<"1. Promedio de N numeros \n";
		cout<<"2. Mayor de N numeros \n";
		cout<<"3. Suma de dígitos \n";
		cout<<"0. Salir \n";
		cout<<"Opcion: ";
		cin>>opcion;
		switch(opcion){
		case 1:
			cout<<"Ingrese la cantidad de números: ";
			cin>>N;
			suma=0;
			for(int i=1; i<=N; i++){
				cin>> numero;
				suma=suma+numero;
			}
			cout<<"El promedio es: "<< suma/N;
			break;
		case 2:
			cout<<"Ingrese la cantidad de números: ";
			cin>>N;
			cin>>numero;
			mayor = numero;
			suma = numero;
			for(int i=1; i<=N-1; i++){
				cin>>numero;
				if(mayor<=numero)
					mayor=numero;
				else
				suma=suma+numero;
			}
			cout<<"El mayor es: "<<mayor<<"\n";
			break;
		case 3:
			cout<<"Ingrese el dígito: ";
			cin>>NUMERO;
			suma=0;
			while(NUMERO!=0){
				suma = suma + NUMERO%10;
				NUMERO = NUMERO/10;
			}
			cout<<"La suma de los digitos es: "<<suma;
			break;
		case 0:
			cout<<"Saliendo del programa \n";
			break;
		default: cout<<"Error al colocar opcion";
			break;
		}
		getch();
		system("cls");
	}while(opcion!=0);
	getch();
}
