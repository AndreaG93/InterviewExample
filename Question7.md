# Domanda 7

Sia dato il seguente snippet di codice:

    public async Task DoAsync()
    {
        Console.WriteLine("Before await");

        await Task.Delay(TimeSpan.FromSeconds(1));

        Console.WriteLine("Between awaits");

        await Task.Delay(TimeSpan.FromSeconds(1));

        Console.WriteLine("After await");
    }

>## Cosa fa?