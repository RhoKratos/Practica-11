#include <stdio.h>
#include <string.h>
#include <ctype.h>
#include <stdlib.h>

int main(){
	
	char cadena[50];
	int i;
	FILE*archivo = fopen("archivo.txt","a");
	
	printf("Teclea una cadena:");
	gets(cadena);
	
	printf("%s", cadena);
	
	for(i=0;i<strlen(cadena);i++){
		if(i==0){
			cadena[i]=toupper(cadena[i]);
		}
		if(cadena[i]==' '){
			cadena[i]='-';
			cadena[i+1]=toupper(cadena[i+1]);
		}
	}
	
	printf("\n%s", cadena);
	fprintf(archivo,"\n%s", cadena);
	
	fclose(archivo);
	scanf("%d");
	
	return 0;
}

