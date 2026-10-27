Repozytorium pełni rolę mojego notatnika laboratoryjnego z nauki podstaw ewaluacji modeli językowych (LLM) oraz poznawania narzędzia **UK AISI `inspect_ai`**.

**Nota dotycząca kodu:** 
Szkielety skryptów w Pythonie zostały przygotowane przy wsparciu AI jako materiał szkoleniowy. 
Moja praca w ramach tego poligonu polegała na lokalnym skonfigurowaniu środowiska (Ollama), uruchamianiu poszczególnych scenariuszy, modyfikowaniu instrukcji systemowych (`system_message`) oraz analizie logów w celu zrozumienia, jak zmiany w prompcie wpływają na podatność modelu w praktyce. Starałem się też zrozumieć rolę poszczególnych bloków kodu i przepływ egzekucji testowanych skryptów.

## Cel ćwiczeń
Praktyczne sprawdzenie koncepcji opisanych w literaturze z zakresu AI Safety na lokalnym modelu językowym (m.in. Llama 3.1 8B) – przejście od teorii z publikacji do obserwacji rzeczywistego zachowania modelu w terminalu i `inspect view`.

## Przeanalizowana literatura
   * Perez & Ribeiro (2022) – *Ignore Previous Prompt*.
   * Greshake et al. (2023) – *Not What You've Signed Up For*
   * Wei et al. (2023) – *Jailbroken: How Does LLM Safety Training Fail?*
   * Röttger et al. (2023) – *XSTest*
   
Przykład uruchomienia testowej ewaluacji: 
```bash 
inspect eval 05_asr_vs_overrefusal_eval.py --model ollama/llama3.1:8b 
inspect view
