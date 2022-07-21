# Patika.dev-VeriYapilariveAlgoritmalar-InsertionSortProjesi
Patika.dev - Veri Bilimi Patikası - Veri Yapıları ve Algoritmalar Dersi - Insertion Sort Projesi

Proje 1
[22,27,16,2,18,6] -> Insertion Sort

1) Yukarıda verilen dizinin sort türüne göre aşamalarını yazınız.
2) Big-O gösterimini yazınız.
3) Time Complexity: Average case: Aradığımız sayının ortada olması,Worst case: Aradığımız sayının sonda olması, Best case: Aradığımız sayının dizinin en başında olması.
4) Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.


[7,3,5,8,2,9,4,18,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

1) Insertion Sort

1. [22,27,16,2,18,6] - ilk hal
2. [2,27,16,22,18,6]
3. [2,6,16,22,18,27]
4. [2,6,16,18,22,27] - sıralanmış hal

2) Big-O Notation

Best Case: O(n) - Liste sıralıdır. Hiçbir yer değiştirme yapılmadan yalnızca elemanlar kontrol edilir.
Worst Case: O(n²) - Liste tam tersi şekilde sıralıdır. Her seferinde elemanların yeri değişmelidir.

3) Time Complexity

Best Case: Aranılan elemanın başta olmasıdır. Liste de ona göre tasarlanmalıdır. 
Best Case Senaryosu: [2,6,16,18,22,27]

Worst Case: Aranılan elemanın en sonda olması durumudur.
Worst Case Senaryosu: [27,22,18,16,6,2]

Average Case: Aranılan elemanın ortanca olma veya ortalara yakın olma durumudur.

4) 18 sayısı?

18 sayısı, dizi sıralandıktan sonra 4. elemandır. Average case olarak nitelendirilebilir.


[7,3,5,8,2,9,4,18,6] Insertion Sort

1. [7,3,5,8,2,9,4,18,6] - ilk hal
2. [2,3,5,8,7,9,4,18,6] - 1. aşama
3. [2,3,4,8,7,9,5,18,6] - 2. aşama
4. [2,3,4,5,7,9,8,18,6] - 3. aşama
5. [2,3,4,5,6,9,8,18,7] - 4. aşama
