1.  возращение список уникальных чисел

def list(num):
mas = []
for item in num :
 if item not in mas:
 mas.append(item)
return mas

print(list([1, 2, 3, 1, 2]))


2. возврат простых чисел в диапазоне

lower = int(input("нижнее: "))
upper = int(input("верхнее: "))

print("все простые числа в диапозоне: ")
for number in range(lower, upper + 1):
 if number > 1:
 for i in range(2, number):
 if(number % i) == 0:
 break
 else:
 print(number)


3. Создать класс Point, который представляет собой точку в двумерном пространстве. Класс должен иметь методы для инициализации координат точки, вычисления расстояния до другой точки, а также для получения и изменения координат.
class Point:
    def __init__(self, x=0, y=0):
        # Инициализация.
        self.x = x
        self.y = y

    def distance_to(self, other):
        # Вычисление расстояния до другой точки.
        return ((self.x - other.x) ** 2 + (self.y - other.y) ** 2) ** 0.5

    def get_coordinates(self):
        # Получение координат точки в виде кортежа (x, y).
        return self.x, self.y

    def set_coordinates(self, x, y):
        # Установка новых координат точки.
        self.x = x
        self.y = y
4. Написать программу, которая сортирует список строк по длине, сначала по возрастанию, а затем по убыванию.
def sort_strings_by_length(strings):

      #Сортировка по возрастанию длины строки
    sorted_strings_asc = sorted(strings, key=len)

      #Сортировка по убыванию длины строки
    sorted_strings_desc = sorted(strings, key=len, reverse=True)

    return sorted_strings_asc, sorted_strings_desc
