# C-language
C language vowels consonants
#include<stdio.h>
void main()
{
    char strn[200];
    int i,vowels=0,consonants=0,words=0,specialCharacters=0;
    
    printf("Enter a string\n");
    gets(strn);
    printf("Characters= %ld", strlen(strn));
    for(i=0;strn[i]!='\0';i++)
    {
        if(strn[i]=='a' || strn[i]=='e' || strn[i]=='i' ||strn[i]=='o' || strn[i]=='u' || strn[i]=='A' ||strn[i]=='E' || strn[i]=='I' || strn[i]=='O' ||strn[i]=='U')
        {
            ++vowels;
        }
        else if((strn[i]>='a'&& strn[i]<='z') || (strn[i]>='A'&& strn[i]<='Z'))
        {
            ++consonants;
        }
        
        else if (strn[i]==' ')
        {
            ++words;
        }
        else if (strn[i]==',' || strn[i]=='&' || strn[i]=='@' || strn[i]=='.')
        {
            ++specialCharacters;
        }
        else
        {
            printf("ERROR");
        }
    }
 
    printf("\nVowels = %d",vowels);
    printf("\nConsonants = %d",consonants);
    printf("\nWhite spaces = %d",words);
    printf("\nSpecial characters = %d",specialCharacters);
    
}
