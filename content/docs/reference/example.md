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
### Authentication API

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.odul.com.tr/wex.cfm/mobiusmus/get_user`</span>

```bash
curl -X POST \
        https://erp.odul.com.tr/wex.cfm/mobiusmus/get_user \
        -d "username=test_user" \
        -d "password=12345" \
        -d "sifre=<MOBIUSTAN_TALEP_EDINIZ>"

```

**Request body**

**username** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:red;margin-left:4px;font-size:0.9em">Gerekli</span>

Mevcut kullanıcı adlarından biri girilmedilir.

---

**password** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:red;margin-left:4px;font-size:0.9em">Gerekli</span>

Girilen kullanıcı adına ait parola girilmelidir.

---

{{< /tab >}}
{{< tab "node" >}}

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.odul.com.tr/wex.cfm/mobiusmus/get_user";

// Gönderilecek veriler
const data = {
    username: "test_user",
    password: "12345"
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

{{< /tab >}}
{{< /tabs >}}



### Cari Listesi API

{{< tabs "create-new-site" >}}
{{< tab "cURL" >}}
<span style="color:gray">`POST`</span>
<span style="color:black">`https://erp.odul.com.tr/wex.cfm/mobiusmus/get_cari`</span>

```bash
curl -X POST \
        https://erp.odul.com.tr/wex.cfm/mobiusmus/get_cari \
        -d "firma_ismi=<FIRMA_ISMI>" \
        -d "password=<MOBIUSTAN_TALEP_EDINIZ>" \
        -d "sifre=<
```

**Request body**

**password** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:red;margin-left:4px;font-size:0.9em">Gerekli</span>

[Mobius](https://www.mobiusyazilim.com/)'tan edinilen parolayı girmelisiniz.

---

**firma_ismi** <span style="color:gray;margin-left:4px;font-size:0.9em">string</span> <span style="color:light-blue;margin-left:4px;font-size:0.9em">Opsiyonel</span>


---

{{< /tab >}}
{{< tab "node" >}}

```javascript
const axios = require('axios');

// API endpoint
const url = "https://erp.odul.com.tr/wex.cfm/mobiusmus/get_cari";

// Gönderilecek veriler
const data = {
    firma_ismi: "<FIRMA_ISMI>",
    password: "<MOBIUSTAN_TALEP_EDINIZ>"
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

{{< /tab >}}

{{< /tabs >}}
