<p align="center">
  <img src="assets/banner.svg" alt="Awesome Made in Georgia" width="100%"/>
</p>

<h1 align="center">Awesome Made in Georgia</h1>

<p align="center">
  <b>ქართველი დეველოპერების შექმნილი ღია კოდის კურირებული კოლექცია</b><br/>
  შერჩეული <a href="https://aipulsegeorgia.ge">AI Pulse Georgia</a>-ს მიერ
</p>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"/></a>
  <img src="https://img.shields.io/badge/repos-2-00D0FF?style=flat-square&labelColor=111827" alt="Repos"/>
  <img src="https://img.shields.io/badge/categories-6-A949DA?style=flat-square&labelColor=111827" alt="Categories"/>
  <img src="https://img.shields.io/badge/made_in-Sakartvelo_%F0%9F%87%AC%F0%9F%87%AA-00D0FF?style=flat-square&labelColor=111827" alt="Made in Sakartvelo"/>
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-welcome-A949DA?style=flat-square&labelColor=111827" alt="PRs welcome"/></a>
  <a href="https://aipulsegeorgia.ge"><img src="https://img.shields.io/badge/aipulsegeorgia.ge-website-A949DA?style=flat-square&labelColor=111827" alt="Website"/></a>
</p>

<p align="center"><i>A curated list of open source software built by Georgian developers — from Sakartvelo 🇬🇪, the country in the Caucasus (not the US state).</i></p>

---

## 🇬🇪 რა არის ეს სია

ქართველი დეველოპერები კარგ ღია კოდს წერენ, მაგრამ ეს კოდი GitHub-ის მილიონობით რეპოზიტორიაში იკარგება — არსად არსებობს ერთი ადგილი, სადაც ნახავ, რას აშენებენ საქართველოში. ეს სია ზუსტად ამას აკეთებს.

განსხვავებით უმეტესი awesome-სიისგან, ეს კოლექცია **თემატურად** კი არა, **წარმოშობით** არის აწყობილი. აქ არ არის მნიშვნელოვანი, რეპო AI-ზეა, ვებზე თუ თამაშზე — მნიშვნელოვანია, რომ მას ქართველმა შექმნა.

> **დაკავშირებული სია:** [Awesome AI Pulse Georgia](https://github.com/tornikebolokadze1-cyber/awesome-ai-pulse-georgia) — 300 საერთაშორისო AI და დეველოპერ ხელსაწყო, ქართული აღწერებით. ეს სია მისი დაა: იქ ვირჩევთ *საუკეთესოს მსოფლიოდან*, აქ ვაჩვენებთ *ჩვენსას*.

**რას ნიშნავს „ქართული"** — ზუსტი კრიტერიუმი და დამატების წესები: [CONTRIBUTING.md](CONTRIBUTING.md)

---

## შინაარსი

- [🤖 AI აგენტები და ორკესტრაცია](#-ai-აგენტები-და-ორკესტრაცია)
- [🛠️ დეველოპერ ხელსაწყოები](#️-დეველოპერ-ხელსაწყოები)
- [🔤 ქართული ენა და NLP](#-ქართული-ენა-და-nlp)
- [🌐 ვები და აპლიკაციები](#-ვები-და-აპლიკაციები)
- [📦 ბიბლიოთეკები და SDK](#-ბიბლიოთეკები-და-sdk)
- [🎮 თამაშები და გრაფიკა](#-თამაშები-და-გრაფიკა)

---

## 🤖 AI აგენტები და ორკესტრაცია

> **AI Agents & Orchestration** — სისტემები, რომლებიც AI მოდელებს ერთმანეთთან და შენს კოდთან ამუშავებენ: აგენტების მართვა, დავალებების განაწილება, კონტექსტის შენახვა და შედეგის შემოწმება.

| რეპოზიტორია | ⭐ | აღწერა |
|---|---|---|
| [kimi-atlas](https://github.com/null0xxx/kimi-atlas) | 13 | მრავალაგენტიანი ორკესტრატორი Kimi Code-ისთვის, 115 ჩაშენებული ოფიციალური skill-პაკეტით. მთავარი პრინციპი ისაა, რომ „გავიდა თუ ჩავარდა" გადაწყვეტილებას **არასოდეს იღებს LLM** — მას დეტერმინისტული (ყოველთვის ერთნაირად მომუშავე) 6-ლინზიანი შემოწმების ჰარნესი წყვეტს. ბირთვი `atlas` ერთ ცვლილებას ატარებს მკაფიო მდგომარეობათა მანქანაში `INIT → … → OUTPUT`, `ATLAS-WEAVE` კი დიდ ცვლილებას file-disjoint plan-DAG-ად შლის (ისე დაშლილი ამოცანები, რომ ორი აგენტი ერთსა და იმავე ფაილს არ ეხება) და ერთდროულად მაქსიმუმ 3 აგენტს უშვებს. აქვს ცოცხალი ContextGraph — გაშვების მდგომარეობის რუკა, რომელიც კოდერს ყოველ გადამოწმებაზე ხელახლა მიეწოდება — და forward-only rollback იზოლირებულ worktree-ში, ანუ შენს რეალურ ფაილებს არასოდეს ეხება. Python, MIT. |
| [AIWorkHub](https://github.com/shrec/AIWorkHub) | 2 | VS Code-ისთვის შექმნილი local-first control plane, რომელიც თითოეულ Git რეპოზიტორიას იზოლირებულ AI-სამუშაო სივრცედ აქცევს. აერთიანებს VS Code-ში უკვე ხელმისაწვდომ მოდელებს (Codex, Claude, DeepSeek, GLM, Copilot) რეპოზიტორიაზე მიბმულ დავალებების რიგთან, Source Graph-თან (კოდის სტრუქტურული რუკა), სესიების მენეჯერთან, AI-მეხსიერებასთან და review inbox-თან. არც ღრუბლოვანი ანგარიში სჭირდება და არც HTTP სერვისი — ყველაფერი ლოკალურად მუშაობს და არსებული CLI-ების ავტორიზაციას იყენებს, პაროლებს არსად აკოპირებს. ორი მთავარი იდეა: აგენტი კონტექსტს Source Graph-იდან იღებს და არა კოდის ხელახალი სკანირებით (ტოკენების დაზოგვა), ცვლილება კი მხოლოდ მაშინ მიიღება, როცა მტკიცებულება შემოწმებას გაივლის. Python + VS Code extension, MIT. |

---

## 🛠️ დეველოპერ ხელსაწყოები

> **Developer Tools** — CLI-ები, ავტომატიზაცია, build-ხელსაწყოები, DevOps და ყველაფერი, რაც დეველოპერს ყოველდღიურ სამუშაოს უადვილებს.

*ჯერ ცარიელია — შენი რეპო შეიძლება პირველი გახდეს. [დაამატე →](CONTRIBUTING.md)*

---

## 🔤 ქართული ენა და NLP

> **Georgian Language & NLP** — ქართული ენის ტექნოლოგიური ხელსაწყოები: NLP მოდელები, შრიფტები, კლავიატურები, transliteration, TTS/STT, spell-checker-ები და dataset-ები.

*ჯერ ცარიელია — შენი რეპო შეიძლება პირველი გახდეს. [დაამატე →](CONTRIBUTING.md)*

---

## 🌐 ვები და აპლიკაციები

> **Web & Applications** — ვებ-აპლიკაციები, საიტები, frontend და backend პროექტები, მობაილური აპები.

*ჯერ ცარიელია — შენი რეპო შეიძლება პირველი გახდეს. [დაამატე →](CONTRIBUTING.md)*

---

## 📦 ბიბლიოთეკები და SDK

> **Libraries & SDKs** — პაკეტები, რომლებსაც სხვა დეველოპერები საკუთარ პროექტებში იყენებენ: npm, PyPI, crates.io, Maven და სხვა.

*ჯერ ცარიელია — შენი რეპო შეიძლება პირველი გახდეს. [დაამატე →](CONTRIBUTING.md)*

---

## 🎮 თამაშები და გრაფიკა

> **Games & Graphics** — თამაშები, გრაფიკული ძრავები, კრეატიული კოდი და ვიზუალიზაცია.

*ჯერ ცარიელია — შენი რეპო შეიძლება პირველი გახდეს. [დაამატე →](CONTRIBUTING.md)*

---

## ჩვენს შესახებ

<p align="center">
  <a href="https://aipulsegeorgia.ge"><img src="https://img.shields.io/badge/AI_Pulse_Georgia-2026-00D0FF?style=for-the-badge&labelColor=111827" alt="AI Pulse Georgia 2026"/></a>
</p>

ეს სია იმართება **[AI Pulse Georgia](https://aipulsegeorgia.ge)**-ს მიერ — საზოგადოება, რომელიც ფოკუსირებულია AI აგენტებზე, ავტომატიზაციაზე და ავტონომიური სისტემების მომავალზე.

> *„Exploring Georgia's AI Future"*

თუ ქართულ ღია კოდს აშენებ ან უბრალოდ გინდა, რომ ის უფრო ხილული გახდეს — მიეცი ვარსკვლავი და გაუზიარე სხვებს.

## წვლილის შეტანა

იცნობ ქართველი დეველოპერის შექმნილ კარგ რეპოზიტორიას? ან შენი გაქვს? გახსენი issue ან გამოაგზავნე pull request — სრული წესები და „ქართულობის" კრიტერიუმი აქ არის: **[CONTRIBUTING.md](CONTRIBUTING.md)**

საკუთარი პროექტის დამატება წახალისებულია. ეს არ არის თავმოწონება — სია მხოლოდ მაშინ იმუშავებს, თუ ავტორები თავად შემოიტანენ თავიანთ სამუშაოს.

## ლიცენზია

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

სია გავრცელებულია [CC0 1.0 Universal](LICENSE) ლიცენზიით. ჩამოთვლილი რეპოზიტორიები საკუთარ ლიცენზიებს ინარჩუნებენ.
