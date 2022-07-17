# Patika Veri Yapılar ve Algoritmalar Dersi Insertion Sort Projesi



## **[22,27,16,2,18,6]** -> Insertion Sort

* Bu dizinin insertion sort türüne göre aşamaları:

1. [2,27,16,22,18,6]  // 0. index için en küçük değer bulundu yerleri değiştirildi
2. [2,6,16,22,18,27]  // 1. index için en küçük değer bulundu yerleri değiştirildi
3. [2,6,16,22,18,27]  // 2. index doğru yerde olduğu için işlem yapılmadı bir sonraki indexe geçildi
4. [2,6,16,18,22,27]  // 3. index için en küçük değer bulundu yerleri değiştirildi
5. [2,6,16,18,22,27]  // 4. index doğru yerde olduğu için işlem yapılmadı bir sonraki indexe geçildi
6. [2,6,16,18,22,27]  // 5. index doğru yerde olduğu için işlem yapılmadı ve sorting bitti.

---

* Big-O Gösterimi

n input size için düşündüğümüzde n=6. İlk adımda n tane işlem yaptık hepsini karşılaştırdık ve itemleri sadece yer değiştirdiğimiz için ekstra yer ve işlem kaybı yaşamadık. Daha sonraki adımlarda bir önceki itemin indexi belirlendiği için n=1 olana kadar yani işlem boyutumuz 1'er azalarak devam ediyor. Matematiksel gösterim olarak: 
$$
n+(n-1)+(n-2)+...+(n-(n-1))
$$
Son işlem n-(n-1)=1 olduğu için 1'den n'ye kadar olan sayıların toplamı:
$$
(n(n+1))/2 = (n^2+n)/2 
$$
Big-O Notation'da dominant fonksiyon katsayısı önemsiz olduğundan:
$$
n^2
$$
Sonuç olarak bu fonksiyonun Big-O notation'ı  şudur:
$$
O(n^2)
$$

---

* Time Complexity:
  1. Average Case: Aradığımız sayının ortada olması
  2. Worst Case: Aradığımız Sayının sonda olması
  3. Best Case: Aradığımız sayının dizinin en başında olması

Bütün caselerde insertion sorting yaparken her index için sağındakiler ile karşılaştırdığı için yine O(n^2) olarak bulunur. 

----

* Dizi sıralandıktan sonra "18" sayısının girdiği case: 

18 sayısı 4. adımda doğru indexe alındığı için 3. ve 4. adımların ortada olması nedeniyle Average case olarak değerlendirilir.

---



## **[7,3,5,8,2,9,4,15,6**] -> Insertion Sort

* Bu dizinin insertion sort türüne göre ilk 4 aşamaları:

1. [2,3,5,8,7,9,4,15,6]  // 0. index için en küçük değer bulundu yerleri değiştirildi
2. [2,3,5,8,7,9,4,15,6]  // 1. index doğru yerde olduğu için işlem yapılmadı bir sonraki indexe geçildi
3. [2,3,4,8,7,9,5,15,6]  // 2. index için en küçük değer bulundu yerleri değiştirildi
4. [2,3,4,5,7,9,8,15,6]  // 3. index için en küçük değer bulundu yerleri değiştirildi