---
title: "Authentication"
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

* status
* data

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

* status
* data
---
{{< /tab >}}
{{< /tabs >}}

