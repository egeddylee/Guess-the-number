"""Игра в угадай число"""
import random


games_played = 0
wins = 0
losses = 0

while True:
    level = input("Выберете уровень сложности: легкий / средний / тяжелый: ").strip().lower()
    games_played+=1
    
    if level == "легкий":
        N = random.randint(1, 10)
        count_left = 7
        print(f"Компьютер загадал число от 1 до 10")
        
    elif level == "средний":
        N = random.randint(1, 20)
        count_left = 5
        print(f"Компьютер загадал число от 1 до 20")
        
    elif level == "тяжелый":
        N = random.randint(1, 50)
        count_left = 3
        print(f"Компьютер загадал число от 1 до 50")
        
    else:
        print("Неизвестный уровень сложности! Ставлю средний...")
        N = random.randint(1, 20)
        count_left = 5
        print(f"Компьютер загадал число от 1 до 20")

    
    while count_left > 0:
        print(f"У Вас осталось {count_left} попыток!")
        
        try:
            n = int(input("Введите ваше число: "))
            
        except ValueError:
            print(f"Ошибка! Вы ввели не число! Попробуйте снова.")
            print()
            continue
        
        if n > N:
            print("Твоё число больше загаданного числа!")
        
        elif n < N:
            print("Твоё число меньше загаданного числа!")
        
        else:
            print("Ура, ты угадал число! Поздравляю!")
            wins+=1
            break
    
        count_left-=1

        if count_left == 0:
            print(f"У Вас закончились попытки! Загаданное число было: {N}.")
            losses+=1
        print()
        
    answer = input("Вы хотите продолжить игру? Y/N?").strip().lower()

    if answer == "y":
        print("Начинаем новую игру!")
        print(f"Сыграно {games_played}, из них {wins} побед и {losses} поражений!")
        continue
    
    elif answer == "n":
        print("Игра завершена!")
        print(f"Было сыграно {games_played}, из них {wins} побед и {losses} поражений!")
        break
    
    else:
        print("Не понял ответа, прерываю игру")
        print(f"Было сыграно {games_played}, из них {wins} побед и {losses} поражений!")
        break
