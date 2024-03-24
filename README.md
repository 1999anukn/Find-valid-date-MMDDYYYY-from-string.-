# Find-valid-date-MMDDYYYY-from-string.-
using System;
using System.Text.RegularExpressions;

class Program
{
    static void Main(string[] args)
    {
        string input = "Hdjsh asd2324234jghjsd hjsdg sdhk  12212021 idf32432 32423 d34234jh dfh"; // enter the required string here to check the date in the MMDDYYYY format 

        // Define the regular expression pattern for MMDDYYYY format
        string pattern = @"\b(0[1-9]|1[0-2])(0[1-9]|[12][0-9]|3[01])(19|20)\d{2}\b";

        // Find matches
        MatchCollection matches = Regex.Matches(input, pattern);

        // Print matches
        if (matches.Count > 0)
        {
            Console.WriteLine("Valid dates found:");
            foreach (Match match in matches)
            {
                Console.WriteLine(match.Value);
            }
        }
        else
        {
            Console.WriteLine("No valid dates found.");
        }
    }
}


