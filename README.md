# diziler-kullan-larak-sayilari-kücükten-büyüge-sıralama
#include<stdio.h>
#include<stdlib.h>
int main(void)
{
	int sinir,j,sakla,i;
	int dizi[100];
	
	printf("girilecek sayi adeti:");
	scanf("%d",&sinir);   
	//kac adete sayi girilecegi kullanicidan ogrenilir
	
	//kullanicidan sayilar alinir
	for(i=0;i<sinir;i++)
	{
		printf("%d)sayi giriniz ",i+1);
		scanf("%d",&dizi[i]);
	}
	//alinan sayilar ekrana yazdirilir
	printf("dizinin eski hali\n");
	for(i=0;i<sinir;i++)
	{
		printf("%d",dizi[i]);
		printf("\n\n");
	}
	
	for(i=1;i<sinir;i++)
	{
		sakla=dizi[i];
		j=i;
		while(j>0 && sakla<dizi[j-1])
		{
			dizi[j]=dizi[j-1];
			j--;
		}
		dizi[j]=sakla;
		
	}
	//dizinin siralanmis halini ekrana yazdirir
	printf("dizinin yeni hali\n");
	for(i=0;i<sinir;i++)
	{
		printf("%d",dizi[i]);
		printf("\n");
		
	}

	return 0;
	
}
