# Insertion-Sort-Projesi
Patika.dev Veri yapıları ve Algoritmalar dersinin insertion sort projesi.

## Proje Soruları

- [22,27,16,2,18,6] -> Insertion Sort

1. Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.

2. Big-O gösterimini yazınız.

3. Time Complexity: Average case: Aradığımız sayının ortada olması,Worst case: Aradığımız sayının sonda olması, Best case: Aradığımız sayının dizinin en başında olması.

4. Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.

5. [7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

## Çözümler

1.
    - İlk aşamada diziye tek tek bakılır ve en küçük eleman sol baştaki eleman ile yer değiştirir.
    
    `[22,27,16,2,18,6] ---> [2,27,16,22,18,6]`
    
    - Bu aşamadan sonra diziyi ilk yerleştirilen eleman ve geri kalan elemanlar şeklinde ayrı düşünebiliriz.
    
    `[2,|27,16,22,18,6]`
    
    - İlk elemandan sonra, dizinin geri kalanını taranır ve en küçük eleman ikinci sradaki elemanla yer değiştirilir.
    
    `[2,6,|16,22,18,27] `
    
    - Aynı işlem sıradaki her eleman için de uygulanır. Eğer sıradaki eleman zaten geri kalan serinin en küçüğüyse yeri sabit kalır.
    
    ```
    [2,6,16,|22,18,27]
    
    [2,6,16,18,|22,27]
    
    [2,6,16,18,22,|27]
    
    [2,6,16,18,22,27]
    ```
    - İşlem bittiğinde dizi sıralanmış olur.
    
2. Big O gösterimi O(![n kare](https://latex.codecogs.com/png.image?\inline&space;\LARGE&space;\dpi{110}\bg{black}n^2)) olacaktır.

3. - Worst case olarak "n" elemanlı bir dizi insertion algoritmasıyla sıralanırken ilk aşamada "n" eleman kontrol edilecek ve her aşamada kontrol edilen eleman sayısı 1 azalacağından yapılan işlem sayısı "n + (n-1) + (n-2)+...+1" şeklinde olacaktır. Bu ifade "1"den "n"e kadar 1'er 1'er artan sayıların toplamı olduğundan !["1"den "n"e kadar 1'er 1'er artan sayıların toplamı](https://latex.codecogs.com/png.image?\inline&space;\LARGE&space;\dpi{110}\bg{black}\frac{n^2^&space;&plus;&space;n}{2}) şeklinde yazılabilir. Bu ifadede dominant kuvvet ![n kare](https://latex.codecogs.com/png.image?\inline&space;\LARGE&space;\dpi{110}\bg{black}n^2) olduğundan O(![n kare](https://latex.codecogs.com/png.image?\inline&space;\LARGE&space;\dpi{110}\bg{black}n^2)) Time Complexity'sine sahip bir algoritma olur.
    - Average case, elimizdeki dizinin aranan elemanlarının en sonda olmaması ama en başta da olmaması olacaktır. Bu şekilde Time Complexity, kat sayısını bilemesek de O(n) olacaktır.
    - Best case, elimizdeki dizinin hali hazırda küçükten büyüğe sıralı olmasıdır. Bu case "n" işlemde tamamlanacaktır. O yüzden Time Complexity O(n) olur.

4. Dizi sıralandıktan sonra 18 elemanı Average Case kapsamına girecektir.

5. ```
   [7,3,5,8,2,9,4,15,6]
   [2,|3,5,8,7,9,4,15,6]
   [2,3|,5,8,7,9,4,15,6]
   [2,3,4|,8,7,9,5,15,6]
   [2,3,4,5|,7,9,8,15,6]
   ```

 
    
