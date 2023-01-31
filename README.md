string[] source = new string[] { "dog", "cat", "mouse" };
 for (int i = 0; i < Math.Pow(2, source.Length); i++)
 {
     string[] combination = new string[source.Length];
     for (int j = 0; j < source.Length; j++)
     {
         if ((i & (1 << (source.Length - j - 1))) != 0)
         {
             combination[j] = source[j];
         }
    }
    Console.WriteLine("[{0}, {1}, {2}]", combination[0], combination[1], combination[2]);
}
