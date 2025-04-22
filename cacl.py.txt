import random

def generate_random_list(length, min_value, max_value):
    """Генерирует список случайных целых чисел."""
    random_list = []
    for _ in range(length):
        random_list.append(random.randint(min_value, max_value))
    return random_list

def calculate_average(numbers):
    """Вычисляет среднее значение списка чисел."""
    if not numbers:
        return 0  # Избегаем деления на ноль
    total = sum(numbers)
    average = total / len(numbers)
    return average

if __name__ == "__main__":
    list_length = 10
    min_range = 1
    max_range = 100

    my_list = generate_random_list(list_length, min_range, max_range)
    print("Сгенерированный список:", my_list)

    average = calculate_average(my_list)
    print("Среднее значение:", average)
