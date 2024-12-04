# Wiki.js Docker Compose Kurulumu

Bu repo, **Wiki.js** adlı modern ve esnek bir açık kaynaklı wiki platformunu, **PostgreSQL** veritabanı ile birlikte Docker Compose kullanarak kolayca kurmanızı sağlar.

## Özellikler

- **Wiki.js**: Bilgi paylaşımı ve dokümantasyon için güçlü bir çözüm.
- **PostgreSQL**: Hafif ve güvenilir bir veritabanı.
- **Kalıcı Veri**: Veritabanı ve Wiki.js verileri için volume desteği.
- **Kolay Kurulum**: Tek bir `docker-compose.yml` dosyası ile hızlı kurulum.
- **Ağ İzolasyonu**: Özel `wiki-network` ağı ile servislerin iletişimi güvence altına alınır.

## Kurulum

### 1. Depoyu Klonlayın

```bash
git clone <repository-url>
cd <repository-directory>
```

### 2. Ortam Değişkenlerini Düzenleyin

`docker-compose.yml` dosyasındaki aşağıdaki değişkenleri kendi ihtiyaçlarınıza göre düzenleyin:

- `CHANGE_DB_NAME`: Veritabanı adı
- `CHANGE_DB_USER`: Veritabanı kullanıcı adı
- `CHANGE_DB_PASSWORD`: Veritabanı şifresi

Opsiyonel olarak bir `.env` dosyası oluşturabilirsiniz.

### 3. Servisleri Başlatın

Aşağıdaki komut ile Docker Compose'u başlatın:

```bash
docker-compose up -d
```

### 4. Tarayıcıdan Erişim

Wiki.js arayüzüne [http://localhost](http://localhost) adresinden erişebilirsiniz.

## Dosya Yapısı

- `db-data`: PostgreSQL veritabanı verileri
- `wiki-data`: Wiki.js uygulama verileri
- `backup`: Wiki.js yedekleme dizini

## Hızlı Notlar

- Servisler yeniden başlatıldığında veriler kaybolmaz.
- Varsayılan olarak 80 portu kullanılır; gerekirse `docker-compose.yml` dosyasında değiştirebilirsiniz.
- Daha fazla bilgi için [Wiki.js Belgeleri](https://docs.requarks.io/) adresini ziyaret edin.
