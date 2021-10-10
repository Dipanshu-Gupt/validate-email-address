# validate-email-address
email id verification

#include <stdio.h>

int test(char test[])
{
    int i;
    char *pos1,*pos2;
    char *ch;
    
    puts("enter email");
    scanf("%39s",test);
    while(1) 
    {
        for(i=0,ch=test; *ch; *ch++) {
            if(*ch=='@'){
                pos1=ch;
                i++;
            }
        }
        pos2=ch;
        if(i==1) {
            while(pos1-test && ch-pos1 > 1) {
                if((pos2-ch) > 2 && *ch== '.') {
                    printf("pos2-ch is %ld and *ch is %c",pos2-ch, *ch);
                    return 1;
                }   
                ch-- ;
            }
        }
    puts("Email wrong ! Enter again");
    scanf("%39s",test);
}
return 1;
}


