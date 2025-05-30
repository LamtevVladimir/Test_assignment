# Описание работы
Так как в описании задания уже были даны списки доменов и адресов, то в начале программе они прописаны соответствующе. Можно дописать программу, доделав ввод этих данных из стороннего файла/базы данных или ввода из консоли.

Программа построена как бесконечный цикл: когда программа через консоль получает на вход строку, она её обрабатывает и выдаёт результат, после чего можно снова написать строку. Для завершения работы программы нужно написать команду "stop" в консоли.

При обработке строки запускается цикл for, который проходит по каждому домену. Рассмотрим алгоритм для конкретного домена: 
1) поиск исключений; при нахождении хотя бы одного поднимается "f";
2) если флаг поднят (if (f == 1)), то из строки удаляются все адреса из списка для подстановки;
3) усли флаг не поднят, то роверяется есть ли домен в строке (else if (...)). Если правило выполняется, то из списка для подстановки добавляются адреса, которых ещё не было в строке;

Все вносимые данные записываются как строка "origin", в таком ввиде и обрабатываюся.
Программа написана на языке C#.

# Возможные улучшения

Для дальнейшего длительного использования и создании новых программ и приложений на основе этой работы можно провести ряд улучшений:
1) сделать ввод списков начальных данных;
2) пункты 2) и 3) из алгоритма работы программы можно вынести как отдельный метод
3) можно провести оптимизацию

# Тестовые запуски

Input:
To: t.kogni@vtb.ru; i.ivanov@tbank.ru Copy: e.gras@tbank.ru; t.tbankovich@tbank.ru; v.veronickovna@tbank.ru
To: v.veronickovna@tbank.ru; t.kogni@acl.com; i.ivanov@tbank.ru; v.veronickovna@tbank.ru Copy: e.gras@tbank.ru; t.tbankovich@tbank.ru; v.veronickovna@tbank.ru
To: z.xcy@email.com Copy: p.rivet@email.com 
To: t.kogni@acl.com Copy: i.ivanov@tbank.ru
To: q.qweshnikov@batut.com; w.petrov@alfa.com Copy: f.patit@buisness.com

Output:
To: t.kogni@vtb.ru; i.ivanov@tbank.ru Copy: e.gras@tbank.ru; a.aleksandrov@vtb.ru
To: t.kogni@acl.com; i.ivanov@tbank.ru Copy: e.gras@tbank.ru
To: z.xcy@email.com Copy: p.rivet@email.com 
To: t.kogni@acl.com Copy: i.ivanov@tbank.ru
To: q.qweshnikov@batut.com; w.petrov@alfa.com Copy: f.patit@buisness.com; v.vladislavovich@alfa.com
