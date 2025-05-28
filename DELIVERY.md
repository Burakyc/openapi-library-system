# OpenAPI Tasarımı Ödevi Teslim Raporu

## 👤 Öğrenci Bilgileri
- **Ad Soyad**: Burak Yüceler
- **Öğrenci Numarası**: 170422852

---

## 📂 OpenAPI YAML Dosyası

- **openapi.yaml** dosyasını projenizin GitHub reposuna yükleyiniz.
- Swagger Editor ile test ettiğinizden emin olunuz.

### 🔗 GitHub Repo Linki
https://github.com/Burakyc/openapi-library-system

---

## 📝 API Açıklaması

Bu API, üniversitenin çevrim içi kütüphane sistemi için tasarlanmıştır ve üç ana varlık üzerinden CRUD işlemleri sağlamaktadır:

Varlıklar (entities):

books: Kitap bilgilerini yönetir.
students: Öğrenci bilgilerini yönetir.
loans: Kitap ödünç alma ve iade işlemlerini yönetir.
CRUD İşlemleri:

GET /books, POST /books, PUT /books/{id}, DELETE /books/{id}, GET /books/{id} gibi endpoint’ler kitaplar için.
Benzer şekilde students ve loans endpoint’leri de aynı CRUD yapısına uygun şekilde tasarlanmıştır.
components/schemas: Tüm veri modelleri (Book, Student, Loan) bu bölümde detaylıca tanımlandı.

parameters: Path ve query parametreleri (id, page, size) burada tanımlı.

responses: Hata durumları (400, 404, 500) ve başarılı cevaplar burada açıklandı.

Sayfalama: GET /books endpoint’inde page ve size parametreleriyle uygulandı.

Ek Açıklamalar: API key tabanlı basit bir securitySchemes örneği de eklendi.

---

## 🧪 Test Notları (Opsiyonel)

Swagger Editor üzerinden test ettiğiniz örnek istek/yanıtları özetleyebilirsiniz:
- `GET /books` çağrısında ne döner?
[
  {
    "id": "b1a2c3d4-e5f6-7890-abcd-1234567890ab",
    "title": "Clean Code",
    "author": "Robert C. Martin",
    "isbn": "9780132350884",
    "publisher": "Prentice Hall",
    "pageCount": 464,
    "stock": 5
  }
]
- `POST /students` için örnek `requestBody` nedir?
{
  "id": "a1b2c3d4-e5f6-7890-abcd-1234567890cd",
  "name": "Jane Doe",
  "studentNumber": "2023012345",
  "email": "jane.doe@uni-library.edu.tr",
  "isActive": true
}
- Hatalı bir istek için dönen `400` örneği var mı?
{
  "message": "Invalid request parameters."
}
---


