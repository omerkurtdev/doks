---
title: "Genel API"
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
### Authentication
{{< callout context="caution" title="Hatırlatma" icon="outline/alert-triangle" >}}
Lütfen parolanızı [Mobius](https://www.mobiusyazilim.com/)'tan istemeyi unutmayınız. Dokümanda \<PASSWORD\>  küçüktür ve büyüktür simgesi olmadan tanımlayız.
{{< /callout >}}

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_user?password=<PASSWORD>`</span>

```bash
curl -X POST \
        https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_user?password=<PASSWORD> \
        -d "user_name=test_user" \
        -d "user_password=<KULLANICI_PAROLASI>"

```

**Request body**

**user_name** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:red;margin-left:4px;font-size:0.9em">Gerekli</span>

Kullanıcı adı girilmedilir.

---

**user_password** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:red;margin-left:4px;font-size:0.9em">Gerekli</span>

Küçüktür ve büyüktür olmadan, kullanıcıya ait parola girilmelidir.

---


**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

---

{{< /tab >}}
{{< tab "node" >}}

<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_user?password=<PASSWORD>`</span>

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.DOMAIN-ADI/wex.cfm/mobiusmus/get_user?password=<PASSWORD>";

// Gönderilecek veriler
const data = {
    user_name: "test_user",
    user_password: "12345"
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

**user_name** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:red;margin-left:4px;font-size:0.9em">Gerekli</span>

Kullanıcı adı girilmedilir.

---

**user_password** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:red;margin-left:4px;font-size:0.9em">Gerekli</span>

Küçüktür ve büyüktür olmadan, kullanıcıya ait parola girilmelidir.

---


**Return Type** <span style="color:gray;margin-left:4px;font-size:0.9em">JSON

JSON olarak veri dönecektir.

---
{{< /tab >}}
{{< /tabs >}}



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


{{< /tab >}}

{{< /tabs >}}

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

{{< /tab >}}
{{< /tabs >}}


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

{{< /tab >}}
{{< /tabs >}}
