## Завдання

https://play.picoctf.org/practice/challenge/320

## Виконання

1. Скачати файл з сайту

1. Перевірити що за файл ми скачали через утиліту `file`

    ```shell
    ~/tmp> file files.zip 
    files.zip: Zip archive data, made by v3.0 UNIX, extract using at least v1.0, last modified, last modified Sun, May 13 2022 16:07:40, uncompressed size 0, method=store
    ```

1. Програма говорить що ми отримати **zip** архів. Тому розпакуємо його за допомогою `unzip -q`

    ```shell
    ~/tmp> unzip -q files.zip 
    ```

1. В завданні нас попросили знайти файл **uber-secret.txt**, що ми і зробимо за допомогою `find -name uber-secret.txt`

    ```shell
    ~/tmp> find . -name uber-secret.txt
    ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
    ```

1. Використаємо `cd` + Tab для того щоб перейти в каталог **deepest_secrets**

    ```shell
    ~/tmp> cd files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
    ```

1. Зчитаємо вміст файлу через `cat`

    ```
    ~/t/f/a/m/.s/d/deepest_secrets> cat uber-secret.txt 
    picoCTF{f1nd_15_f457_ab443fd1}
    ```