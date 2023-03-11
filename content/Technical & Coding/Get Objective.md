Get a game objective form a text file

`using System;
using System.IO;
using System.Linq;

class Program
{
    static void Main(string[] args)
    {
        string filePath = @"objectives.txt";

        // Read all lines from the file into an array
        string[] lines = File.ReadAllLines(filePath);

        // Generate a random number between 0 and the number of lines in the file
        Random random = new Random();
        int randomLineNumber = random.Next(0, lines.Length);

        // Get the random line from the array
        string randomLine = lines[randomLineNumber];

        Console.WriteLine("Objective:");
        Console.WriteLine(randomLine);
    }
}`