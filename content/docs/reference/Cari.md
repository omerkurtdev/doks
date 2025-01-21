---
title: "Cari"
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

### Cari Listesi

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari?password=<PASSWORD> \
        -d "firma_ismi=<FIRMA_ISMI>"
```

**Request body**

**firma_ismi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em">Opsiyonel</span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Firma ID
* Firma Kategori (Text)
* Firma Adı
* Firma İl
* Firma İlçe
* Bakiye
---

{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
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

**firma_ismi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em">Opsiyonel</span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* Firma ID
* Firma Kategori (Text)
* Firma Adı
* Firma İl
* Firma İlçe
* Bakiye

---

{{< /tab >}}
{{< /tabs >}}

### Cari Extre

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari_extre?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari_extre?password=<PASSWORD> \
        -d "cari_id=1"
```

**Request body**

**cari_id** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* İşlem Tarihi
* Vade Tarihi
* İşlem Türü
* Borç  Tutarı
* Alacak Tutarı


---

{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari_extre?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_cari_extre?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
    cari_id: "1",
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

**cari_id** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

* İşlem Tarihi
* Vade Tarihi
* İşlem Türü
* Borç  Tutarı
* Alacak Tutarı


---

{{< /tab >}}
{{< /tabs >}}





### Yaşlandırma

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_yaslandirma?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_yaslandirma?password=<PASSWORD> \
        -d "firma_ismi=<FIRMA_ISMI>"
```

**Request body**

**firma_ismi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

---

{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_yaslandirma?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_yaslandirma?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
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

**firma_ismi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em"></span>


---

**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

---

{{< /tab >}}
{{< /tabs >}}

