# LinqWithSkumar
Linq




Console.WriteLine(numbers.First());

Console.WriteLine(numbers.FirstOrDefault());

Console.WriteLine(numbers.SingleOrDefault(c=> c==1));

Console.WriteLine(numbers.Single());


Console.WriteLine(Enumerable.Empty<int>());

Console.WriteLine(Enumerable.Repeat("hello",3));

Console.WriteLine(Enumerable.Range(1,10));

Console.WriteLine(Enumerable.Range('a','z'-'a').Select(a=> (char)a));



  # Projection + Operations
  
` var numbers = Enumerable.Range(1,4);
var squares = numbers.Select(x => x*x);
Console.WriteLine(squares);`

`string sentence = "This is a nice sentence";
var wordLengths = sentence.Split().Select(w => w.Length);
Console.WriteLine(wordLengths);`

`// keep both word and length
var wordsWithLength = sentence.Split().Select(w => new { Word = w, Size = w.Length});
Console.WriteLine(wordsWithLength);`

`// get all the words
var sequences = new[]{ "red,green,blue", "orange", "white,pink" };
var allWords = sequences.SelectMany(s => s.Split(',')); // select
Console.WriteLine(allWords);`

`// select each pair (cross product) from two collections
string [] objects = { "house", "car", "bicycle" };
string [] colors = { "red", "green", "gray" };
var pairs = colors.SelectMany(z => objects, (c, o) => $"{c} {o}");
Console.WriteLine(pairs);`
  
