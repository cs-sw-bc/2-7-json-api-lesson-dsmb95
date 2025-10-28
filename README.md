# JavaScript Foundations - Lesson 7: APIs & JSON

### Duration

2 hours 30 minutes

---

## 🎯 Learning Objectives

By the end of this class, learners will be able to:

* Understand the difference between **Objects** and **JSON**
* Recognize the role of **APIs** in providing dynamic data
* Identify **HTTP methods** and **status codes**
* Use **Postman** to test public APIs
* Parse and use **JSON data** in JavaScript

---

## 🧠 Section 1: What is JSON?

**Pencils Down:** Explain what JSON is.

> JSON (JavaScript Object Notation) is a text-based format for storing and exchanging data.

**Key Points:**

* Looks like JavaScript objects, but it’s just text.
* All keys and string values use **double quotes**.
* Data types: string, number, boolean, null, array, and object.

**Example:**

```json
{
  "name": "Whiskers",
  "age": 3,
  "isFriendly": true,
  "favoriteFoods": ["tuna", "salmon", "catnip"],
  "owner": { "firstName": "Alex", "lastName": "Ramos" }
}
```

**Pencils Up:** Parse it in JS using:

```js
const cat = JSON.parse(jsonData);
console.log(cat.name);
```

Discuss `JSON.parse()` and `JSON.stringify()`.

---

## 💡 Section 2: Objects vs JSON

**Analogy:**

> A JavaScript Object is your pet. JSON is its photo.

**Differences:**

| Feature            | JavaScript Object   | JSON                      |
| ------------------ | ------------------- | ------------------------- |
| Nature             | Live data structure | Text format               |
| Usage              | In code             | For sharing over internet |
| Keys               | No quotes           | Double quotes             |
| Supports Functions | ✅                   | 🚫                        |

**In-Class Demo:** `object_vs_json.html`

---

## 🌐 Section 3: Dynamic Data and the Client–Server Model

**Pencils Down:**
Explain how websites fetch live data.

> The browser (client) sends a **request** → server processes → sends **response** (usually JSON).

**Diagram:**

```
Browser → Request → API → Response → JSON → Browser updates UI
```

**Dynamic Data =** data that changes in real time (weather, quotes, cats, etc.).

---

## ⚙️ Section 4: HTTP Methods & Status Codes

| Method    | Purpose              | Example          |
| --------- | -------------------- | ---------------- |
| GET       | Retrieve data        | `GET /cat`       |
| POST      | Send new data        | `POST /users`    |
| PUT/PATCH | Update existing data | `PUT /user/1`    |
| DELETE    | Remove data          | `DELETE /post/1` |

| Status | Meaning         |
| ------ | --------------- |
| 200    | Success ✅       |
| 404    | Not Found 🚫    |
| 500    | Server Error 💥 |
| 403    | Forbidden 🔒    |

---

## 🧰 Section 5: Postman Hands-On

**Goal:** Use Postman to explore different API types.

### 🐱 1. Cat-as-a-Service (CATAAS)

**URL:** [https://cataas.com/cat?json=true](https://cataas.com/cat?json=true)
**Returns:** cat image data (JSON)

```json
{ "id": "abc123", "tags": ["cute", "sleepy"] }
```

* Teaches basic GET request.

---

### 💬 2. Quotable API

**URL:** [https://api.quotable.io/random](https://api.quotable.io/random)
**Returns:** random quote

```json
{ "content": "Be yourself; everyone else is already taken.", "author": "Oscar Wilde" }
```

* Teaches nested JSON and string data.

---

### 🌦️ 3. Weatherstack API

**URL:** [http://api.weatherstack.com/current?access_key=XvziLk12%&query=Toronto](http://api.weatherstack.com/current?access_key=XvziLk12%&query=Toronto)
**Returns:** current weather (requires API key)

```json
{
  "location": { "name": "Toronto", "country": "Canada" },
  "current": { "temperature": 14, "weather_descriptions": ["Cloudy"] }
}
```

* Teaches authentication and query parameters.

---

### 🔢 4. isEven API

**URL:** [https://isevenapi.xyz/api/iseven/10](https://isevenapi.xyz/api/iseven/10)
**Returns:**

```json
{ "iseven": true, "ad": "Thanks for using isEvenAPI!" }
```

* Teaches path parameters.

---

### 😈 5. Evil Insult API

**URL:** [https://evilinsult.com/generate_insult.php?lang=en&type=json](https://evilinsult.com/generate_insult.php?lang=en&type=json)
**Returns:**

```json
{ "insult": "You're as useless as the 'ueue' in 'queue'." }
```

* Teaches query parameters and humor in APIs.

---

## 🧩 Section 6: Practice Exercise

1. Choose one API from the list.
2. Use Postman to send a request.
3. Copy the JSON response.
4. Paste it into your code and access one property.

Example:

```js
let quote = {
  content: "Be yourself; everyone else is already taken.",
  author: "Oscar Wilde"
};

console.log(quote.content);
```

🪄 **Next Class Preview:** We'll automate all this using the **Fetch API**!

---

## 📘 Homework

* Explore at least 2 APIs and identify:

  * Uses path parameters
  * Uses query parameters
  * Requires authentication
  * Returns JSON or something else
* Bring one unique API to share next week!

---

## 🧾 Key Terms Cheat Sheet

* **API** – A way for two systems to talk.
* **Endpoint** – A URL where data is sent or received.
* **Response** – The data the server sends back.
* **Request** – What the client sends to the server.
* **JSON** – A text format to exchange data.
* **Authentication** – Proof you’re allowed to access the data.

---

## 💬 Instructor Tips

* Use the *Pencils Down / Pencils Up* rhythm.
* Start with jokes or cat pics to keep the mood light.
* Show live status code changes in Postman.
* Reinforce: JSON is text; Objects are real code.

---

## 🧱 Next Lesson Teaser

> Lesson 8 – Fetch API: Bringing live data from APIs into our JavaScript code!
