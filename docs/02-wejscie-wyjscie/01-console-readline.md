# Wczytywanie tekstu z konsoli - Console.ReadLine()

## Cel lekcji

Nauczysz się wczytywać tekst wpisany przez użytkownika w konsoli za pomocą `Console.ReadLine()`.

Po tej lekcji powinieneś umieć:

- odróżnić wejście programu od wyjścia programu,
- wypisać komunikat dla użytkownika,
- wczytać tekst z konsoli,
- zapisać wczytany tekst do zmiennej typu `string`,
- wypisać wczytaną wartość.

## 1. Czym jest wejście programu

Wejście programu to dane, które program otrzymuje z zewnątrz.

W programie konsolowym wejściem może być tekst wpisany przez użytkownika z klawiatury.

Przykład: użytkownik wpisuje swoje imię, nazwę miasta albo nazwę szkoły.

## 2. Czym jest wyjście programu

Wyjście programu to dane, które program pokazuje użytkownikowi.

W programie konsolowym wyjściem jest najczęściej tekst wypisany w konsoli.

Do wypisywania danych używamy `Console.WriteLine()`.

## 3. Przypomnienie Console.WriteLine()

`Console.WriteLine()` wypisuje dane w konsoli i przechodzi do nowej linii.

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("To jest komunikat dla użytkownika.");
    }
}
```

W tej lekcji `Console.WriteLine()` będzie często używane do pokazania użytkownikowi, co ma wpisać.

## 4. Wczytywanie danych za pomocą Console.ReadLine()

`Console.ReadLine()` wczytuje tekst wpisany przez użytkownika.

Program czeka, aż użytkownik:

- wpisze tekst,
- naciśnie Enter.

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Podaj swoje imię:");
        string imie = Console.ReadLine();

        Console.WriteLine("Witaj, " + imie + "!");
    }
}
```

W tym przykładzie:

- program najpierw wypisuje komunikat,
- użytkownik wpisuje imię,
- `Console.ReadLine()` wczytuje wpisany tekst,
- tekst zostaje zapisany w zmiennej `imie`,
- program wypisuje powitanie.

## 5. Console.ReadLine() zwraca string

`Console.ReadLine()` zawsze zwraca tekst typu `string`.

Nawet jeśli użytkownik wpisze:

```csharp
123
```

program na tym etapie traktuje to jako tekst `"123"`, a nie jako liczbę.

Do obliczeń liczbowych potrzebna będzie konwersja. Konwersję omówimy w kolejnej lekcji.

## 6. Zapisanie wczytanego tekstu do zmiennej

Wczytany tekst najczęściej zapisujemy do zmiennej typu `string`.

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Podaj nazwę szkoły:");
        string szkola = Console.ReadLine();

        Console.WriteLine("Twoja szkoła to: " + szkola);
    }
}
```

Zmienna `szkola` przechowuje tekst wpisany przez użytkownika.

## 7. Wypisanie wczytanej wartości

Po wczytaniu tekstu można go wypisać w konsoli.

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Podaj ulubiony język programowania:");
        string jezyk = Console.ReadLine();

        Console.WriteLine("Wybrany język: " + jezyk);
    }
}
```

Wartość zmiennej `jezyk` pochodzi od użytkownika.

## 8. Prosty dialog z użytkownikiem

Program może prowadzić prosty dialog z użytkownikiem.

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Podaj swoje imię:");
        string imie = Console.ReadLine();

        Console.WriteLine("Podaj nazwę miasta:");
        string miasto = Console.ReadLine();

        Console.WriteLine("Imię: " + imie);
        Console.WriteLine("Miasto: " + miasto);
    }
}
```

To nadal są dane tekstowe. Program nie wykonuje na nich obliczeń.

## 9. Komunikat dla użytkownika a wczytanie odpowiedzi

Komunikat dla użytkownika i wczytanie odpowiedzi to dwie różne instrukcje.

Mniej czytelny przykład:

```csharp
using System;

class Program
{
    static void Main()
    {
        string imie = Console.ReadLine();

        Console.WriteLine("Witaj, " + imie + "!");
    }
}
```

Ten program zadziała, ale użytkownik może nie wiedzieć, co ma wpisać.

Lepszy przykład:

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Podaj swoje imię:");
        string imie = Console.ReadLine();

        Console.WriteLine("Witaj, " + imie + "!");
    }
}
```

Jeżeli przed `Console.ReadLine()` nie wypiszemy komunikatu, użytkownik może nie wiedzieć, co ma wpisać.

## 10. Console.WriteLine() i Console.ReadLine()

Najważniejsza różnica:

- `Console.WriteLine()` wypisuje dane,
- `Console.ReadLine()` wczytuje tekst.

Przykład:

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Podaj ulubiony przedmiot:");
        string przedmiot = Console.ReadLine();

        Console.WriteLine("Ulubiony przedmiot: " + przedmiot);
    }
}
```

Pierwsze `Console.WriteLine()` pokazuje pytanie. `Console.ReadLine()` czeka na odpowiedź. Drugie `Console.WriteLine()` wypisuje wynik.

## Typowe błędy

- Brak komunikatu przed `Console.ReadLine()`.
- Mylenie `Console.WriteLine()` z `Console.ReadLine()`.
- Oczekiwanie, że `Console.ReadLine()` od razu zwraca liczbę.
- Próba wykonywania obliczeń na tekście bez konwersji.
- Zapomnienie o zapisaniu wyniku `Console.ReadLine()` do zmiennej.

## Zapamiętaj

- Wejście programu to dane podane przez użytkownika.
- Wyjście programu to dane pokazane użytkownikowi.
- `Console.WriteLine()` wypisuje dane.
- `Console.ReadLine()` wczytuje tekst.
- `Console.ReadLine()` czeka na wpisanie tekstu i naciśnięcie Enter.
- Wynik `Console.ReadLine()` ma typ `string`.
- Nawet wpisane `123` jest na tym etapie tekstem.
- Do obliczeń liczbowych potrzebna będzie konwersja, którą omówimy w następnej lekcji.
- Przed wczytaniem danych warto wypisać komunikat dla użytkownika.

## Ćwiczenia

1. Wczytaj imię użytkownika i wypisz powitanie.
2. Wczytaj nazwę miasta i wypisz ją w zdaniu.
3. Wczytaj nazwę szkoły i wypisz komunikat.
4. Wczytaj ulubiony przedmiot użytkownika.
5. Wczytaj dwie informacje tekstowe i wypisz je w dwóch liniach.
6. Sprawdź, co się stanie, gdy wpiszesz liczbę zamiast tekstu.
7. Dodaj komunikat przed każdym `Console.ReadLine()`.
8. Popraw program, w którym użytkownik nie wie, co ma wpisać.
