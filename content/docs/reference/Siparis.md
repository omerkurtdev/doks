---
title: "Siparis"
description: "Mobius Workcube API"
summary: ""
date: 2023-09-07T16:13:18+02:00
lastmod: 2023-09-07T16:13:18+02:00
draft: false
weight: 910
toc: true
seo:
  title: "siparis" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### Sipariş Listesi

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis?password=<PASSWORD> \
        -d "siparis_no=12" \
        -d "firma_adi=<FIRMA_ADI>"
```

**Request**

**firma_adi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**siparis_no** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Sipariş Tarihi
* Sipariş No
* Firma
* Süreç
* Kdv Hariç Tutar
* Kdv Dahil Tutar
* Para Birimi
---

{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
    firma_adi: "<FIRMA_ISMI>",
    siparis_no: "1",
};

// API çağrısı
axios.post(url, data)
    .then(response => {
        console.log("Başarılı bir yanıt alındı:");
        console.log(response.data); // Yanıt verisi
    })
    .catch(error => {
        console.error("Hata oluştu:", error.response ? error.response.data : error.message);
    });

```

**Request**

**firma_adi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**siparis_no** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Sipariş Tarihi
* Sipariş No
* Firma
* Süreç
* Kdv Hariç Tutar
* Kdv Dahil Tutar
* Para Birimi

---

{{< /tab >}}

{{< /tabs >}}

### Sipariş Detay

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis_det?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis_det?password=<PASSWORD> \
        -d "siparis_id=1"
```

**Request body**

**siparis_id** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Sipariş Cari
* Sipariş No
* Sipariş Tarih
* Satır
    * Ürün
    * Miktar
    * Birim
    * Birim Fiyat
    * Toplam Fiyat
    * Para Birimi

---

{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis_det?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_siparis_det?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
    siparis_id: "1",
};

// API çağrısı
axios.post(url, data)
    .then(response => {
        console.log("Başarılı bir yanıt alındı:");
        console.log(response.data); // Yanıt verisi
    })
    .catch(error => {
        console.error("Hata oluştu:", error.response ? error.response.data : error.message);
    });

```

**Request body**

**siparis_id** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Sipariş Cari
* Sipariş No
* Sipariş Tarih
* Satır
    * Ürün
    * Miktar
    * Birim
    * Birim Fiyat
    * Toplam Fiyat
    * Para Birimi

---

{{< /tab >}}
{{< /tabs >}}

