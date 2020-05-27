#include <stdio.h>
#include <cs50.h>
#include <string.h>
#include <math.h>
#include <ctype.h>

int main(void)
{

    string text = get_string("Text: "); //prompt the user for a string of text
    int letters = 0;
    int spaces = 0;
    int i = 0;
    int words = 0;
    int sentences = 0;
    int txtlen;
    txtlen = strlen(text); //number of characters in text

    for (i = 0; i < txtlen; i++) //run through each character in a for loop
    {
        if (text[i] == ' ') //count number of spaces
        {
            spaces++;
        }
        if (text[i] == '.') //count number of sentences
        {
            sentences++;
        }
        if (text[i] == '!') //count number of sentences
        {
            sentences++;
        }
        if (text[i] == '?') //count number of sentences
        {
            sentences++;
        }
        if (isalpha(text[i]) != 0) //count number of alphabets
        {
            letters++;
        }
    }
    words = spaces + 1; //count number of words
    float L = (float) letters / (float) words * 100; //average number of letters per 100 words in the text
    float S = (float) sentences / (float) words * 100; //average number of sentences per 100 words in the text
    float grade = 0.0588 * L - 0.296 * S - 15.8; //Coleman-Liau index
    if (grade > 16)
    {
        printf("Grade 16+\n");
    }
    else if (grade < 1)
    {
        printf("Before Grade 1\n");
    }
    else
    {
        printf("Grade %.0f\n", round(grade));
    }
}
