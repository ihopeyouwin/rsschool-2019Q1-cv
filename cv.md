### **Curriculum Vitae**
1. Kalinaev Ivan
2. **Contacts** : +375447929396(mob.), ihopeyouwin_ship(skype), ihopeyouwon@gmail.com(e-mail)
3. **Summary**
Programming was always an appropriate thing for me, i liked it when i was at school, but at that moment i did not realize that i can bound my life with it. 
Now I cant deny my passion to it and I'm going to become a skilled specialist, i went to a retraining couple of mounths ago, also I'm studying technologies myself, 
in addition to this my superiour language skills serve me good, and no matter happens on that JS-course, I will become a skilled specialist that way, or another.
4. **Skills**: basic C++ knowledge, MS SQL basics, C#(basics, WFP, LINQ, ADO.NET + EntityFramework), Java(basics)
5. **Code examples**
```C#
    public partial class Page3 : Page
    {
        CollectionViewSource managersViewSource;
        public Page3()
        {
            InitializeComponent();
            managersViewSource = (CollectionViewSource)FindResource("managersViewSource");
            DataContext = this;
        }
        private void Window_Loaded(object sender, RoutedEventArgs e)
        {
            App.Context.managers.Load();
            managersViewSource.Source = App.Context.managers.Local;
        }
        private void Btn1_Click(object sender, RoutedEventArgs e)
        {
            ManagerAD add = new ManagerAD();
            bool? wasAdded = add.ShowDialog();
            if (wasAdded == true)
            {
                managersViewSource.View.Refresh();
            }
        }
        private void Btn2_Click(object sender, RoutedEventArgs e)
        {
            managers selectedM = managersDataGrid.SelectedItem as managers;
            MessageBoxResult confirmation = MessageBox.Show("Точно нужно удалить этого сотрудника", "Внимание!", MessageBoxButton.YesNo, MessageBoxImage.Question);
            if (confirmation == MessageBoxResult.Yes)
            {
                App.Context.managers.Remove(selectedM);
                managersViewSource.View.Refresh();
                App.Context.SaveChanges();
            }
        }
        private void managersDataGrid_MouseDoubleClick(object sender, RoutedEventArgs e)
        {
            managers selectedM = managersDataGrid.SelectedItem as managers;
            Editmanager change = new Editmanager(selectedM);
            bool? wasAdded = change.ShowDialog();
            if (wasAdded == true)
            {
                managersViewSource.View.Refresh();
                App.Context.SaveChanges();
            }
        }
    }

    public partial class Window1 : Window
    {
        CollectionViewSource win1viewsource;
        public Window1()
        {
            InitializeComponent();
            this.win1viewsource = (CollectionViewSource)FindResource("ordersViewSource");
            DataContext = this;
        }

        private void Window_Loaded(object sender, RoutedEventArgs e)
        {
            App.Context.Switchboard_Items.Load();
            this.win1viewsource.Source = App.Context.orders.Local;
            WpfApp1.tryhard1DataSet tryhard1DataSet = ((WpfApp1.tryhard1DataSet)(this.FindResource("tryhard1DataSet")));
            WpfApp1.tryhard1DataSetTableAdapters.clientsTableAdapter tryhard1DataSetclientsTableAdapter = new WpfApp1.tryhard1DataSetTableAdapters.clientsTableAdapter();
            tryhard1DataSetclientsTableAdapter.Fill(tryhard1DataSet.clients);
            System.Windows.Data.CollectionViewSource clientsViewSource = ((System.Windows.Data.CollectionViewSource)(this.FindResource("clientsViewSource")));
            WpfApp1.tryhard1DataSetTableAdapters.managersTableAdapter tryhard1DataSetmanagersTableAdapter = new WpfApp1.tryhard1DataSetTableAdapters.managersTableAdapter();
            tryhard1DataSetmanagersTableAdapter.Fill(tryhard1DataSet.managers);
            System.Windows.Data.CollectionViewSource managersViewSource = ((System.Windows.Data.CollectionViewSource)(this.FindResource("managersViewSource")));
            WpfApp1.tryhard1DataSetTableAdapters.trailersTableAdapter tryhard1DataSettrailersTableAdapter = new WpfApp1.tryhard1DataSetTableAdapters.trailersTableAdapter();
            tryhard1DataSettrailersTableAdapter.Fill(tryhard1DataSet.trailers);
            System.Windows.Data.CollectionViewSource trailersViewSource = ((System.Windows.Data.CollectionViewSource)(this.FindResource("trailersViewSource")));
        }
        private void B1_Click(object sender, RoutedEventArgs e)
        {
            orders neword = new orders();
            neword.заказ = заказTextBox.Text;
            neword.статус = статусTextBox.Text;
            neword.погрузка = погрузкаDatePicker.SelectedDate;
            neword.ведущ_код = Convert.ToString(ведущ_кодComboBox.SelectedItem as managers);
            neword.менеджер = Convert.ToString(менедж_кодComboBox.SelectedItem as managers);
            neword.машина = Convert.ToString(тягач_номComboBox.SelectedItem as trailers); 
            neword.выгрузка = выгрузкаTextBox.Text;
            neword.маршрут = маршрутTextBox.Text;
            neword.договор = договорTextBox.Text;
            neword.клиент = Convert.ToString(_клиент_кор_ComboBox.SelectedItem as clients);
            neword.тип_перевозки = тип_перевозкиTextBox.Text;
            neword.простой = простойTextBox.Text;
            neword.фрахт = float.Parse(фрахтTextBox.Text);
            App.Context.orders.Add(neword);
            App.Context.SaveChanges();
            this.DialogResult = true;
            this.Close();
        }
        private void B2_Click(object sender, RoutedEventArgs e)
        {
            this.DialogResult = false;
            this.Close();
        }
    }
}
```
6. **Experience:** Making a text game in C#, building a calculator, completing tasks within the courses, making an application for the SQL base(C#) to show its contents;
7. **Education:** Belarusian State Economic University, Economist, Accounting in Transport. Information Systems Software(c++/C# courses), Javarush free, Codecademy "introduction to HTML" & "Learn CSS" courses
8. **English level:** B2(gymnasium #38 with English specialization, english camps(3 times), international sales practice(4 years), winner of the English BaKonkurs competition 2008 (for students of 11th grade in Belarus)