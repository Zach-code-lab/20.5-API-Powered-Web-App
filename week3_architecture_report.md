# Module 21 — Architecture Report

## 1. MVC Table (Lesson 21.1)

| MVC Part | In My Project |
|----------|----------------|
| **Model** | The API JSON data I fetch (example: Pokémon data). This is the data layer my app depends on. |
| **View** | My HTML and CSS files. They control layout, styling, and what the user sees on the screen. |
| **Controller** | My JavaScript (script.js). It handles fetch calls, event listeners, and updates the DOM. |

---

## 2. Design Pattern Examples (Lesson 21.2)

### **Data → Logic → UI Pattern**
- **Data:** Fetching JSON from an API.  
- **Logic:** Extracting values like `name`, `height`, or image URLs.  
- **UI:** Inserting those values into the `<div id="output">` element.

### **Example From My Code**
- Data: `fetch("https://pokeapi.co/api/v2/pokemon/squirtle")`
- Logic: `data.name`, `data.height`, `data.weight`
- UI: `document.getElementById("output").innerHTML = ...`

This pattern keeps my code clean and prevents mixing data processing with HTML.

---

## 3. Refactored Code Summary (Lesson 21.2)

Before refactoring, my code mixed DOM updates and fetch logic in one long block.  
After refactoring, I separated responsibilities:

- A function that fetches data  
- A function that formats the data  
- A function that updates the UI  

This made the code easier to read, easier to debug, and easier to expand later.

---

## 4. Runtime Environments Comparison Table (Lesson 21.3)

| Platform | Language(s) | Runtime Environment | Example Apps |
|----------|--------------|----------------------|----------------|
| **iOS** | Swift / SwiftUI | iOS Runtime | Messages, Safari |
| **Android** | Kotlin / Java | ART (Android Runtime) | YouTube, Instagram |
| **Web** | JavaScript / HTML / CSS | Browser Engine (V8, WebKit, Gecko) | My Module 20 App |
| **Desktop** | Varies (C#, Swift, C++, JS via Electron) | OS‑specific runtimes (.NET, Cocoa, Linux frameworks) | Photoshop, VS Code |

---

## 5. Hosting Comparison Table (Lesson 21.4)

| Hosting Type | Description | Cost Level | Best For |
|--------------|-------------|------------|----------|
| **Shared Hosting** | Many sites share one server. | Low | Small personal sites, beginners. |
| **VPS Hosting** | Virtual private server with isolated resources. | Medium | Growing apps needing more control. |
| **Dedicated Hosting** | One physical server for one customer. | High | High‑traffic apps, full customization. |
| **Static Hosting (GitHub Pages)** | Serves HTML/CSS/JS with no backend. | Free | Portfolios, class projects, static apps. |
| **Cloud Hosting (AWS/Azure)** | Scalable, on‑demand hosting. | Varies | Apps needing databases, APIs, auth, scaling. |

---

## 6. One‑Page Summary: What I Learned About Architecture

Throughout this module, I learned how different parts of a web application fit together to form a clean architecture. MVC helped me understand how to separate the data layer, the logic layer, and the user interface so my code stays organized and easier to maintain. Design patterns like “Data → Logic → UI” showed me how to structure my JavaScript so it’s readable and predictable. I also learned how runtime environments affect where and how code executes — browsers run JavaScript, mobile apps run on iOS or Android runtimes, and desktop apps rely on OS‑specific frameworks. Hosting matters too, because different types of apps need different levels of power, scaling, and backend support. Overall, this module helped me see how real applications are structured and what choices developers make behind the scenes.

