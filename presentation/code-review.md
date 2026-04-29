Code review

Sources: 
1. Google book, google research
2. https://www.youtube.com/watch?v=UfzrF6Vwcy8 The PrimeTime
3. https://www.youtube.com/watch?v=ly86Wq_E18o Amazing Code Reviews: Creating a Superhero Collective • Alejandro Lujan • GOTO 2019
4. https://www.youtube.com/watch?v=d9_fweNDjKw Better Code Reviews in 6 SIMPLE STEPS Trisha Gee
5. https://google.github.io/eng-practices/review/



Plan wstępny:
# Plan Prezentacji: Code Review 2.0

**Grupa:** 10 osób, kameralny meetup lokalny
**Prelegent:** [Twoje Imię]

---

## 0. Tytuł (Pytanie angażujące)
> **"Code Review: Przykry obowiązek czy najlepszy moment na naukę?"**

---

## 1. Wstęp: Co nas boli? (The PrimeTime vibe)
* **Nitpicking:** Czepialstwo o styl, który powinien załatwić linter.
* **Ping-pong:** Nieskończona pętla poprawek ("Zrób tak", "Nie, jednak inaczej").
* **Ghosting:** Czekanie 3 dni na jeden komentarz.
* **Cel:** Zbudowanie wspólnego frontu – "wszyscy to znamy, zmieńmy to".

---

## 2. Kontrowersja: Mit szukania bugów
* **Teza:** Jeśli robisz CR tylko po to, by łapać bugi, to tracisz czas.
* **Dane:** Badania Google i Microsoft (Bacchelli & Bird) pokazują, że tylko ok. **15-20%** komentarzy dotyczy błędów logicznych.
* **Rzeczywisty cel:** * Transfer wiedzy (Knowledge Sharing).
    * Wiedza plemienna i strategiczna (Wskazówki od CTO/Produkcji).
    * Utrzymywalność (Maintainability) i czytelność.

---

## 3. Fundament: Psychologia i Standardy Google
* **Projekt Aristotle:** Najważniejszym czynnikiem efektywności jest **bezpieczeństwo psychologiczne**.
* **Zasada Google:** Reviewer ma dążyć do poprawy systemu (Continuous Improvement), a nie do narzucenia swojej subiektywnej perfekcji.
* **Szybkość:** Feedback powinien być szybki (najlepiej kilka godzin), by nie tracić kontekstu.

---

## 4. Warsztat: Automatyzacja i Proces
* **GitHub Reminders:** Ustawienie powiadomień na Slacku (koniec z wymówką "nie widziałem").
* **Round Robin:** Automatyczne przydzielanie review, by nie obciążać jednej osoby.
* **Draft PRs:** Pokazywanie pracy wcześnie (Alejandro Lujan), by uniknąć wyrzucania kodu do kosza po 3 dniach pracy.

---

## 5. Case Study 1: Eksperyment vs Ping-pong
* **Sytuacja:** Podejrzenie, że warunek w K8s nie zadziała.
* **Działanie:** Zamiast komentarza-pytania, krótki eksperyment (Go + LLM). 5 minut pracy zamiast 3 dni dyskusji.
* **Wniosek:** Reviewer jako partner-badacz. Przynieś wiedzę, a nie tylko wątpliwości.

---

## 6. Case Study 2: Marka Osobista (Personal Brand)
* **Dowód:** Screenshoty z ocen rocznych (koledzy doceniający jakość i sposób robienia review).
* **Przemiana:** "Nie zawsze tak było". Pokazanie, że bycie dobrym reviewerem to skill, który buduje szacunek w zespole.

---

## 7. Podsumowanie i Źródła
* **Google Engineering Practices:** [link](https://google.github.io/eng-practices/review/)
* **Project Aristotle:** [link](https://rework.withgoogle.com/print/guides/5721312602112000/)
* **Wideo:**
    * Trisha Gee - "Better Code Reviews"
    * Alejandro Lujan - "Superhero Collective"
    * The PrimeTime - "Stop Doing Code Reviews" (as we know them)
