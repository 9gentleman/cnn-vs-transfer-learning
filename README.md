README - cnn-vs-transfer-learning
---------------------------------------------------------------

Proje Adı / Project Title:
---------------------------------
cnn-vs-transfer-learning

Açıklama / Description:
---------------------------------
Bu proje kapsamında, iç mekan (indoor) görüntü sınıflandırması problemi üzerinde derin öğrenme temelli farklı yaklaşımlar karşılaştırılmıştır. İlk olarak klasik CNN mimarisi ile model geliştirilmiş, ardından VGG16 tabanlı transfer öğrenme uygulanarak Head-Only ve Fine-Tune yöntemlerinin başarımı test edilmiştir.

This project focuses on comparing different deep learning approaches for indoor scene classification. A baseline CNN model was developed first, followed by transfer learning experiments using VGG16 architecture with Head-Only and Fine-Tuning strategies.

Dizin Yapısı / Directory Structure:
---------------------------------
├── README.txt               → Bu açıklama dosyası / This description file

├── video/                   → Demo videosu / Demo video

├── src/                     → Tüm kaynak kodlar / All source codes

├── Outputs						  → Çıktıları içeren pdf / Output  pdf

Gereksinimler / Requirements:
---------------------------------
- Python 3.11
- TensorFlow
- Scikit-learn
- Matplotlib
- Pandas
- PIL (Pillow)
- Jupyter Notebook

Kurulum Talimatları / Setup Instructions:
---------------------------------
1. Proje dosyalarını indirin ve çıkarın.
2. Dataset klasörünü masaüstüne şu isimle yerleştirin:

C:\Users<KullanıcıAdınız>\Desktop\data.set


3. Kod dosyaları içerisindeki yol tanımlarının sizin kullanıcı adınıza ve konumunuza göre güncel olduğundan emin olun:

base_dir = Path.home() / "Desktop" / "data.set" / "indoorCVPR_09" / "Images"

---------------------------------
1. Download and extract the project files.
2. Place the dataset folder on your Desktop with the following structure:

C:\Users\<YourUsername>\Desktop\data.set

3. Make sure the dataset path definitions inside the code are updated to match your username and folder structure. Example:

base_dir = Path.home() / "Desktop" / "data.set" / "indoorCVPR_09" / "Images"

Çalıştırma Adımları / Execution Steps:
---------------------------------
1. Dataset yüklenir ve bozuk veriler ayıklanır
2. Klasik CNN modeli eğitilir ve doğrulama sonuçları analiz edilir
3. Hiperparametre grid search yapılır
4. VGG16 Head-Only ve Fine-Tune modelleri eğitilir
5. Sonuç karşılaştırma tabloları ve görselleştirmeler oluşturulur
6. Test seti üzerinde Confusion Matrix ve Classification Report çıkarılır

1. Dataset loading and filtering
2. Baseline CNN model training and validation analysis
3. Hyperparameter grid search
4. VGG16 Head-Only and Fine-Tune training
5. Result comparison tables and visualizations
6. Confusion Matrix and Classification Report generation

Özet Bulgular / Summary of Results:
---------------------------------
Val Accuracy Sonuçları (Doğrulama Seti):
- Part 1 CNN: %99.53 doğruluk, %0.0747 kayıp
- VGG16 Head-Only: %72.10 doğruluk, %0.9388 kayıp
- VGG16 Fine-Tune: %82.74 doğruluk, %0.5687 kayıp

Test Set Sonuçları:
- Baseline CNN Model: %8 doğruluk, F1-Skor: 0.08
- VGG16 Fine-Tune Model: %62 doğruluk, F1-Skor: 0.61

Yorum:
Klasik CNN modeli overfitting etkisi göstererek validasyon setinde yüksek sonuçlar üretse de test setinde başarısız olmuştur. Transfer learning ile geliştirilen VGG16 Fine-Tune modeli ise gerçek dünya test setinde açık ara daha yüksek performans sağlamıştır. Bu nedenle final uygulamalar için VGG16 Fine-Tune modelinin tercih edilmesi önerilmektedir.

Interpretation:
Although the baseline CNN model achieved high validation scores, it severely overfitted and failed on the test set. In contrast, the VGG16 Fine-Tune model delivered significantly better results on the unseen test data, making it the recommended approach for real-world deployment.

Hazırlayan / Prepared by:
Can Kutlay


====================================================================

