// # Calculo_Combustible

#include<iostream>
#include <iomanip> 

using namespace std;
double Millas, Ppg, Km, z, costo, Mpg, precio = 234.30, g = 1;

int main()
{
	while (g == 1)
	{
	cout << "Calculemos el Precio de su viaje:" << endl ;
	cout << "Cual es su distancia a recorrer en Km? " << endl ;
	cin >> Km ;
	cout << "Digite las millas por galon de su vehiculo" << endl; 
	cin >> Mpg ;
	Millas = Km * 0.6221;  
	
	cout << "Sabe el precio de su combustible ?" << endl << "Si(1)" << endl << "No(2)" << endl ;
	cin >>  z ;
	
	if (z == 1)
	{
		cout << "Digite el precio del combustible por galon" << endl ;
		cin >> Ppg ; 
		costo = (Millas / Mpg) * Ppg ;
		cout << fixed << "Su costo del viaje es de " << setprecision(3) << costo << endl ;
	}
	
	if(z == 2)
	{
		costo = (Millas / Mpg) * precio ;
		cout << fixed << "Su costo del viaje es de " << setprecision(3) << costo << endl ;	
	}
	
	if(z!=1 and z!=2)
	{
		cout << "Valor no aceptado" ;
	}
	
	cout << "Desea continuar (1) ?" << endl ;
	cout << "Salir (0)" << endl ;
	cin >> g ; 
	}
return 0;
}
