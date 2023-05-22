# 2
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Посочете кое твърдение е вярно за променливите?
Променливата е място, на което пазим информация., 
Всяка една променлива в C# си има тип и име., 
Не може да има две променливи с едно и също име.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Опишете как се инициализира многомерен масив в C#?
Инициализация на многомерни масиви:

Инициализацията на многомерни масиви е аналогична на инициализацията на едномерните. Стойностите на елементите могат да се изброяват непосредствено след декларацията:
            
       int[,] matrix =
      {
         {1, 2, 3, 4}, // row 0 values
         {5, 6, 7, 8}, // row 1 values
      };
+++++++++++++++++++++++++++=
Двумерен масив с цели числа с 2 реда и 4 колони. Във външните фигурни скоби се поставят елементите от първата размерност, т.е. редовете на двумерната матрица. Всеки ред представлява едномерен масив.
..................................................................................................................................................
![image](https://github.com/arndv/2/assets/125039034/3e5bc4bc-c1e5-44af-bff7-113391d552a3)
..................................................................................................................................................
В най-популярната система за контрол на версиите GitHub има няколко основни команди, които се използват когато пишете в конзолния клиент GitBash. Обяснете какво прави командата git add, като поставите липсващите думи в празните полета.
С командата add [добавяте] промените в индекса на Git, които смятате, че са готови да [публикувате] (commit). 
..................................................................................................................................................
![image](https://github.com/arndv/2/assets/125039034/b3be02c7-83dc-425f-8c9f-8dcd8891dbb4)
..................................................................................................................................................
Дефинирайте понятието речник, като попълните липсващите думи в текста.

Речниците са известни още като [асоциативни масиви или карти]. В тях всеки [елемент ] представлява съответствие между [ключ и стойност].  На един [ключ] може да се съпостави точно една [стойност].

..................................................................................................................................................
![image](https://github.com/arndv/2/assets/125039034/2cc26c9b-15cc-46ba-b888-cf364e4b6dc3)
..................................................................................................................................................
//Баскетболен сезон

    static void Main(string[] args)
        {
            SortedDictionary<string, int> dict = new SortedDictionary<string, int>();

            string[] input = Console.ReadLine().Split(" - ", StringSplitOptions.RemoveEmptyEntries); 
            while (!input[0].Equals("END"))
            {
                if (!dict.ContainsKey(input[0]))
                { 
                    dict.Add(input[0], 0); 
                }
                dict[input[0]] += int.Parse(input[1]); 
                input = Console.ReadLine().Split(" - ", StringSplitOptions.RemoveEmptyEntries); 
            }

            foreach (var kvp in dict) 
            {
                Console.WriteLine($"{kvp.Key} -> {kvp.Value}"); 
            }
        }
..................................................................................................................................................
Дефинирайте понятието шестнадесетична бройна система. Къде най-често се използва? Как се представят шестнайсетичните числа в шестнадесетичната бройна система?

При шестнайсетичните числа (hexadecimal numbers) имаме за основа на бройната система числото 16, което налага да бъдат използвани 16 знака (цифри) за представянето на всички възможни стойности от 0 до 15 включително. 
Шестнадесетичната бройна система се използва често при компютрите, тъй като тя може да представи двоичните числа в по-удобен вид.
За представянето на шестнайсе­тичните числа се използват числата от 0 до 9 и латинските букви от A до F. Всяка от тях има съответната стойност:

A=10, B=11, C=12, D=13, E=14, F=15

Като примери за шестнайсетични числа могат да бъдат посочени съответно, D2, 1F2F1, D1E и др.
..................................................................................................................................................

//Видове числа

        static void Main(string[] args)
        {
            int[] nums = Console.ReadLine().Split(',').Select(int.Parse).ToArray(); 

            List<int> evens = new List<int>(); 
            List<int> odds = new List<int>();  
            List<int> sum5 = new List<int>();  

            for (int i = 0; i < nums.Length; i++) 
            {
                if (nums[i] % 2 == 0) 
                {
                    evens.Add(nums[i]);
                }
                else
                {
                    odds.Add(nums[i]);
                }
                if (SumDigits(nums[i]) % 10 == 5)
                {
                    sum5.Add(nums[i]); 
                }
            }
            Console.WriteLine(String.Join(", ", evens));
            Console.WriteLine(String.Join(", ", odds));
            Console.WriteLine(String.Join(", ", sum5));
        }
        public static int SumDigits(int number)
        {
            int sum = 0;

            while (number != 0) 
            {
                sum += number % 10;
                number /= 10;
            }

            return sum;
        }
 ..................................................................................................................................................       
 Посочете кое от изброените НЕ е вярно за стойностните типове данни?
 Стойностните типове данни съдържат в стека за изпълyнение на програмата референция (адрес) към динамичната памет (heap).
.................................................................................................................................................. 
 Посочете как се декларира многомерен масив в C#.
 Декларация на двумерен масив: int[,] twoDimentionalArray;

Декларация на тримерен масив: int[,,] threeDimentionalArray;
..................................................................................................................................................
Памет за многомерни размери се заделя като се използва ключовата дума new и за всяка размерност в квадратни скоби се задава размерът, който е необходим: 

int[,] intMatrix = new int[3, 4];

float[,] floatMatrix = new float[8, 2];

string[,,] stringCube = new string[5, 5, 5];

 intMatrix е двумерен масив с 3 елемента от тип int[] и всеки от тези 3 елемента има размерност 4. Разглеждат се като двумерни матрици, които имат редове и колони за размерности. Редовете и колоните на квадратните матрици се номерират с индекси от 0 до n-1. Ако един двумерен масив има размер m на n, той има точно m*n елемента.
..................................................................................................................................................
Имате дадена следната матрица:
![image](https://github.com/arndv/2/assets/125039034/c738d726-6f93-42a2-ac39-99ee2c01e3b9)
Имате и следният код на C#:
![image](https://github.com/arndv/2/assets/125039034/95a81779-ad9b-4af9-b146-30e917582584)
Какво ще се отпечата на конзолата? Решете задачата и запишете отговора в празното поле!

4 1 7 1 2
5 7
7
5 2 1 8

..................................................................................................................................................
Посочете кои от характеристиките се отнасят към централизираните сорс-контрол системи и кои към децентрализираните сорс-контрол системи.

Използват един сървър, съдържащ всички контролирани файлове и множество от клиенти, които издърпват файловете от това централно място. [Централизирани]

Клиентите изтеглят последния snapshot на файловете и изцяло клонират цялото хранилище, включително пълната му история. [Децентрализирани]

Администраторите имат подробен контрол върху това кой какво може да прави и освен това е много по-лесно да се администрира. [Централизирани]

Ако сървърът загине, хранилището на даден проект може да се възстанови от локалното копие на всеки клиент. [Децентрализирани]

Всички данни се пазят на едно място и зависят от надеждността на сървъра, който ги съхранява. [Централизирани]

Ако сървърът по някаква причина не е достъпен за час - тогава през този час никой не може да качва своите промени. [Централизирани]

..................................................................................................................................................
В най-популярната система за контрол на версиите GitHub има няколко основни команди, които се използват когато пишете в конзолния клиент GitBash. Обяснете какво прави командата git pull, като поставите липсващите думи в празните полета.
С командата pull автоматично [изтегляте] промените от отдалеченото хранилище.
..................................................................................................................................................
//Магически числа

       static void Main(string[] args)
        {
            int[] nums = Console.ReadLine().Split(',').Select(int.Parse).ToArray(); 
            List<int> evens = new List<int>();
            List<int> odds = new List<int>(); 
            List<int> sum5 = new List<int>(); 

            for (int i = 0; i < nums.Length; i++)
            {
                if (nums[i] % 2 == 0 && (nums[i] % 10 == 4 || nums[i] % 10 == 8)) 
                {
                    evens.Add(nums[i]);
                }
                else if (nums[i] % 2 != 0 && (nums[i] % 10 == 5 || nums[i] % 10 == 7)) 
                {
                    odds.Add(nums[i]);
                }
                if (SumDigits(nums[i]) == 15)
                {
                    sum5.Add(nums[i]); 
                }
            }

            Console.WriteLine(String.Join(", ", evens));
            Console.WriteLine(String.Join(", ", odds)); 
            Console.WriteLine(String.Join(", ", sum5));
        }
        public static int SumDigits(int number)
        {
            int sum = 0;

            while (number != 0)
            {
                sum += number % 10;
                number /= 10;
            }

            return sum; 
        }
 ..................................................................................................................................................       
Дефинирайте понятието двоична бройна система. Какво представлява? Къде се използва най-често? Как са представени числата в двоичната бройна система?

Двоичната бройна система (binary numeral system), е системата, която се използва за представяне и обработка на числата в съвременните електронноизчислителни машини. 
Числата представени в двоична бройна система, се задават във вторичен вид, т.е. вид удобен за възприемане от изчислителната машина. Този вид е малко по-трудно разбираем за човека. За представянето на двоичните числа, се използва двоичната бройна система, която има за основа числото 2. Числата записани в нея са подредени по степените на двойката. За тяхното представяне, се използват само цифрите 0 и 1.
Например със записа 1110(2) означаваме число в двоична бройна система. Ако не бъде указана изрично, бройната система се приема, че е десетична. 
..................................................................................................................................................

Дефинирайте понятието string в C# като попълните липсващите думи в текста.

Символният низ е [последователност от символи], записана на даден адрес в паметта. 
Символният низ е [неизменим (immutable)]. След като се  инициализира, съдържанието на променливата [не се] променя директно – ако опитаме да променим стойността, тя ще бъде записана на [ново ] място в [динамичната ] памет, а променливата ще започне да сочи към него.
..................................................................................................................................................
![image](https://github.com/arndv/2/assets/125039034/8f8640e4-c0d1-4f26-96e3-22e8fa3b1bd7)
..................................................................................................................................................
//Великденски яйца

         static void Main(string[] args)
        {
            Dictionary<string, int> dict = new Dictionary<string, int>();
            int eggs = int.Parse(Console.ReadLine()); 
            for (int i = 0; i < eggs; i++) 
            {
                string color = Console.ReadLine(); 
                if (!dict.ContainsKey(color)) 
                {
                    dict.Add(color, 0); 
                }
                dict[color]++;
            }

            Console.WriteLine($"Red eggs: {(dict.ContainsKey("red") ? dict["red"] : 0)}"); 
            Console.WriteLine($"Orange eggs: {(dict.ContainsKey("orange") ? dict["orange"] : 0)}"); 
            Console.WriteLine($"Blue eggs: {(dict.ContainsKey("blue") ? dict["blue"] : 0)}");
            Console.WriteLine($"Green eggs: {(dict.ContainsKey("green") ? dict["green"] : 0)}");
            Console.WriteLine($"Max eggs: {dict.Values.Max()} -> {dict.OrderByDescending(x => x.Value).FirstOrDefault().Key}");
        }
..................................................................................................................................................        
Какво се случва, когато създаваме масив в C#? Посочете верните отговори. 
В динамичната памет (heap) се заделя участък равен на броя на елементите в масива, които се инициализират със стойността по подразбиране на избрания тип данни., В стека за изпълнение на програмата се заделя променлива с име Името_на_масива.
 
..................................................................................................................................................
Обяснете какво прави метода ContainsKey(key) реализиран в класа Dictionary<K,V>?
Проверява дали в речника присъства наредена двойка с посочения ключ. Операцията работи изключително бързо.
..................................................................................................................................................
Опишете как ще преминете от десетична бройна система в двоична бройна система.
Преобразувайте числото  132(10)  от десетична бройна система в двоична бройна система.

При преминаване от десетична в двоична бройна система, се извършва преобразуване на десетичното число в двоично. За целите на преобразу­ването се извършва делене на две с остатък. Така се получават частно и остатък, който се отделя.
Числото 132 се дели целочислено на основата, към която ще преобразуваме (в примера тя е 2). След това, от остатъците получени при деленето (те са само нули и единици), се записва преобразуваното число. Деленето продължава, докато получим частно нула.
 
132:2=66 остатък 0;

66:2=33   остатък 0;

33:2=16   остатък 1;

16:2=8     остатък 0;

8:2=4       остатък 0;

4:2=2       остатък 0;

2:2=1       остатък 0;

1:2=0       остатък 1;

След като вече семе извършили деленето, записваме стойностите на остатъците в ред, обратен на тяхното получаване, както следва:
10000100
132(10) = 10000100(2)
..................................................................................................................................................
Дайте пример за това как бихте декларирали променлива от тип низ със стойност "Hello, World!"?

string message = "Hello, World!"
..................................................................................................................................................
Обяснете какво прави метода ContainsValue(V) реализиран в класа Dictionary<K,V>?
Проверява дали в речникa присъстват една или повече наредени двойки с посочената стойност. Тази операция работи бавно, тъй като проверява всеки елемент на хеш-таблицата.
..................................................................................................................................................
Посочете правилната стойност по подразбиране към всеки от типовете данни:
Правилният отговор е: char → '\u0000', bool → false, sbyte → 0, object → null, float → 0.0f, decimal → 0.0m, string → null

..................................................................................................................................................
В най-популярната система за контрол на версиите GitHub има няколко основни команди, които се използват когато пишете в конзолния клиент GitBash. Обяснете какво прави командата git commit, като поставите липсващите думи в празните полета.
След като промените са готови (staged), с командата commit [публикувате] промените.
..................................................................................................................................................
Демонстрирайте с C# код по какъв начин ще декларирате и ще заделите място в паметта на списък, който съдържа текстов тип данни?
List<string> list = new List<string> ..................................................................................................................................................           
Дефинирайте понятието string в C# като попълните липсващите думи в текста.
            
Символният низ е [последователност от символи], записана на даден адрес в паметта. 
Типът string е [клас ] и като такъв той спазва [принципите на обектно‑ориентираното програмиране]. Стойностите му се записват в [динамичната ] памет, а променливите от тип string пазят [референция към обект] в паметта.
..................................................................................................................................................            
Какво се случва, когато създаваме масив в C#? Посочете верните отговори.
В C# масив се създава с ключовата дума new, която служи за заделяне на памет., След заделянето на масива променливата Името_на_масива сочи към адрес в динамичната памет, където се намира нейната стойност. , Елементите на масивите винаги се съхраняват в динамичната памет.
            
..................................................................................................................................................
//Видове числа
            
            static void Main(string[] args)
            {
            int[] nums = Console.ReadLine().Split(',').Select(int.Parse).ToArray(); 

            List<int> evens = new List<int>(); 
            List<int> odds = new List<int>();  
            List<int> sum5 = new List<int>();  

            for (int i = 0; i < nums.Length; i++) 
            {
                if (nums[i] % 2 == 0) 
                {
                    evens.Add(nums[i]);
                }
                else
                {
                    odds.Add(nums[i]);
                }
                if (SumDigits(nums[i]) % 10 == 5)
                {
                    sum5.Add(nums[i]); 
                }
            }
            Console.WriteLine(String.Join(", ", evens));
            Console.WriteLine(String.Join(", ", odds));
            Console.WriteLine(String.Join(", ", sum5));
        }
        public static int SumDigits(int number)
        {
            int sum = 0;

            while (number != 0) 
            {
                sum += number % 10;
                number /= 10;
            }

            return sum;
        }
                                            
..................................................................................................................................................                                            
//Великденски яйца
                                            
    static void Main(string[] args)
        {
            Dictionary<string, int> dict = new Dictionary<string, int>();
            int eggs = int.Parse(Console.ReadLine()); 
            for (int i = 0; i < eggs; i++) 
            {
                string color = Console.ReadLine(); 
                if (!dict.ContainsKey(color)) 
                {
                    dict.Add(color, 0); 
                }
                dict[color]++;
            }

            Console.WriteLine($"Red eggs: {(dict.ContainsKey("red") ? dict["red"] : 0)}"); 
            Console.WriteLine($"Orange eggs: {(dict.ContainsKey("orange") ? dict["orange"] : 0)}"); 
            Console.WriteLine($"Blue eggs: {(dict.ContainsKey("blue") ? dict["blue"] : 0)}");
            Console.WriteLine($"Green eggs: {(dict.ContainsKey("green") ? dict["green"] : 0)}");
            Console.WriteLine($"Max eggs: {dict.Values.Max()} -> {dict.OrderByDescending(x => x.Value).FirstOrDefault().Key}");
        }                                           
..................................................................................................................................................                                            
Посочете по кой от начините бихте инициализирали речник с ключ низ и стойност цяло число?
                                     Dictionary<string,int> dict = new Dictionary<string,int>();
..................................................................................................................................................   
            
Опишете по какъв начин ще извлечете дължината на многомерен масив в C#? 
Запишете методите, които ще използвате, за да извлечете броя на редовете на двумерен масив и дължината на всеки от редовете.

            
            Дължина на многомерен масив

Всяка размерност на многомерен масив има собствена дължина, която е достъпна по време на изпълнение на програмата.
int[,] matrix =
{
      {1, 2, 3, 4},    
      {5, 6, 7, 8},
};

Можем да извлечем броя на редовете на този двумерен масив чрез matrix.GetLength(0), а дължината на всеки от редовете (т.е. броя колони) с matrix.GetLength(1).
..................................................................................................................................................            
Посочете кои от характеристиките се отнасят към централизираните сорс-контрол системи и кои към децентрализираните сорс-контрол системи.
Използват един сървър, съдържащ всички контролирани файлове и множество от клиенти, които издърпват файловете от това централно място. [Централизирани]
Клиентите изтеглят последния snapshot на файловете и изцяло клонират цялото хранилище, включително пълната му история. [Децентрализирани]
Администраторите имат подробен контрол върху това кой какво може да прави и освен това е много по-лесно да се администрира. [Централизирани]
Ако сървърът загине, хранилището на даден проект може да се възстанови от локалното копие на всеки клиент. [Децентрализирани]
Всички данни се пазят на едно място и зависят от надеждността на сървъра, който ги съхранява. [Централизирани]
Ако сървърът по някаква причина не е достъпен за час - тогава през този час никой не може да качва своите промени. [Централизирани]

..................................................................................................................................................            
Опишете как се осъществява достъп до елементите на многомерен масив в C#?
            
Достъп до елементите на многомерен масив

Матриците имат две размерности и съответно всеки техен елемент се достъпва с помощта на два индекса – един за редовете и един за коло­ните. Многомерните масиви имат различен индекс за всяка размерност.

Всяка размерност в многомерен масив започва от индекс нула.

int[,] matrix =
{
      {1, 2, 3, 4},    
      {5, 6, 7, 8},
};

Масивът matrix има 8 елемента, разположени в 2 реда и 4 колони. Всеки елемент може да се достъпи по следния начин: matrix[0, 0]  matrix[0, 1] и т.н.
Ако означим индекса по редове с row, а индекса по колони с col, тогава достъпа до елемент от двумерен масив има следния общ вид: matrix[row, col].
При многомерните масиви всеки елемент се идентифицира уникално с толкова на брой индекси, колкото е размерността на масива: nDimensionalArray[index1, … , indexN]

..................................................................................................................................................            
Дефинирайте понятието сорс-контрол система. Какво представляват? За какво служат? Как се използват?
            
Система за контрол на версиите (Version control system) е механизмът, по който се управлява работата по даден софтуерен проект. За да се улесни разработката на софтуер са създадени специални системи, които намаляват неудобствата при съвместна работа на много хора върху един проект.
Системите за контрол на версиите обикновено използват едно централно хранилище, в което се съхраняват файловете на проекта. Когато някой започне да работи по този проект, той създава копие на файловете от това хранилище на своята система и работи с тези копия. В процеса на работа потребителят може да изпраща към хранилището направените от него промени и да получава промените, направени по проекта от другите хора в екипа.
След обновяване на хранилището, в него се запазват старите версии на променените файлове. Така тези файлове могат да бъдат възстановени при необходимост. Системата за контрол на версиите също така следи за конфликти – различни промени на различните потребители, които ползват хранилището.

..................................................................................................................................................
Демонстрирайте как ще запишете с код на C# променлива от тип символен низ със стойност: Hello, my name is Niki. Запишете отговора в полето.
Правилният отговор е: string text = "Hello, my name is Niki.";
..................................................................................................................................................
Дайте пример за това как бихте декларирали променлива от реален тип с десетична точност със стойност 13.45?
Правилният отговор е: decimal num = 13.45m;
            
..................................................................................................................................................            
Напишете примерен код на C#, който да прочете от конзолата матрица с 3 реда и 4 колони със следните стойности:
3 4 5 2
1 5 8 9
4 5 3 6

            int rows = 3;
            int cols = 4;
            int[,] matrix = new int[rows, cols];
            for (int row = 0; row < rows; row++)
            {
                int[] numbers = Console.ReadLine().Split().Select(int.Parse).ToArray();
                for (int col = 0; col < cols; col++)
                {
                    matrix[row, col] = numbers[col];
                }
            }
..................................................................................................................................................            
//Баскетболен сезон
            
              static void Main(string[] args)
        {
            SortedDictionary<string, int> dict = new SortedDictionary<string, int>();

            string[] input = Console.ReadLine().Split(" - ", StringSplitOptions.RemoveEmptyEntries); 
            while (!input[0].Equals("END"))
            {
                if (!dict.ContainsKey(input[0]))
                { 
                    dict.Add(input[0], 0); 
                }
                dict[input[0]] += int.Parse(input[1]); 
                input = Console.ReadLine().Split(" - ", StringSplitOptions.RemoveEmptyEntries); 
            }

            foreach (var kvp in dict) 
            {
                Console.WriteLine($"{kvp.Key} -> {kvp.Value}"); 
            }
        }
 
            
..................................................................................................................................................           
Какво представляват бройните системи? Дефинирайте понятието бройна система, като поставите липсващите думи в изреченията. 

Бройните системи са начин за [представяне] на числата, чрез [краен набор] от [графични знаци] наречени цифри. Към тях трябва да се добавят и [правила] за представяне на числата.

..................................................................................................................................................
Опишете как се декларира едномерен масив в C# като попълните празните думи в текста:
В C# масивите имат [фиксирана] дължина, която се указва при [инициализирането ] им и определя [броя на елементите им]. След като веднъж е зададена [дължината ] на масив при неговото създаване, след това [не е възможно да се променя].
..................................................................................................................................................
Посочете кое от изброените е вярно за символните низове?
Символните низове имат свойство Length., Символните низове позволяват достъп по индекс.
..................................................................................................................................................            
Дефинирайте понятието многомерен масив в C#. 
Всеки допустим в C# тип може да бъде използван за тип на елементите на масив. Масивите също може да се разглеждат като допустим тип. Едномерен масив от цели числа декларираме с int[], а двумерен масив с int[,].
Такива масиви се наричат двумерни, защото имат две измерения или още матрици (терминът идва от математиката). Масиви с повече от едно измерение се наричат многомерни.
Аналогично можем да декларираме и тримерни масиви като добавим още едно измерение int[,,].
..................................................................................................................................................            
Опишете как ще преминете от двоична бройна система в десетична.
Преобразувайте числото  10110101(2)  от двоична в десетична бройна система.

При преминаване от двоична в десетична бройна система, се извършва преобразуване на двоичното число в десетично. Числата записани в двоична бройна система се състоят от двоични цифри, които са подредени по степените на двойката. 
Всяка една двоична цифра се умножава по 2 на степен, позицията, на която се намира (в двоичното число). Накрая се извършва събиране на числата, получени за всяка от двоичните цифри, за да се получи десетичната равностойност на двоичното число.

10110101(2)  = 1х27 + 0х26+ 1х25+ 1х24 + 0х23 + 1х22 + 0х21 + 1х20

                          = 128(10) + 0(10) + 32(10) + 16(10) + 0(10) + 4(10) + 0(10) + 1(10)= 181
       
..................................................................................................................................................
Посочете по кой от начините ще добавите стойност в речник, ако речника има за ключ тип данни низ и за стойност целочислен тип данни?
Правилният отговор е: dict.Add("tomatoes", 2);  
..................................................................................................................................................            
В най-популярната система за контрол на версиите GitHub има няколко основни команди, които се използват когато пишете в конзолния клиент GitBash. Обяснете какво прави командата git push, като поставите липсващите думи в празните полета.
С командата push [качвате] промените в отдалеченото хранилище.
..................................................................................................................................................
![image](https://github.com/arndv/2/assets/125039034/1b05c26f-9137-4c48-9d7f-14374a09fcf8)
            
           for (int row = 0; row < matrix.GetLength(0); row++)
{
      for (int col = 0; col < matrix.GetLength(1); col++)
      {
             Console.Write(matrix[row, col]);
      }
      Console.WriteLine();
}

..................................................................................................................................................            
В най-популярната система за контрол на версиите GitHub има няколко основни команди, които се използват когато пишете в конзолния клиент GitBash. Обяснете какво прави командата git commit, като поставите липсващите думи в празните полета.
След като промените са готови (staged), с командата commit [публикувате] промените.

..................................................................................................................................................            
Демонстрирайте с C# код по какъв начин ще декларирате и ще заделите място в паметта на масив, който съдържа целочислен тип данни и е с дължина 6?

int[] arrary = new int[6];   
..................................................................................................................................................            
Имате някакъв текст. Вашата задача е да намерите всички различни думи в текста, както и колко пъти се среща всяка една от тях. Като допълнително условие имате и да изведете намерените думи по азбучен ред.
Посочете кой от класовете в C# е най-подходящ да използвате, за да решите дадения проблем?
Правилният отговор е: SortedDictionary 
..................................................................................................................................................            
Дайте пример за това как бихте декларирали променлива от целочислен тип със стойност 10?
Правилният отговор е: int num = 10;
