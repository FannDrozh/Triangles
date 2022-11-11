# Треугольники

Программа для определения вида треугольников таких как: равносторонний, равнобедренный или разносторонний.

## Начало работы

Для работы с проектом необходимо перейти по ссылке и скачать либо zip архив, либо клонировать репозиторий себе на компьютер. Если вы скачали zip архивом его необходимо распаковать в удобное для вас место и внутри папки проекта запустить sln файл.

### Необходимые условия

Для установки необходима Visual Studio.
<br>
Данную программу можно скачать с 
[Visual Studio downloading](https://visualstudio.microsoft.com/ru/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false) (Перейдя по ссылке сразу начнётся установка exe файла)

### Установка

1. Шаг<br>
Проверить, если на компьютере программное обеспечение в ввиде Visual Studio. Если её нет, то необходимо перейти предыдущему пункту и прочесть его. 
2. Шаг<br>
После необходимо перейти на проект [Triangles](https://github.com/FannDrozh/Triangles)
3. Шаг<br>
Перейдя на проект необходимо нажать на зелёную кнопку Code
![Проект на GitHub](https://sun9-north.userapi.com/sun9-80/s/v1/ig2/cftnQc9ln4PxwD6LM88i4yYvOj0nHdx4LUCNxN2aXT7oQu0YOsDSEMjfYVnzTAmOq2A-Q1gj_EnFbjbEo9-H4dPJ.jpg?size=931x300&quality=96&type=album)
4. Шаг<br>
Далее откроется меню, где возможно выбрать один из нескольких вариантов:
![](https://sun9-west.userapi.com/sun9-1/s/v1/ig2/C1eG-zlTyjSDgY24D4r60vKQZmCHIhaQYDnMctnAQLj_sgd5Kjmoiw2rNhClCmf3H8Y4WeFCCm8ltaJUg1wCeTsp.jpg?size=393x420&quality=96&type=album)
    * Нажав на Open with Visual Studio, то вам откроеться программа Visual Studio и начнётся процесс переноса проекта на ваш компьютер;
    * Нажав на Dowload ZIP вы скачаете zip архив, который вам надо будет разорхивировать на компьютере. А после открыть внутри sln файл.
5. Шаг<br>
Вам необходимо будет нажать на кнопку Triangles. После этого запуститься программа.
![](https://sun9-north.userapi.com/sun9-80/s/v1/ig2/YqV0R3rfGvS9zz5vzHovNsHI9oa62K9zglGlJzOobILmaaowrC4ZCD1A7UbupGZSO8Hzykoz9QPLQHreCMWOncc5.jpg?size=943x307&quality=96&type=album)
6. Шаг<br>
Программа запущена!
![Запущенная программа](https://sun9-west.userapi.com/sun9-62/s/v1/ig2/Fu6i-n91ZovN7iJLqetogH0LUcRAwvVzW9IAK6urcgAO8CwQbYgfGOntw4aPHKOacCPq6fkN8sZMkE6XlQr3WzjX.jpg?size=781x389&quality=96&type=album)

## Код

``` C#
public int VAB1, VBC1, VCA1;
        public MainWindow()
        {
            InitializeComponent();            
        }
        private void Button_Click(object sender, EventArgs e)
        {
            try
            {
                TextBlock textBlock = new TextBlock();
                textBlock.Text = Type.Text;
                VAB1 = Convert.ToInt32(VAB.Text);
                VBC1 = Convert.ToInt32(VBC.Text);
                VCA1 = Convert.ToInt32(VCA.Text);
            }
            catch (System.FormatException) 
            {
                MessageBox.Show("Проверьте введенные данные");
            }
            if (VAB1 == VBC1 && VBC1 == VCA1 && VCA1 == VAB1)
            {        
                if (VAB1 <= 0 || VBC1 <= 0 || VCA1 <= 0 || VAB1 + VBC1 <= VCA1 || VAB1 + VCA1 <= VBC1 || VBC1 + VCA1 <= VAB1)
                {
                    MessageBox.Show("Треугольника не существует");
                    MessageBox.Show("Введите положительное целочисленное значение не равное 0");
                }
                else
                {
                    Type.Text = "Равносторонний";
                }
            } 
            else if (VAB1 == VBC1 || VBC1 == VCA1 || VCA1 == VAB1)
            {
                if (VAB1 <= 0 || VBC1 <= 0 || VCA1 <= 0 || VAB1 + VBC1 <= VCA1 || VAB1 + VCA1 <= VBC1 || VBC1 + VCA1 <= VAB1)
                {
                    MessageBox.Show("Треугольника не существует");
                    MessageBox.Show("Введите положительное целочисленное значение не равное 0");
                }
                else
                {
                    Type.Text = "Равнобедренный";
                }
            }
            else if (VAB1 != VBC1 && VBC1 != VCA1 && VCA1 != VAB1)
            {
                if (VAB1 <= 0 || VBC1 <= 0 || VCA1 <= 0 || VAB1 + VBC1 <= VCA1 || VAB1 + VCA1 <= VBC1 || VBC1 + VCA1 <= VAB1)
                {
                    MessageBox.Show("Треугольника не существует");
                    MessageBox.Show("Введите положительное целочисленное значение не равное 0");
                }
                else
                {
                    Type.Text = "Разносторонний";
                }                               
            }
        }
```

## Авторы

* **Барашенков Илья** - *Основная работа* - [FannDrozh](https://github.com/FannDrozh)

See also the list of [Triangles](https://github.com/FannDrozh/Triangles) who participated in this project.
