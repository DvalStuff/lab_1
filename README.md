# lab_1
Лабораторна робота №1 "Вивчення Git"

0. Підготовка
   Файли для виконання лабораторної роботи були завантаженні з https://githowto.com/githowto.zip та розпаковані на робочий стіл, протягом курсу використовувалась тільки папка repositories.

1. [Хід роботи](screenshots/1.png)<br>
   Почала з того, що налаштувала Git, щоб він знав, хто вносить зміни в проєкти. Я виконала наступні команди у командному рядку:<br>
   <br>git config --global user.name "Kyryllova Sofiia"<br>
   git config --global user.email "bulldoshka3@gmail.com"<br>
   <br>Це дозволить автоматично підписувати всі зміни, які я вношу, моїм ім'ям та електронною поштою. Тепер Git знає, хто відповідальний за будь-які зміни в проєктах.<br>
   Далі я налаштувала Git так, щоб він використовував "main" як назву гілки за замовчуванням. Це важливо, тому що при ініціалізації нових репозиторіїв основна гілка буде називатися "main", а не "master". Для цього виконала команду:<br>
   <br>git config --global init.defaultBranch main<br>
   <br>Тепер кожен новий репозиторій, який я створюю, матиме головну гілку з назвою "main".<br>
   Щоб уникнути проблем з перенесенням рядків при роботі на різних операційних системах, я налаштувала Git відповідно до моєї системи. Оскільки я використовую Windows, виконала наступні команди:<br>
   <br>git config --global core.autocrlf true<br>
   git config --global core.safecrlf warn<br>
   <br>Це налаштування дозволяє Git автоматично перетворювати закінчення рядків у правильний формат під час комітів, а також попереджати мене, якщо є якісь проблеми з закінченням рядків. <br>

   Для початку роботи я створила нову порожню директорію work в рамках директорії repositories. Для цього використала команду:<br>
<br>mkdir work<br>
<br>Після цього я перейшла у новостворену директорію за допомогою:
<br>cd work<br>
<br>У директорії work я створила новий файл hello.html з простим вмістом. Для цього використала команду:<br>
<br>touch hello.html<br>
[скрин етапу](screenshots/1.png)
<br>Далі я відкрила файл hello.html у текстовому редакторі та додала до нього простий HTML-код, який відображає текст «Hello, World» на веб-сторінці.<br>
Ініціалізація Git-репозиторія Щоб перетворити директорію work у Git-репозиторій, я використала команду:<br>
<br>git init<br>
<br>Це створило новий підкаталог .git, який містить усі файли та метадані, необхідні для керування версіями в цьому репозиторії.
<br>Результат виконання команди:<br>
<br>Initialized empty Git repository in /home/alex/githowto/repositories/work/.git/<br>
<br>Додавання файлу до індексу Я додала файл hello.html до індексу Git за допомогою команди:<br>
<br>git add hello.html<br>
<br>Після додавання файлу до індексу я зафіксувала зміни, створивши перший коміт з повідомленням "Initial commit":<br>
<br>git commit -m "Initial commit"<br>
<br>Результат виконання команди:<br>
[main (root-commit) 5836970] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 hello.html<br>
 [скрин етапу](screenshots/2.png)   [скрин етапу](screenshots/3.png)

Першим кроком я відкрила термінал і перейшла до директорії, де розташований мій Git-репозиторій. Для перевірки поточного стану репозиторія я виконала команду:
git status
Результатом виконання команди була наступна інформація:
On branch main
nothing to commit, working tree clean
Це означає, що я перебуваю на гілці main, і немає жодних змін, які потрібно комітити. Мій робочий каталог є чистим, що підтверджує, що всі зміни вже збережені у репозиторії.
Цей етап допоміг мені підтвердити, що мій репозиторій знаходиться в стабільному стані і готовий до подальшої роботи.
 [скрин етапу](screenshots/4.png)

 Я відкрила файл hello.html у редакторі тексту.
Змінила вміст файлу, додавши HTML-теги до вітання. Зберегла зміни у файлі.
Відкрила термінал для перевірки стану робочої директорії.
Виконала команду git status, щоб перевірити статус файлів у репозиторії:
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
    modified:   hello.html
no changes added to commit (use "git add" and/or "git commit -a")
У результаті я побачила, що файл hello.html був змінений, але ці зміни ще не зафіксовані у репозиторії. Git підказує, що для внесення змін у репозиторій потрібно використовувати команду git add. Якщо я не хочу зберігати ці зміни, я можу скористатися командою git restore, щоб скасувати їх.
Якщо я вирішу зберегти зміни, наступним кроком буде виконання команди git add hello.html, щоб підготувати файл до коміту.
Якщо я захочу відмовитися від змін, я скористаюся командою git restore hello.html для повернення до попередньої версії файлу.
 [скрин етапу](screenshots/4.png)

Для того щоб Git зафіксував зміни у файлі hello.html, я використовую команду:
git add hello.html
Ця команда додає файл до індексу (так званої стадії підготовки), що означає, що Git тепер знає про ці зміни. Вони ще не записані остаточно в репозиторій, але готові до коміту.
Після того як я проіндексувала зміни, я перевіряю стан репозиторія за допомогою команди:
git status
Виведення команди виглядає наступним чином:
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  modified:   hello.html
Це означає, що я знаходжуся на гілці main, і зміни у файлі hello.html були проіндексовані. Git повідомляє, що ці зміни готові до коміту.
Якщо я вирішу, що не хочу комітити ці зміни, я можу зняти індексацію змін за допомогою команди:
git restore --staged hello.html
Всі проіндексовані зміни будуть включені в наступний коміт, але поки що вони лише проіндексовані, а не записані остаточно в репозиторій.
 [скрин етапу](screenshots/5.png)

Виконала команду git commit, щоб зафіксувати зміни у репозиторії. Після запуску команди я побачила редактор, в якому потрібно було ввести коментар до коміту.
Я ввела коментар "Added h1 tag" у першому рядку редактора, після чого зберегла файл і вийшла з редактора. Для цього у редакторі Vim я натиснула клавішу ESC, ввела :wq, і натиснула Enter.
Результат команди git commit виглядав наступним чином:
[main 78433de] Added h1 tag
 1 file changed, 1 insertion(+), 1 deletion(-)
Це означає, що зміни були успішно зафіксовані: один файл був змінений, додано один рядок і видалено один рядок.
Після коміту я виконала команду git status, щоб перевірити стан репозиторію. Результат був таким:
On branch main
nothing to commit, working tree clean
Це підтверджує, що всі зміни були зафіксовані, і моя робоча директорія є чистою. Я можу продовжити роботу, оскільки не залишилося невирішених змін.
 [скрин етапу](screenshots/6.png)    [скрин етапу](screenshots/7.png)   [скрин етапу](screenshots/8.png)

Я відкрила файл hello.html і внесла необхідні зміни, щоб додати стандартні HTML теги. Додала теги <html> та <body>.
Після внесення змін я додала файл до індексу Git, використавши команду:
git add hello.html
Наступним кроком було додати секцію <head> до файлу hello.html.
Я перевірила статус репозиторію, щоб переконатися, що зміни були зафіксовані:
git status
У результаті я побачила, що перша зміна (додавання стандартних тегів) була проіндексована і готова до коміту, а друга зміна (додавання заголовка HTML) залишалася непроіндексованою.
Виконала коміт проіндексованих змін з повідомленням:
git commit -m "Added standard HTML page tags"
Перевіривши статус знову, я побачила, що друга зміна досі була непроіндексованою.
Я додала другу зміну до індексу, використовуючи команду:
git add .
Після цього я перевірила статус, щоб впевнитися, що всі зміни були проіндексовані:
git status
Нарешті, я здійснила коміт другої зміни з повідомленням:
git commit -m "Added HTML header"
Тепер всі внесені зміни були зафіксовані у репозиторії.
[скрин етапу](screenshots/9.png)  [скрин етапу](screenshots/10.png)  [скрин етапу](screenshots/11.png)

Отримання списку зроблених змін — функція команди git log. Налаштування проводжу під себе.
[скрин етапу](screenshots/12.png)  

Першим кроком було переглянути історію змін у репозиторії за допомогою команди git log. Я знайшла хеш першого коміту в останньому рядку результату. Хеш першого коміту виглядав так: 863ea9d. Я скопіювала цей хеш для подальшого використання.
Щоб перевірити вміст файлу hello.html на момент першого коміту, я виконала команду:
git checkout 863ea9d
[скрин етапу](screenshots/13.png)  
Після цього я перевірила вміст файлу hello.html за допомогою команди:
cat hello.html
Вміст файлу був таким:
Hello, World!
Це підтвердило, що на момент першого коміту файл містив лише цей текст.
Щоб повернутися до останньої версії коду на гілці main, я скористалася командою:
git switch main
Відповідь Git була наступною:
Previous HEAD position was 863ea9d Initial commit
Switched to branch 'main'
Після цього я знову перевірила вміст файлу hello.html:
cat hello.html
Файл мав в собі всі останні зміни (head, body..).
Це підтвердило, що на гілці main файл hello.html був оновлений до останньої версії.
[скрин етапу](screenshots/14.png)  

Створення тегів проходить за допомогою команди git tag v1. Вони дозволяють пересуватися між комітами не за хешами, а за зрозумілими назвами, які ми їм призначимо.
Для переміщення між тегами використовується: 
git checkout v1
git checkout v1-beta
Також можна подивитися теги у лозі.
git log main --all
[скрин етапу](screenshots/15.png)   [скрин етапу](screenshots/16.png)  

Я впевнилася, що перебуваю на останньому коміті гілки main, як зазначено в інструкції. Для цього я виконала команду:
git switch main
Наступним кроком було внести зміни у файл hello.html. Я додала небажаний коментар у цей файл.
Перевірила стан робочої директорії, щоб дізнатися про статус змін. Для цього виконала команду:
git status
Результат показав, що файл hello.html був змінений, але ще не проіндексований:
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   hello.html
no changes added to commit (use "git add" and/or "git commit -a")
Вирішила скасувати внесені зміни у файлі hello.html і повернути його до версії, яка була в репозиторії. Для цього я використала команду:
git checkout hello.html
Після цього я перевірила стан робочої директорії знову:
git status
Результат показав, що в робочій директорії немає незафіксованих змін, і файл hello.html повернувся до свого початкового стану. Я також перевірила вміст файлу за допомогою команди:
cat hello.html
Таким чином, небажаний коментар був успішно видалений з файлу, і я підтвердила, що робоча директорія чиста і готова до подальших змін.
 [скрин етапу](screenshots/17.png)   [скрин етапу](screenshots/18.png)   [скрин етапу](screenshots/19.png)  

Знову додала небажанний коментарій до коду.
Після цього я проіндексувала ці зміни за допомогою команди:
git add hello.html
Перевірила стан репозиторію, щоб упевнитися, що зміни були проіндексовані. Виконала команду:
git status
Результат показав, що файл hello.html був модифікований і готовий до коміту:
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  modified:   hello.html
Щоб скасувати індексацію змін і повернути файл у попередній стан, я використала команду git reset:
git reset HEAD hello.html
Результат показав, що зміни були відкликані з індексації, але залишились у робочій директорії:
Unstaged changes after reset:
M	hello.html
Щоб видалити небажані зміни з робочої директорії, я скористалася командою git checkout:
git checkout hello.html
Потім я знову перевірила стан репозиторію:
git status
Результат показав, що робоча директорія чиста, і всі небажані зміни були видалені.
 [скрин етапу](screenshots/20.png)  

Скасуємо коміт шляхом створення нового коміту, що скасовує небажані зміни. Використовую:
git add hello.html
git commit -m "Oops, we didn't want this commit"
Для скасування останнього коміту використала команду git revert HEAD. Ця команда створює новий коміт, який скасовує зміни, внесені в останньому коміті. В результаті виконання команди відкрився редактор, в якому я змогла редагувати або залишити стандартне повідомлення коміту. Я зберегла та закрила файл.
Далі перевірила журнал комітів за допомогою команди git log. Ця команда показала всі коміти, включаючи той, який був скасований. Я переконалася, що у логу є і новий коміт, який скасовує попередній.
У логу видно, що новий коміт "Revert" з'явився на вершині списку, і він скасовує попередній небажаний коміт.
 [скрин етапу](screenshots/21.png)   [скрин етапу](screenshots/22.png)  

Два останні коміти — "Oops" і "Revert Oops" — є помилковими і їх потрібно видалити.
Перед видаленням комітів я позначила останній коміт тегом "oops", щоб потім можна було до нього повернутися. Для цього виконала команду:
git tag oops
Результат підтвердив, що тег було успішно додано.
Вирішила скинути гілку до коміту з тегом "v1", який є попереднім до помилкових комітів. Для цього виконала команду:
git reset --hard v1
Команда виконалась успішно, і результат був наступним:
HEAD is now at 0e97af7 Added HTML header
Перегляд історії комітів після скидання підтвердив, що гілка тепер вказує на коміт "v1", а коміти "Revert Oops" і "Oops" більше не з'являються в історії.
Щоб перевірити, що коміти "Revert Oops" і "Oops" не зникли остаточно, я виконала команду:
git log --all
Результат показав, що помилкові коміти все ще присутні в репозиторії, але більше не є частиною основної гілки.
Тег oops свою функцію виконав, видалимо його. Це дасть змогу внутрішньому механізму Git прибрати залишкові коміти, на які тепер не посилаються жодні гілки або теги.
git tag -d oops
 [скрин етапу](screenshots/23.png)   [скрин етапу](screenshots/24.png)  

 Спочатку я додала файл hello.html до індексу Git за допомогою команди:
git add hello.html
Потім створила коміт з повідомленням:
git commit -m "Added copyright statement"
Це додало один файл з однією вставкою до коміту. Результат команди git log показав, що новий коміт був створений з повідомленням "Added copyright statement" і відобразився на початку історії комітів.
Відредагувала файл hello.html, додавши адресу електронної пошти автора.
Для того, щоб включити адресу електронної пошти в коміт без створення нового коміту, я використала команду:
git add hello.html
git commit --amend -m "Added copyright statement with email"
Це дозволило змінити останній коміт, додавши оновлену інформацію про автора. Після цього git log показав, що коміт був змінений, і повідомлення коміту тепер включало електронну пошту.
[скрин етапу](screenshots/25.png)  [скрин етапу](screenshots/26.png)  

Роблю сторінку більш привабливою, додавши CSS-стилі. Для цього я створила нову гілку в Git під назвою style. Виконала команду:
git switch -c style
Це дозволило мені перейти до нової гілки безпосередньо. Перевірила поточний стан репозиторію за допомогою команди:
git status
Результат підтвердив, що я перебуваю в гілці style, і робоча директорія була чистою.
Додавання файлу стилів Далі я створила новий файл стилів style.css. Для цього виконала команду:
touch style.css
У файлі style.css я прописала, щоб заголовки H1 відображалися червоним кольором.
Після цього додала файл до індексації за допомогою команди:
git add style.css
І виконала коміт з повідомленням:
git commit -m "Added css stylesheet"
Редагування файлу hello.html Щоб підключити новий файл стилів до сторінки, я відредагувала файл hello.html.
І виконала коміт:
git commit -m "Included stylesheet into hello.html"
Перевірка результатів Після внесення змін та коміту, перевірила роботу локально, переконавшись, що заголовок на сторінці відображається червоним кольором відповідно до правил CSS.
[скрин етапу](screenshots/27.png)  [скрин етапу](screenshots/28.png)  

Тепер у проєкті є дві гілки: main і style. Наступним кроком я перемкнулася на гілку main за допомогою команди:
git switch main
Перевірила вміст файлу hello.html командою:
cat hello.html
У гілці main немає стилів, підключених через файл style.css. Це потрібна нам версія.
Далі я повернулася до гілки style за допомогою команди:
git switch style
Знову перевірила вміст файлу hello.html:
cat hello.html
Цього разу у файлі були присутні зміни, пов'язані з CSS.
Таким чином, я побачила, що всі зміни, зроблені у гілці style, збережені і відображають підключення файлу стилів.
[скрин етапу](screenshots/29.png)  [скрин етапу](screenshots/30.png)  

Для початку я переглянула історію змін файлів hello.html і style.css за допомогою команди git log.
git log hello.html
Результат показав всі коміти, в яких був змінений hello.html:
Потім я перевірила історію style.css:
git log style.css
Перегляд змін у конкретному коміті, зміни були внесені до файлу hello.html у коміті з тегом v1. Для цього використала команду git show.
git show v1
Результат показав зміни у файлі hello.html в коміті з тегом v1.
Я перейменувала файл hello.html на index.html за допомогою команди mv, а потім перевірила статус змін.
mv hello.html index.html
git status
Git показав, що hello.html був видалений, а index.html був створений як новий файл:
deleted:    hello.html
Untracked files:
  index.html
Далі я додала зміни до індексу:
git add .
git status
Тепер Git розпізнав перейменування:
renamed:    hello.html -> index.html
Переміщення файлу без втрати історії Я створила нову директорію css і перемістила файл style.css до цієї директорії, використовуючи команду git mv:
mkdir css
git mv style.css css/style.css
git status
Результат показав, що style.css був переміщений до css/style.css:
renamed:    style.css -> css/style.css
Я закомітила зміни:
git commit -m "Renamed hello.html; moved style.css"
Нарешті, я перевірила історію змін для css/style.css з і без опції --follow, щоб побачити історію файлу до та після переміщення:
git log css/style.css
git log --follow css/style.css
Результат показав, що історія файлу була збережена і правильно відображена.
[скрин етапу](screenshots/31.png)  [скрин етапу](screenshots/32.png)  [скрин етапу](screenshots/33.png)  

Створила файл README. Він буде пояснювати, про що мій проєкт.
Наразі я перебуваю у гілці style. Файл README не є частиною цієї гілки, тому перед комітом слід перейти до гілки main:
git switch main
git add README
git commit -m "Added README"
Тепер у репозиторії є дві гілки, що розходяться. Виконую команду log, щоб переглянути гілки і те, як вони розходяться.
git log --all --graph
Злиття переносить зміни з двох гілок в одну. Повертаємося до гілки style і зливаємо main із style.
git switch style
git merge main
git log --all --graph
[скрин етапу](screenshots/34.png)  [скрин етапу](screenshots/35.png)  

Спочатку я повернулася на гілку main, виконавши команду:
git switch main
У файлі hello.html я додала метаінформацію про автора.
Після редагування файлу я виконала команду, щоб додати зміни:
git add hello.html
Cтворила новий коміт із повідомленням:
git commit -m "Added meta title"
Щоб побачити структуру гілок, я використала команду:
git log --all --graph
Виявилося, що після коміту «Added README» гілка main була об'єднана з гілкою style, але в гілці main є новий коміт, який поки не злитий з style.
[скрин етапу](screenshots/36.png)  

Почала роботу з переходу на гілку style, щоб потім з нею злити зміни з main. Виконала команди:
git switch style
git merge main
Після злиття отримала повідомлення про конфлікт у файлі index.html. Переглянула конфліктні зміни.
Це було очікувано, тому спочатку перевірила стан репозиторію за допомогою команди:
git status
У результаті побачила, що є "unmerged paths", а саме — конфлікт у index.html. Розуміючи, що можу скасувати злиття, спробувала команду:
git merge --abort
Ця команда відмінила злиття, і після перевірки статусу за допомогою git status я переконалася, що конфлікт більше не впливає на робочу гілку.
Після цього я вирішила повторно виконати злиття:
git merge main
Щоб вирішити конфлікт, вручну відредагувала файл index.html, об'єднавши обидві частини коду. 
Після редагування, додала файл до індексу і закомітила його:
git add index.html
git commit -m "Resolved merge conflict"
Знову перевірила статус репозиторію:
git status
Усе виглядало добре, тож виконала команду git log --all --graph, щоб переконатися, що історія змін була правильно оновлена після злиття.
[скрин етапу](screenshots/37.png)  [скрин етапу](screenshots/38.png)  

Переходимо до гілки style за допомогою команди:
git switch style
Оскільки я вже перебувала на цій гілці, система повідомила: "Already on 'style'".
Далі я переглянула історію комітів за допомогою команди:
git log --graph
Це дало мені детальний список комітів, де я знайшла останній коміт перед злиттям — це був коміт з повідомленням "Renamed hello.html; moved style.css". Його хеш — 0f19376, але, щоб полегшити собі завдання, я вирішила використовувати позначення HEAD2, яке вказує на коміт за два кроки від останнього.
Для скидання гілки до цього коміту я виконала:
git reset --hard HEAD~2
Після цього гілка style повернулася до стану перед злиттям з main, і повідомлення підтвердило це:
HEAD is now at 0f19376 Renamed hello.html; moved style.css
Щоб перевірити, що все пройшло успішно і що більше немає комітів злиття, я знову переглянула історію комітів командою:
git log --graph
Як і очікувалося, комітів злиття більше не було, і тепер гілка style повернулася до стану перед злиттям з основною гілкою.
[скрин етапу](screenshots/39.png)  [скрин етапу](screenshots/40.png)  

Перебазування гілки style на main, щоб перенести зміни з main до моєї гілки, замість того, щоб використовувати звичну команду merge.
Переключилася на гілку style за допомогою команди:
git switch style
Далі я виконала команду перебазування:
git rebase main
Процес перебазування почався, але виник конфлікт у файлі hello.html, де зміни з style і main не могли бути автоматично об'єднані. Я вручну вирішила конфлікт, відредагувавши файл так, щоб він відповідав моїм очікуванням.
Після цього я додала зміни до індексу:
git add .
Та продовжила процес rebase:
git rebase --continue
Git завершив перебазування, і я перевірила статус:
git status
Все було успішно, і я переглянула історію комітів за допомогою команди:
git log --all --graph
Тепер гілка style містить всі зміни з гілки main.
[скрин етапу](screenshots/41.png)  [скрин етапу](screenshots/42.png)  [скрин етапу](screenshots/43.png)  

Тепер зіллю зміни style в гілку main.
git switch main
git merge style
Оскільки остання фіксація у гілці main безпосередньо передує останній фіксації у гілці style, Git може об'єднати швидке перемотування вперед, просто пересунувши вказівник гілки вперед, щоб він вказував на ту саму фіксацію, що й у гілці style.
Переглядаю логи:
git log --all --graph
Тепер гілки style і main ідентичні.
[скрин етапу](screenshots/44.png)  

Я перейшла в директорію, де буду працювати з репозиторіями. Для цього виконала наступні команди:
cd ..
pwd
ls
Перевіривши вміст директорії за допомогою команди ls, я побачила єдиний репозиторій під назвою work, що означає правильне місцезнаходження в директорії repositories.
Далі я вирішила створити клон репозиторія work, використовуючи команду git clone. Це дозволяє створити точну копію наявного репозиторія для подальшої роботи з нею:
git clone work home
ls
У результаті у мене з'явилося два репозиторії в директорії repositories: оригінальний репозиторій work і новий клонований репозиторій home.
[скрин етапу](screenshots/45.png)  

Перейшла в папку home, щоб переглянути файли, які знаходяться в клонованому репозиторії. Виконала команду:
cd home
Потім ввела команду для перегляду вмісту директорії:
ls
У результаті я побачила файли на верхньому рівні репозиторія: css, index.html, та README.
Перегляд історії репозиторія Щоб переглянути історію комітів у цьому репозиторії, я скористалася командою:
git log --all --graph
Історія комітів в моєму репозиторії збігалася з оригінальною історією комітів, яка була в репозиторії, з якого я клонувала.
[скрин етапу](screenshots/46.png)  

Спершу перевірила, які віддалені репозиторії налаштовані в моєму проекті. Для цього я ввела команду:
git remote
У результаті я побачила, що віддалений репозиторій називається origin. Це стандартна назва для віддалених репозиторіїв за замовчуванням після клонування. 
git remote show origin
Результат показав деталі, зокрема URL для отримання і надсилання даних (fetch та push), головну гілку main, а також інші віддалені гілки, з якими працює репозиторій. Також я дізналася, що моя локальна гілка main налаштована для автоматичного злиття з віддаленою гілкою main.
[скрин етапу](screenshots/47.png)  

Вирішила переглянути локальні гілки за допомогою команди:
git branch

Якщо хочется побачити всі доступні гілки, включно з віддаленими. Для цього є команда:
git branch -a
Результат показав всі гілки, включно з віддаленими.
Отже, крім локальної гілки main, я побачила дві віддалені гілки: origin/style та origin/main. Ці гілки існують на віддаленому сервері, але не є локальними.
[скрин етапу](screenshots/48.png)  

Я перейшла в репозиторій work, виконавши команду:
cd ../work
Після цього відкрила файл README та внесла наступні зміни:
This is the Hello World example from the Git tutorial.
(changed in origin)
Збережені зміни додала до індексу за допомогою команди:
git add README
Далі я зробила коміт, використавши таку команду:
git commit -m "Changed README in original repo"
Тепер в оригінальному репозиторії є оновлення, яких ще немає в клонованій версії. На наступному етапі я перенесу ці зміни до клонованого репозиторія і зіллю їх для синхронізації двох репозиторіїв.
[скрин етапу](screenshots/49.png)  

Перейшла до необхідної директорії командою:
cd ../home
Далі я виконала команду git fetch, щоб підтягнути нові коміти з віддаленого репозиторія.
Після цього я переглянула історію всіх комітів за допомогою команди:
git log --all --graph
В результаті вивелося дерево комітів, де я знайшла коміт з описом «Changed README in original repo». Цей коміт містив у собі коміти з origin/main та origin/HEAD. Також я звернула увагу на коміт «Renamed hello.html; moved style.css», на який вказувала моя локальна гілка main.
Я зробила висновок, що команда git fetch дозволяє підтягувати нові коміти з віддаленого репозиторія, але не зливає їх автоматично з моїми локальними гілками. Для демонстрації того, що зміни в файлі README не відбулися в локальній версії, я виконала команду:
cat README
У виведеному результаті файл залишився без змін:
This is the Hello World example from the GitHowTo tutorial.
Таким чином, я переконалася, що команда git fetch не змінює локальні файли без явного злиття змін.
[скрин етапу](screenshots/49.png)  

Отримавши підтягнуті зміни з віддаленого репозиторія, тепер їх потрібно злити локальну гілку main. Для цього я використала команду:
git merge origin/main
Зміни в файлі README були успішно інтегровані. Було додано дві вставки та одна частина тексту була видалена.
Щоб переконатися, що зміни відбулися, я скористалася командою для перегляду вмісту файлу README:
cat README
В результаті побачила наступне:
This is the Hello World example from the Git tutorial.
(changed in origin)
Як видно, зміни в файлі README були успішно застосовані. Цей файл тепер містить оновлену інформацію з віддаленого репозиторія.
Дізнавшись про різницю між командами git fetch та git merge, я зрозуміла, що можна використовувати також команду git pull, яка поєднує ці дві дії в одну. Для майбутніх завдань я буду використовувати:
git pull
Це зручно, оскільки дозволяє підтягути і зливати зміни одним викликом.
[скрин етапу](screenshots/50.png)  

Я виконав команду для налаштування відстеження віддаленої гілки style:
git branch --track style origin/style
Ця команда налаштовує локальну гілку style для відстеження віддаленої гілки origin/style. Результат підтвердив, що гілка style тепер відстежує віддалену гілку style з репозиторію origin.
Далі я перевірив список всіх гілок у репозиторії за допомогою команди:
git branch -a
Результат показав, що у моєму локальному репозиторії є дві гілки: main і style. Також були відображені віддалені гілки: remotes/origin/HEAD, remotes/origin/main, і remotes/origin/style.
Щоб перевірити останні коміти, я використав команду:
git log --all --graph --max-count=2
[скрин етапу](screenshots/51.png)  

Спочатку перейшла на один рівень вище, щоб бути в директорії repositories.
cd ..
Далі я виконала команду для клонування репозиторія у вигляді чистого (bare) репозиторія:
git clone --bare work work.git
В результаті цієї команди був створений чистий репозиторій з назвою work.git.
Перевірила вміст директорії work.git за допомогою команди:
ls work.git
Результат показав, що директорія містить деякі елементи.
Оскільки репозиторій є чистим, я побачила, що в директорії work.git немає робочих файлів. Це вірно, оскільки чистий (bare) репозиторій є лише директорією .git зі звичайного репозиторія без робочих файлів.
[скрин етапу](screenshots/52.png)  

Додаю репозиторій work.git до нашого оригінального репозиторія:
cd work
git remote add shared ../work.git
[скрин етапу](screenshots/53.png)  

Відкрила файл README і внесла зміни до тексту. Замінила його на:
This is the Hello World example from the Git tutorial.
(changed in the origin and pushed to shared)
Це потрібно було зробити для того, щоб створити нову зміну, яку я потім відправлю в спільний репозиторій.
Я переключилася на гілку main, щоб мати можливість комітити зміни:
git switch main
Потім додала відредагований файл до індексу:
git add README
Створила коміт з описом змін:
git commit -m "Added shared comment to readme"
Відправлення змін до спільного репозиторія
Щоб передати свої зміни до спільного репозиторія, я виконала команду:
git push shared main
В результаті команда підтвердила, що зміни були успішно відправлені до репозиторія.
[скрин етапу](screenshots/53.png)  

