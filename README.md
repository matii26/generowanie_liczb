# generowanie_liczb

using System;
using System.Windows;

public partial class MainWindow : Window
{
    public MainWindow()
    {
        InitializeComponent();
        GenerateRandomNumbers();
    }

    private void GenerateRandomNumbers()
    {
        Random random = new Random();
        NumbersTextBlock.Text = string.Empty;
        for (int i = 0; i < 100; i++)
        {
            NumbersTextBlock.Text += random.Next(100) + "\n";
        }
    }
}


....


using System;
using System.Text;
using System.Windows;

public partial class MainWindow : Window
{
    public MainWindow()
    {
        InitializeComponent();
    }

    private void GenerateNumbersButton_Click(object sender, RoutedEventArgs e)
    {
        Random random = new Random();
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < 100; i++)
        {
            // Generowanie losowej liczby między 0 a 99
            int randomNumber = random.Next(100);
            sb.AppendLine(randomNumber.ToString());
        }
        // Wyświetlanie wygenerowanych liczb
        NumbersTextBlock.Text = sb.ToString();
    }
}
