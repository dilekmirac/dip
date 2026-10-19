Sobel ve Prewitt Karşılaştırması
Bu çalışmada, görüntü işlemede kenar bulmak için en çok kullanılan iki temel yöntemi yani Sobel ve Prewitt filtrelerini kendi çapımda inceledim ve karşılaştırdım.

İki Filtre Arasındaki Temel Fark
Prewitt ve Sobel filtreleri aslında birbirine acayip benziyor. İkisi de 3'e 3 boyutunda iki farklı matristen oluşuyor; biri yatay çizgileri, diğeri ise dikey çizgileri bulmak için kullanılıyor.

Aralarındaki tek ve en önemli fark sayılarda gizli:

Prewitt filtresinde bütün sayılar 1 ve -1'den ibaret. Yani matrisin içindeki her piksele eşit değer veriyor.

Sobel filtresinde ise orta kısımdaki sayılar 2 (veya -2) yapılmış. Yani merkeze biraz daha fazla ağırlık veriyor.

Hangisi Daha İyi?
İkisini de kod üzerinde deneyince şu farkları net olarak gördüm:

Gürültü Durumu: Resimlerdeki ufak pürüzler ve gürültüler bazen kenar sanılabiliyor. Sobel, merkeze 2 kat ağırlık verdiği için bu tür gürültüleri Prewitt'e göre biraz daha iyi bastırıyor. Tabii ikisinde de en başta Gauss filtresi kullandığımız için resim zaten yumuşuyor, bu da hatalı kenar çıkmasını büyük ölçüde engelliyor.

Kenar Netliği: Sobel filtresi merkezdeki pikselleri önemsediği için kenarları biraz daha belirgin ve kalın çıkarıyor. Prewitt ise biraz daha sade ve yumuşak geçişler bırakıyor.

Kullanım: Açıkçası ikisinin de kod olarak bilgisayarı yorma durumu hemen hemen aynı. Ama piyasada ve derslerde Sobel'in merkeze verdiği ağırlık resmi daha kararlı gösterdiği için genelde herkes Sobel'i tercih ediyor.

Özetle; ikisi de işimizi görüyor ama Sobel merkeze verdiği önemden ötürü kenarları biraz daha net çıkardığı için bana daha mantıklı geldi.
