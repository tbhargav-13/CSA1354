// Simulate a DFA for the language representing strings over 𝚺={a,b} that start with a and end with a

#include<stdio.h>
#include<string.h>

int main(){

    char input[100];

    while(1){
        printf("Enter an Input String over E = {a,b} : ");
        scanf("%s", &input );

        int l = strlen(input);
        int invalid = 0;

        for(int i = 0;i<l;i++){
            if(input[i] == 'a' || input[i] == 'b')
                continue;
            else{
                invalid = 1;
                printf("String Invalid. Enter a String over E = {a,b} .\n\n");
                break;
            }
        }

        if(input[0] == 'a' && input[l-1] == 'a' && invalid == 0)
            printf("String Accepted. HURRAYYY !\n\n");
        else if(input[0] != 'a' || input[l-1] != 'a' && invalid == 0)
            printf("String Rejected. YIKES ! \n\n");
    
    }


    return 0;
}