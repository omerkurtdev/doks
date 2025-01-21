---
title: "Fatura"
description: "Mobius Workcube API"
summary: ""
date: 2023-09-07T16:13:18+02:00
lastmod: 2023-09-07T16:13:18+02:00
draft: false
weight: 910
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### Fatura Listesi

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_fatura?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_fatura?password=<PASSWORD> \
        -d "fatura_no=1" \
        -d "firma_ismi=<FIRMA_ISMI>"
```

**Request body**

**fatura_no** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**firma_ismi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Fatura ID
* Fatura No
* Cari
* Fatura Tarihi
* Kdv Hariç Tutar
* Kdv Dahil Tutar
* Toplam Tutar

---

{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_fatura?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_yaslandirma?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
    fatura_no: "1",
    firma_ismi: "<FIRMA_ISMI>",

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

**fatura_no** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**firma_ismi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Fatura ID
* Fatura No
* Cari
* Fatura Tarihi
* Kdv Hariç Tutar
* Kdv Dahil Tutar
* Toplam Tutar

---

{{< /tab >}}
{{< /tabs >}}


### Fatura Detay

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_fatura_det?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_fatura_det?password=<PASSWORD> \
        -d "fatura_id=1"
```

**Request body**

**fatura_id** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Fatura No
* Fatura Tarihi
* Cari
* Ürün
    * Ürün Adı
    * Miktar
    * Birim
    * Birim Fiyat
    * Satır Toplam Fiyat KDV H.
    * Satır Toplam Fiyat Kdv Dahil
    * Para Birimi


---


{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_fatura_det?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_yaslandirma?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
    fatura_id: "1",

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

**fatura_id** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>

---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Fatura No
* Fatura Tarihi
* Cari
* Ürün
    * Ürün Adı
    * Miktar
    * Birim
    * Birim Fiyat
    * Satır Toplam Fiyat KDV H.
    * Satır Toplam Fiyat Kdv Dahil
    * Para Birimi


---

{{< /tab >}}
{{< /tabs >}}
