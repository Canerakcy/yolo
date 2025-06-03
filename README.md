Ultralytics ile YOLO Modelleri Nasıl Eğitilir ve Dağıtılır (YOLO11, YOLOv8 ve YOLOv5)
Ultralytics YOLO modellerinin nasıl eğitileceğini ve dağıtılacağını gösteren eğitimler ve örnekler.

YOLO Modellerini Eğitin
Seçenek 1. Google Colab ile

YOLO modellerini eğitmek için bir Colab not defterine erişmek için aşağıya tıklayın. Özel bir YOLO modelini eğitmeyi, bir görüntü veri kümesini yüklemek ve birkaç kod bloğu çalıştırmak kadar kolay hale getirir.

Colab'da Aç

Seçenek 2. Yerel bir bilgisayarda

NVIDIA GPU ile donatılmış yerel bir bilgisayarda YOLO modellerini eğitme sürecini adım adım anlatan bir makale yazdım. Aşağıdaki bağlantıdan kontrol edebilirsiniz.

NVIDIA ile YOLO 11 Nesne Algılama Modelleri Yerel Olarak Nasıl Eğitilir

YOLO Modellerini Dağıtın
Betik yolo_detect.py, bir modelin nasıl yükleneceğini, bir görüntü kaynağında çıkarım nasıl çalıştırılacağını, çıkarım sonuçlarının nasıl ayrıştırılacağını ve görüntüdeki her algılanan sınıfın etrafında kutuların nasıl görüntüleneceğini gösteren temel bir örnek sağlar. Bu betik, Python'da YOLO modelleriyle nasıl çalışılacağını gösterir ve daha gelişmiş uygulamalar için bir başlangıç ​​noktası olarak kullanılabilir.

yolo_detect.pyBu depodan indirmek için şu komutu verin:

curl --output yolo_detect.py https://raw.githubusercontent.com/Canerakcy/yolo/refs/heads/main/yolo_detect.py

1280x720 çözünürlükte bir USB kamerada yolov8s modeliyle çıkarım yapmak için şunu çalıştırın:

python yolo_detect.py --model my_model.pt --source usb0 --resolution 1280x720
İşte yolo_detect.py için tüm argümanlar:

--model: Bir model dosyasının yolu (örneğin my_model.pt). Model bulunamazsa, varsayılan olarak . kullanılır yolov8s.pt.
--source: Çıkarımın çalıştırılacağı kaynak. Seçenekler şunlardır:
Resim dosyası (örnek: test.jpg)
Resim klasörü (örnek: my_images/test)
Video dosyası (örnek: testvid.mp4)
Bağlı bir USB kameranın dizini (örnek: usb0)
