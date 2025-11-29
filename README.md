#include<stdio.h>

int main () {
	FILE *fptr;
	fptr = fopen("Test.txt","w");
	fprintf(fptr,"%s","Brave");
	fclose(fptr);

	FILE *ftr;

	ftr= fopen("Text.txt","w");
	fprintf(ftr,"%s","Brave");
	fclose(ftr);


	fptr= fopen("Text.txt","r");
	char ch[200];
	fscanf(fptr,"%s",ch);
	printf("\n%s",ch);

	fclose(fptr);


	fptr = fopen("Test.txt","r");
	int n=1;
	while(n<17) {
		printf(" %c",fgetc(fptr));
		n++;
	}
	fclose(fptr);


	printf("\n");
	fptr=fopen("Text.txt","a");
	fputc('K',fptr);
	fclose(fptr);


	fptr=fopen("Text.txt","r");
	int p=1;

	while(p!=10) {
		printf("%c",fgetc(fptr));
		p++;
	}
	fclose(fptr);

	fptr= fopen("Strings.txt","w");
	fprintf(fptr,"%s","\nHello");
	fprintf(fptr,"%s"," guys.");
	fprintf(fptr,"%s"," How");
	fprintf(fptr,"%s"," are");
	fprintf(fptr,"%s"," you?");

	fclose(fptr);
	fptr=fopen("Strings.txt","r");
	char L;
	while(L != EOF) {
		L =  fgetc(fptr);
		printf("%c",L);
	}
	fclose(fptr);

	fptr=fopen("Number.txt","w");
	fprintf(fptr,"%d",12942);
	fputc(' ',fptr);
	fprintf(fptr,"%d",263);
	fputc(' ',fptr);
	fprintf(fptr,"%d",3968);
	fputc(' ',fptr);
	fprintf(fptr,"%d",4425);
	fputc(' ',fptr);
	fprintf(fptr,"%d",6345);
	fputc(' ',fptr);
	fclose(fptr);

	fptr=fopen("Number.txt","r");

	int i=1;
	int Y;
	while(i<7) {
		fscanf(fptr,"%d",&Y);
		printf("%d ",Y);
		i++;
	}
	fclose(fptr);

     fptr=fopen("Newone.txt","w");
fprintf(fptr,"%s","Hello GuruPremaKosame Nuvuu naaku nachavule");
	 fclose(fptr);
    
      fptr=fopen("Newone.txt","r");
char line[100];
fgets(line,100,fptr);

printf("%s",line);
     fclose(fptr);
 	return 0 ;

}
