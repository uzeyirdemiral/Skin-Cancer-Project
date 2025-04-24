# Skin Cancer Project

## Proje Açıklaması
Bu proje, cilt kanseri teşhisi koymaya yönelik bir model eğitmek için **HAM10000** veri setini kullanmaktadır. Model, veri setindeki cilt kanseri fotoğraflarını sınıflandırmak için derin öğrenme tekniklerini kullanmaktadır. 

## Kullanılan Teknolojiler
- **Python** (TensorFlow, PyTorch)
- **Kaggle API** (Veri setini yüklemek için)
- **Google Colab** (Model eğitimi için)

## Veri Seti

Bu projede **HAM10000** veri seti kullanılmaktadır. Bu veri setini [Kaggle'dan](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000) indirip projeye dahil edebilirsiniz.

### Kaggle Veri Setine Nasıl Erişilir?

1. **Kaggle Hesabı Oluşturun**: Eğer Kaggle hesabınız yoksa, [Kaggle'a](https://www.kaggle.com/) kaydolun.
2. **Kaggle API Anahtarını Alın**: Kaggle API ile veri setini programlı bir şekilde indirmek için şu adımları izleyin:
    - Kaggle hesabınıza giriş yapın.
    - [Kaggle API Anahtarını Alın](https://www.kaggle.com/docs/api) ve JSON formatındaki anahtar dosyasını bilgisayarınıza indirin.
    - Bu dosyayı, `~/.kaggle/kaggle.json` yolu altında saklayın (Google Colab’da `drive/MyDrive/.kaggle/kaggle.json` yolu kullanabilirsiniz).

3. **Veri Setini İndirin**:
    Kaggle API'yi kullanarak veri setini indirmeniz için aşağıdaki komutları kullanabilirsiniz.

    ```bash
    !pip install kaggle  # Kaggle API'yi yükleyin
    !mkdir -p ~/.kaggle  # Kaggle klasörünü oluşturun
    !cp /path/to/kaggle.json ~/.kaggle/  # Kaggle API anahtarınızı doğru dizine kopyalayın
    !chmod 600 ~/.kaggle/kaggle.json  # Anahtar dosyasının izinlerini ayarlayın

    # Veri setini indirin
    !kaggle datasets download -d kmader/skin-cancer-mnist-ham10000
    !unzip skin-cancer-mnist-ham10000.zip -d ./data  # Zip dosyasını çıkarın
    ```

## Modelin Eğitilmesi

Aşağıdaki adımları izleyerek modelinizi eğitebilirsiniz:

### 1. Gerekli Kütüphaneleri Yükleyin

Gerekli Python kütüphanelerini yüklemek için şu komutu çalıştırın:

```bash
pip install timm scikit-learn matplotlib
````

### 2. Modeli Eğitmeye Başlayın 

Eğitim sürecini başlatmak için **skin_cancer.ipynb** dosyasındaki hücreleri sırayla çalıştırın.


