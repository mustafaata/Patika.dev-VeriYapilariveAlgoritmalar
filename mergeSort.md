[16,21,11,8,12,22] -> Merge Sort

1)Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
2)Big-O gösterimini yazınız.

|Dizinin sıralanmamış hali|[16,21,11,8,12,22]|
|---|---|
|Diziyi ortadan ikiye böl|[16,21,11] - [8,12,22]|
|Tekrar ikiye böl|[16,21] [11] - [8,12] [22]
|Tek eleman kalana kadar ikiye bölmeye devam et |[16] [21] - [8] [12]|
|Her hücrede tek eleman kaldı. Birleştirmeye başla.|[16,21] [11] - [8,12][22]|
|Birleştirmeye devam et.|[11,16,21] - [8,12,22]|
|Tek parça haline getir.|[8,11,12,16,21,22]|
