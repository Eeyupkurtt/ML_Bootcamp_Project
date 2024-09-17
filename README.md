--------------------------------------------------------------------------------PERFORMANS DEĞERLENDİRMESİ----------------------------------------------------------------------------------------------------------------

Bu bölümde, K-Means kümeleme algoritması ile gözetimli öğrenme (F1 skoru) sonuçlarının performansını karşılaştırıyorum.
İki yöntem arasında karşılaştırma yaparak, hangi yaklaşımın daha iyi performans gösterdiğini değerlendirdim.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

K-Means Kümeleme Sonuçları:

Silhouette Skoru;
-0.8: Bu skor, kümelerin iyi bir şekilde ayrıldığını ve veri noktalarının uygun kümelere atandığını göstermektedir. 
Yüksek silhouette skoru, kümeler arasındaki ayrımın iyi olduğunu ve veri noktalarının kendi kümelerinde iyi gruplaştığını gösterir.

Küme Merkezleri ve Özellikler;

n_killed ve n_injured Özellikleri;
-Küme 0: Hem n_killed hem de n_injured için ortalama ve medyan sıfır. Bu küme, düşük ölü ve yaralanma sayısına sahip olayları temsil ediyor olabilir.
-Küme 1: n_killed için ortalama 1.16 ve n_injured için ortalama 0.16. Bu küme, biraz daha yüksek ölü sayısı ve düşük yaralanma sayısı olan olayları temsil ediyor olabilir.
-Küme 2: n_injured için ortalama 1.25, ancak n_killed için ortalama 0.03. Bu küme, daha fazla yaralanma sayısına sahip olayları temsil ediyor olabilir.

Grafik Analizi;
Küme merkezlerinin birbirine yakın olması, kümeler arasındaki ayrımın belirgin olmadığını gösterebilir. 
Sarı ve mavi noktaların 0-10 arasında yoğunlaşması, bu bölgede kümelerin toplandığını ve belirli bir düzenin olduğunu ifade eder.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Gözetimli Öğrenme Sonuçları (F1 Skoru):

F1 Skoru;
-Class 0: F1 skoru 0.85. Modelin bu sınıfta oldukça iyi performans gösterdiğini belirtir.
-Class 1: F1 skoru 0.83. Bu da modelin bu sınıfta iyi bir performans gösterdiğini ifade eder.
-Class 2: F1 skoru 0.10. Bu düşük değer, modelin bu sınıfta zayıf performans gösterdiğini gösterir.
-Class 3, Class 4, ve Class 5: F1 skorları 0.0. Modelin bu sınıflarda neredeyse hiç doğru tahminde bulunamadığını belirtir.

Genel Performans:
-Accuracy: %79.25. Modelin genel olarak doğru sınıflandırma oranını gösterir.
-Macro Average: F1 skoru 0.30. Bu, tüm sınıfların ortalama performansını temsil eder. Düşük değer, bazı sınıflarda düşük performansın etkisini yansıtır.
-Weighted Average: F1 skoru 0.75. Sınıf dağılımını dikkate alarak ağırlıklı bir ortalama performans sunar.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Karşılaştırma ve Sonuç:

K-Means Kümeleme;
-Artılar: Yüksek silhouette skoru (0.8) ve kümeler arasındaki iyi ayrım. 
          Kümeleme sonucu, kümelerin belirgin bir şekilde ayrıldığını ve veri noktalarının uygun kümelere atandığını gösterir.
-Eksiler: Küme merkezlerinin yakın olması, kümeler arasındaki ayrımın belirsiz olabileceğini gösterir.

Gözetimli Öğrenme;
-Artılar: Bazı sınıflarda yüksek F1 skorları (Class 0 ve Class 1), modelin bu sınıflarda iyi performans gösterdiğini gösterir. 
          Genel accuracy oranı ve weighted average F1 skoru da görece iyi performans sunar.
-Eksiler: Bazı sınıflarda düşük veya sıfır F1 skorları, modelin bu sınıflarda zayıf performans gösterdiğini gösterir.

Sonuç olarak, hangi yöntemlerin daha iyi performans gösterdiği, hangi metriklerin sizin için daha önemli olduğuna bağlıdır. 
K-Means yüksek silhouette skoru ile kümeler arasındaki ayrımın iyi olduğunu gösterirken, gözetimli öğrenme genel accuracy ve WA F1 skoru ile bazı sınıflarda iyi performans gösteriyor olabilir.
Bu bağlamda eğer amacımız veri kümemizdeki grupları veya kümeleri anlamaksa, K-Means kümeleme uygun bir yöntemdir.
Eğer belirli sınıfları tahmin etmek ve sınıflandırma yapmak istiyorsak, gözetimli öğrenme algoritmalarına odaklanmalıyız.
Sınıflar arasındaki performans farklarını iyileştirmek için veri ön işleme, özellik mühendisliği ve model iyileştirme çalışmalarına ihtiyaç duyabiliriz.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------KAGGLE NOTEBOOK VE DATASET LİNKİ---------------------------------------------------------------------------------------------------------------
Dataset: https://www.kaggle.com/datasets/jameslko/gun-violence-data?select=gun-violence-data_01-2013_03-2018.csv
Sup_Ml_Project: https://www.kaggle.com/code/eypkurt/sup-ml-project
NonSup_Ml_Project: https://www.kaggle.com/code/eypkurt/nonsup-ml-project


