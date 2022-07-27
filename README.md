# count-letter
# c programming
# Let's find the number of corresponding letters in a word in alphabetical order! 알파벳의 순서대로 단어에 해당 알파벳의 개수를 구해보자!
#include <stdio.h>
#include <string.h>
int main(void)
{
    int i, j, k;
    int count[27] = { 0, };
    char user[99];
    char ascii[100];
    printf("입력 문자열: ");
    scanf("%s", user);
    int lenth = strlen(user);
    for (i = 0; i < 100; i++) {
        ascii[i] = 'a' + i; //알파벳순으로 정리  
        if (ascii[i] == 'z')
            break;
    }
    for (i = 0; i <= 26; i++) {
        for (j = 0; j <= lenth; j++)
            if (ascii[i] == user[j]) 
                count[i]++;
    }
    for (k = 1; k < 27; k++) {
        if (count[k] != 0)
            printf("%c문자가 %d번 등장하였음!\n", ascii[k], count[k]);
        
    }
    return 0; 
}
#result--> junghyun g가 1번 등장하였음! h가 1번 등장하였음! j가 1번 등장하였음! n가 2번 등장하였음! u가 2번 등장하였음! y가 1번 등장하였음!
