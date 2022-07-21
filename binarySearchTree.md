Proje 3
[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree aşamalarını yazınız.

Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.

Binary search tree oluşturulurken yapılması gereken ilk şey root belirlenmesidir. Ağaç üzerinde yapılan aramanın çok uzun sürmemesi için root ortanca eleman seçilmelidir.

| Dizi = |   | 7 | 5 | 1 | 8 | 3 | 6 | 0 | 9 | 4 | 2 |
|--------|---|---|---|---|---|---|---|---|---|---|---|
| Root = |   |   |   |   |   | 5 |   |   |   |   |   |

Yukarıdaki örnekte görüldüğü gibi Root 5 olarak belirlenmiştir.

Daha sonrasında yapılacak işlem ise elemanların eklenmesidir. Her eklenecek eleman root'tan küçükse soluna, root'tan büyükse sağına eklenir. Daha sonra eklenecek elemanlar
da bu kıyasa dahil edilir ve eklenen elemanlarla arasındaki büyüklük küçüklük ilişkisine bakılır. Yeni eleman eklenen elemandan küçükse o elemanın soluna, büyükse sağına
yazılır.


| 1. aşama |   |   |   |   |   | 5 |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|

| 2. aşama |   |   |   |   |   | 5 |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|
|          |   |   |   |   |   |   | \ |   |   |   |   |
| Ekle 7   |   |   |   |   |   |   |   | 7 |   |   |   |

| 3. aşama |   |   |   |   |   | 5 |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|
|          |   |   |   |   | / |   | \ |   |   |   |   |
| Ekle 1   |   |   |   | 1 |   |   |   | 7 |   |   |   |

| 4. aşama |   |   |   |   |   | 5 |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|
|          |   |   |   |   | / |   | \ |   |   |   |   |
|          |   |   |   | 1 |   |   |   | 7 |   |   |   |
|          |   |   |   |   |   |   |   |   | \ |   |   |
| Ekle 8   |   |   |   |   |   |   |   |   |   | 8 |   |

| 5. aşama |   |   |   |   |   | 5 |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|
|          |   |   |   |   | / |   | \ |   |   |   |   |
|          |   |   |   | 1 |   |   |   | 7 |   |   |   |
|          |   |   |   |   | \ |   |   |   | \ |   |   |
| Ekle 3   |   |   |   |   |   | 3 |   |   |   | 8 |   |

| 6. aşama |   |   |   |   |   | 5 |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|
|          |   |   |   | / |   |   |   | \ |   |   |   |
|          |   |   | 1 |   |   |   |   |   | 7 |   |   |
|          |   |   |   | \ |   |   |   | / |   | \ |   |
| Ekle 6   |   |   |   |   | 3 |   | 6 |   |   |   | 8 |

| 7. aşama |   |   |   |   |   | 5 |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|
|          |   |   |   | / |   |   |   | \ |   |   |   |
|          |   |   | 1 |   |   |   |   |   | 7 |   |   |
|          |   | / |   | \ |   |   |   | / |   | \ |   |
| Ekle 0   | 0 |   |   |   | 3 |   | 6 |   |   |   | 8 |

| 8. aşama |   |   |   |   |   | 5 |   |   |   |   |   |   |   |
|----------|---|---|---|---|---|---|---|---|---|---|---|---|---|
|          |   |   |   | / |   |   |   | \ |   |   |   |   |   |
|          |   |   | 1 |   |   |   |   |   | 7 |   |   |   |   |
|          |   | / |   | \ |   |   |   | / |   | \ |   |   |   |
|          | 0 |   |   |   | 3 |   | 6 |   |   |   | 8 |   |   |
|          |   |   |   |   |   |   |   |   |   |   |   | \ |   |
| Ekle 9   |   |   |   |   |   |   |   |   |   |   |   |   | 9 |

| 9. aşama |   |   |   |   |   | 5 |   |
|----------|---|---|---|---|---|---|---|
|          |   |   |   | / |   |   |   |
|          |   |   | 1 |   |   |   |   |
|          |   | / |   | \ |   |   |   |
|          | 0 |   |   |   | 3 |   |   |
|          |   |   |   |   |   | \ |   |
| Ekle 4   |   |   |   |   |   |   | 4 |

Not: Kökün sağ tarafı aynı olduğundan yazılmamıştır.

| 10. aşama |   |   |   |   |   | 5 |   |
|-----------|---|---|---|---|---|---|---|
|           |   |   |   | / |   |   |   |
|           |   |   | 1 |   |   |   |   |
|           |   | / |   | \ |   |   |   |
|           | 0 |   |   |   | 3 |   |   |
|           |   |   |   | / |   | \ |   |
| Ekle 2    |   |   | 2 |   |   |   | 4 |

Not: Kökün sağ tarafı aynı olduğundan yazılmamıştır.

<b> Ağacın tam hali </b>
| Tree |   |   |   | - | - | - | 5 | - | - | - |   |   |   |    |
|------|---|---|---|---|---|---|---|---|---|---|---|---|---|----|
|      |   |   | 1 |   |   |   |   |   |   |   | 7 |   |   |    |
|      |   | / |   | \ |   |   |   |   |   | / |   | \ |   |    |
|      | 0 |   |   |   | 3 |   |   |   | 6 |   |   |   | 8 |    |
|      |   |   |   | / |   | \ |   |   |   |   |   |   |   | \| |
|      |   |   | 2 |   |   |   | 4 |   |   |   |   |   |   | 9  |
|      |   |   |   |   |   |   |   |   |   |   |   |   |   |    |
|      |   |   |   |   |   |   |   |   |   |   |   |   |   |    |
|      |   |   |   |   |   |   |   |   |   |   |   |   |   |    |

Bu aşamalardan sonra ağaç oluşturulmuş olur. 
