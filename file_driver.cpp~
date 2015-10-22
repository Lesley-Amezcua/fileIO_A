//Name:Lesley Amezcua
//Date:October 20, 2015
//Description: Programming Practice- File IO A

#include <iostream>
#include <fstream>
#include <cstdlib>
#include <string>
#include <cctype>

using namespace std;

int main ()
{   
    ifstream fin, finC;
    ofstream fout, foutUpper_case, foutCapital_file;
   
    fin.open("gba.txt");
    finC.open("gba.txt");
    fout.open("results.txt");
    foutUpper_case.open("uppercase.txt");
    foutCapital_file.open("capitalize.txt");
    
    string valA, word_No_Punctuation, word_Capitalized, all_Upper_case, makeUpper_case, upper_caseWord;
    
    double counter = 0, average_Characters;
    
    int sum = 0, number_Letters, minus_From_Word_Count = 0, total_NumWords, one_Letter_Words = 0, two_Letter_Words = 0, three_Letter_Words = 0, four_Letter_Words = 0, five_Letter_Words = 0, six_Letter_Words = 0, seven_Letter_Words = 0, eight_Letter_Words = 0, nine_Letter_Words = 0, ten_Letter_Words = 0, eleven_OrMore_Letter_Words = 0, twelve_Letter_Words =0; 
    char individual_Letter, upper_case_First, individual_MakeUpper_case;
   
    if(fin.fail())
    {
        cout << "Error opening input file!" << endl;
        exit(1);
    }
    
    if(finC.fail())
    {
        cout << "Error opening input file!" << endl;
        exit(1);
    }
    
    if(fout.fail())
    {
        cout << "Error opening output file!" << endl;
        exit(1);
    }
    
    if(foutUpper_case.fail())
    {
        cout << "Error opening output file!" << endl;
        exit(1);
    }
    
    if(foutCapital_file.fail())
    {
        cout << "Error opening output file!" << endl;
        exit(1);
    }
    
    while(finC >> makeUpper_case)
    {
        for(int ix = 0; ix < makeUpper_case.length(); ix++)
        {
                individual_MakeUpper_case = toupper(makeUpper_case[ix]);
                upper_caseWord = upper_caseWord + individual_MakeUpper_case;
        }
       foutCapital_file << upper_caseWord << " ";
       upper_caseWord = "";
    }//end of while
    
    while(fin >> valA)
    {
        upper_case_First = toupper(valA[0]); 
        word_Capitalized = upper_case_First + valA.substr(1, valA.length() - 1) + " ";
        foutUpper_case << word_Capitalized;
       
        for(int ix = 0; ix < valA.length(); ix++)
        {
            if(valA[valA.length()-1] == ',' || valA[valA.length()-1] == '.')
            {
              number_Letters = valA.length()-1;  
            } 
            else if(valA == "--")
            {
                number_Letters = 0;
            }
            else
            {
                number_Letters = valA.length();
            } 
        }//end of for loop
        
        sum = sum + number_Letters;
       
        if(number_Letters == 1)
        {
            one_Letter_Words++;
        }
        if(number_Letters == 2 && valA != "--")
        {
            two_Letter_Words++;
        }
        if(valA == "--")
        {
            minus_From_Word_Count++;
        }
        if(number_Letters == 3)
        {
            three_Letter_Words++;
        }
        if(number_Letters == 4)
        {
            four_Letter_Words++;
        }
        if(number_Letters == 5)
        {
            five_Letter_Words++;
        }
        if(number_Letters == 6)
        {
            six_Letter_Words++;
        }
        if(number_Letters == 7)
        {
            seven_Letter_Words++;
        }
        if(number_Letters == 8)
        {
            eight_Letter_Words++;
        }
        if(number_Letters == 9)
        {
            nine_Letter_Words++;
        }
        if(number_Letters == 10)
        {
            ten_Letter_Words++;
        }
        
        if(number_Letters >= 11)
        {
            eleven_OrMore_Letter_Words++;
        }    
        counter++;
    }//end of while loop
    
    total_NumWords = counter - minus_From_Word_Count;
    average_Characters = sum/total_NumWords;
    
    fout << "The average characters per word is " << average_Characters << endl;
    fout << one_Letter_Words << " words of length 1" << endl;
    fout << two_Letter_Words << " words of length 2" << endl;
    fout << three_Letter_Words << " words of length 3" << endl;
    fout << four_Letter_Words << " words of length 4" << endl;
    fout << five_Letter_Words << " words of length 5" << endl;
    fout << six_Letter_Words << " words of length 6" << endl;
    fout << seven_Letter_Words << " words of length 7" << endl;
    fout << eight_Letter_Words << " words of length 8" << endl;
    fout << nine_Letter_Words << " words of length 9" << endl;
    fout << ten_Letter_Words << " words of length 10" << endl;
    fout << eleven_OrMore_Letter_Words << " words of length 11 or longer" << endl;
    fout << "The number of words in the file is " << total_NumWords << endl;
    
    fin.close();
    finC.close();    
    fout.close();
    foutCapital_file.close();
    foutUpper_case.close();
    
    return 0;
}
