#include <stdio.h>
#include <stdlib.h>
#include <string.h>

char a[100][7][100];
char lg[100][2][50];
int p,l,v,su[100];
int j,k;

void Register();
void Password();
void Login();
void Screen_traveller();
void Modify();
void Pass();
void View();
void Search();
void Sort();

int main() {

	char ch1[20];
	
	k=0;
	for( ; ;){
		do{
			do{
				printf("Do you want to Register or Login?\nPlease enter your choice.\n");
				scanf(" %s",&ch1);

				system("cls");
			}while ((strcmp(ch1,"Register")!=0) && (strcmp(ch1,"Login")!=0));

			if(strcmp(ch1,"Register")==0)
				if(k<100) 
					Register();
				else
					printf("The system is full, please try to login");
			else{
				Login();
				break;
			}
		}while(1);
		Screen_traveller();
	}

	return 0;
}

void Register (){
	int f,x,sum,age;

	printf("Please insert your personal data below:\n");
	do{
		/*Diavazoume to epitheto pou eisagei o xrhsths*/
		printf("Surname:\t");
		scanf(" %s", a[k][0]);

		x=0;
		while(x<k){
			if((strcmp(a[k][0],a[x][0])==0)){ 
				printf("This surname already exists!\nPlease enter another one.\n");
				break;
			}
			else 
				x++;
		}
		
		if(x<k)
			continue;
		else 
			break;
			
	}while(1);

	printf("Name:\t");
	scanf(" %s", a[k][1]);

	do{
		printf("Age:\t");
		scanf(" %d",&age);
	
	}while(age<0);
	
	sprintf(a[k][2],"%d",age);

	do{
		printf("Total trips to Lamia:\t");
		scanf(" %d",&l);
		
	}while(l<0);

	do{
		printf("Total trips to Patra:\t");
		scanf(" %d",&p);

	}while(p<0);

	do{
		printf("Total trips to Volos:\t");
		scanf(" %d",&v);

	}while(v<0);

	system("cls");

	sum=p+l+v;
	su[k]=sum;
  sprintf(a[k][3],"%d",l);
	sprintf(a[k][4],"%d",p);
	sprintf(a[k][5],"%d",v);
	sprintf(a[k][6],"%d",sum);
	
	Password();
	
	k++; 
	
	system("cls");
}

void Password(){
	char table[20];
	
  	strcpy(table,a[k][0]);
	strcpy(lg[k][0],table);
	strcpy(lg[k][1],strcat(table,a[k][6]));

	printf("\nYour username is: '%s'\n",lg[k][0]);
	printf("Your password is: '%s'\n",lg[k][1]);
	system("pause");
}

void Login(){
	char username[50],password[50];
	int x;
	
	do{
		printf("Insert your username and your password to enter:\n");
		printf("Username:\t");
		scanf(" %s",&username);
		printf("Password:\t");
		scanf(" %s",&password);

		x=0; 
		while(x<k){ 
			if(strcmp(lg[x][0], username)==0 && strcmp(lg[x][1], password)==0){
				j=x;
				break;
			}
			else
				x++;
		}
	
		if(x<k)
			break;	
	}while(1);
	system("cls");
}

void Screen_traveller(){
	char ch2[20];

	do{
		do{
			printf("Welcome to the Screen Traveller\n");
			printf("Please enter Modify, Pass, View, Search, Sort or Exit:\n");
			scanf(" %s", ch2);

			system("cls");
		}while ((strcmp(ch2,"Modify")!=0) && (strcmp(ch2,"Pass")!=0) && (strcmp(ch2,"View")!=0) && (strcmp(ch2,"Search")!=0) && (strcmp(ch2,"Sort")!=0) && (strcmp(ch2,"Exit")!=0));
		
		system("cls");
		if(strcmp(ch2,"Modify")==0)
			Modify();

		else if(strcmp(ch2,"Pass")==0)
			Pass();

		else if(strcmp(ch2,"View")==0)
			View();

		else if(strcmp(ch2,"Search")==0)
			Search();

		else if(strcmp(ch2,"Sort")==0)
			Sort();

		else if(strcmp(ch2,"Exit")==0)
			break;

	}while(1);
}

void Modify(){
	int f,x,ch,age,sum;
	do{
		printf("What do you want to change from your personl data?\nChoose a number between 1 and 6\n1: Surname\n2: Name\n3: Age\n4: Total trips to Lamia\n5: Total trips to Patra\n6: Total trips to Volos\n");
		scanf(" %d",&ch);
	}while(ch<1 || ch>6);

	if(ch==1){
		do{
			printf("Surname:\t");
			scanf(" %s", a[j][0]);

			x=0;
			while(x<k){
				if((strcmp(a[j][0],a[x][0])==0)){ 
					printf("This surname already exists!\nPlease enter another one.\n");
					break;
				}
				else 
					x++;
			}
		
			if(x<k) 
				continue;
			else 
				break;
		}while(1);
	}
	
	if(ch==2){
		printf("Name:\t");
		scanf(" %s",a[j][1]);
	}

	if(ch==3){
		do{
			printf("Age:\t");
			scanf(" %d",&age);
		}while(age<0);
		
		sprintf(a[j][2],"%d",age);
	}
	
	if(ch==4){
		do{
			printf("Total trips to Lamia:\t");
			scanf(" %d",&l);
		}while(l<0);
	}

	if(ch==5){
		do{
			printf("Total trips to Patra:\t");
			scanf(" %d",&p);
		}while(p<0);
	}
	
	if(ch==6){
		do{
			printf("Total trips to Volos:\t");
			scanf(" %d",&v);
		}while(v<0);
	}
	
	system("cls");

	sum=p+l+v;
	su[j]=sum;
	sprintf(a[j][3],"%d",l);
	sprintf(a[j][4],"%d",p);
	sprintf(a[j][5],"%d",v);
	sprintf(a[j][6],"%d",sum);

	printf("Your username is: '%s'\n",lg[j][0]);
	printf("Your password is: '%s'\n",lg[j][1]);
	system("pause");
	system("cls");
}

void Pass(){
	int b,p;
	
	if(su[j]>20){
		su[j]=su[j]-5;
		sprintf(a[j][6],"%d",su[j]);
		b=5;
		do{
			if(l>1){ 
				l=l-1;
				b=b-1;
				sprintf(a[j][3],"%d",l);
			}
			if(p>1){
				p=p-1;
				b=b-1;
				sprintf(a[j][4],"%d",p);
			}
			if(b>=1){ 
				if(v>1){
					v=v-1;
					b=b-1;
					sprintf(a[j][5],"%d",v);
				}
			}

		}while(b!=0);
	

		printf("Please enter the first two new characters from your password:\n");
		scanf(" %c %c",&lg[j][1][0],&lg[j][1][1]);
		printf("Your new password is: %s\n", lg[j][1]);
		system("pause");
		system("cls");
	}
	else{
		printf("You can't have acess to Pass because you have less than 20 trips\n");
		system("pause");
		system("cls");
	}
}

void View(){ 
	int s,t; 
	for(s=0; s<k; s++){
		for(t=0; t<7; t++){
			printf("%s\t",a[s][t]); 
		}
		printf("\n"); 
	}
	system("pause");
	system("cls");
}

void Search(){
	int s,t,n;
	
	do{		
		printf("Please enter a number of total trips:\n"); 
		scanf(" %d",&n);
	}while(n<0);
		

	for(s=0; s<k; s++){
		if(n==su[s]){
			printf("%s\t",a[s][0]);
			printf("%s\t",a[s][1]);
			printf("%s\n",a[s][6]);
		}
		else
			printf("There is no traveller with these number of trips");
	}
	system("pause");
	system("cls");	
}

void Sort(){
	int s,t,y;
	char temp[20];
	
	for(s=1; s<k; s++){
		for(t=k-1; t>=s; t--){
			if(su[s-1]<su[s]){
				strcpy(temp,a[s][0]);
				strcpy(a[s][0],a[s-1][0]); 
				strcpy(a[s-1][0],temp); 
				
				strcpy(temp,a[s][1]);
				strcpy(a[s][1],a[s-1][1]);
				strcpy(a[s-1][1],temp);
					
				strcpy(temp,a[s][2]);
				strcpy(a[s][2],a[s-1][2]);
				strcpy(a[s-1][2],temp);
				
				strcpy(temp,a[s][3]);
				strcpy(a[s][3],a[s-1][3]);
				strcpy(a[s-1][3],temp);
				
				strcpy(temp,a[s][4]);
				strcpy(a[s][4],a[s-1][4]);
				strcpy(a[s-1][4],temp);
				
				strcpy(temp,a[s][5]);
				strcpy(a[s][5],a[s-1][5]);
				strcpy(a[s-1][5],temp);
							
				strcpy(temp,a[s][6]);
				strcpy(a[s][6],a[s-1][6]);
				strcpy(a[s-1][6],temp);
				
				strcpy(temp,lg[s][0]);
				strcpy(lg[s][0],lg[s-1][0]);
				strcpy(lg[s-1][0],temp);
					
				strcpy(temp,lg[s][1]);
				strcpy(lg[s][1],lg[s-1][1]);
				strcpy(lg[s-1][1],temp);
				
				y=su[s-1];
				su[s-1]=su[s];
				su[s]=y;
			}
		}
	}
				
	for(s=0; s<k; s++){ 
		for(t=0; t<7; t++){
			printf("%s\t", a[s][t]);
		}
		printf("\n");
	}
	system("pause");
	system("cls");
}
