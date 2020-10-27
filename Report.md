# Отчёт о тестировании программы IntelliJ IDEA

**Задачи**

- Установка IntelliJ IDEA
- Проверка работы программы IntelliJ IDEA, с помощью  запуска кода и смены номера карты:

*Код:*
  ```public class Main {
      public static void main(String[] args) {
        // TODO: подставлять номер карты нужно сюда между двойными кавычками, без пробелов
        String number = "5351719427810741";
        System.out.println(String.format("Result is %s", isValidCardNumber(number) ? "OK" : "FAIL"));
      }
    
      public static boolean isValidCardNumber(String number) {
        if (number == null) {
          return false;
        }
    
        if (number.length() != 16) {
          return false;
        }
    
        long result = 0;
        for (int i = 0; i < number.length(); i++) {
          int digit;
          try {
            digit = Integer.parseInt(number.charAt(i) + "");
          } catch (NumberFormatException e) {
            return false;
          }
    
          if (i % 2 == 0) {
            digit *= 2;
            if (digit > 9) {
              digit -= 9;
            }
          }
          result += digit;
        }
    
        return (result != 0) && (result % 10 == 0);
      }
    }
```


**Краткое описание**

<26/10/2020> - <26/10/2020> было проведено установочное, функциональное, интеграционное тестирование программы IntelliJ IDEA

**На тестирование затрачено:** 

6ч.

### В результате тестирования выявлены следующие дефекты 

[]()
[]()
[]()



## Описание процесса тестирования

**В процессе тестирования использовались следующие артефакты:**

- Отчет о тестировании


**В качестве тестовых данных использовались данные - Домашнего задания к занятию «1.1. Введение в Java: JDK, JRE, JVM, IntelliJ IDEA»:**

*Документация:*

[Руководство по установке IntelliJ IDEA](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/idea.md)

[Сервис банковских карт - freeformatter.com](https://www.freeformatter.com/credit-card-number-generator-validator.html)




**Ожидаемый и фактический результат тестирования**

1. Установка IntelliJ IDEA
- ожидаемый/фактический результат:  проведено упешно
2. Проверка работы программы IntelliJ IDEA, с помощью  запуска кода и смены номера карты
- ожидаемый результат: проведено успешно
- фактический результат: **выявлены ошибки**

 
 

**Тестирование производилось в следующем окружении:**

- Версия и разрядность ОС: Windows 10, версия -1703, сборка ОС 15063.0, процессор х64 
- Версия Java: "11.0.9" 
- IntelliJ IDEA
