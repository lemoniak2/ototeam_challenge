OTOTEAM Debugging Challenge
===========================

Instalacja
----------

```
git clone git@github.com:miksturait/ototeam_challenge.git
cd ototeam_challenge
cp config/database.yml.example config/database.yml
rake db:migrate
rake db:seed
rake db:migrate RAILS_ENV=test
guard
```

Zadania
-------

**1. Wszystkie translacje są popsute**

Np. przycisk dodawania nowego eventu wyświetla  `<span class="translation_missing" title="translation missing: dk.events.index.new_event">New Event</span>`

**2. Menu wyświetla się niepoprawnie**

Nierówno i niespójnie. Przycisk logout wyświetla się na różowo...

**3. Guard działa niepoprawnie**

Podczas zmian w testach (np. `event_spec.rb`) testy nie uruchamiają się automatycznie. Jeśli natomiast dokonamy zmian w pliku będącym testowanym (np. `event.rb`) to testy odpalają się normalnie.

**4. Podczas tworzenia eventu nie zapisuje się description**

Jak w temacie. Dodaj także test regresyjny (zwykły test, który pozwoli uniknąć tego błędu w przyszłości)

**5. Podczas wejścia na `http://localhost:3000/slides` wywala się błąd**

Jak w temacie

**6. Po utworzeniu grupy, wyświetlony komunikat to "translation missing"**

Pozostałe komunikaty dotyczące grup wydają się działać poprawnie

**7. Nie da się zapisać frienda podając jedynie email bądź numer telefonu**

Friend zapisuje się tylko wtedy, gdy podamy oba te pola, co powinno być opcjonalne. Dodaj także test regresyjny (zwykły test, który pozwoli uniknąć tego błędu w przyszłości)

**8. Wyszukiwanie eventów po nazwie nie działa**

Jak w temacie

**9. Da się utworzyć event z ujemną wartością dla maksymalnej liczby uczestników**

Jak w temacie. Dodaj także test regresyjny (zwykły test, który pozwoli uniknąć tego błędu w przyszłości)

**10. Po kliknięciu na OtoTeam lub wejściu na http://localhost:3000/ wyświetla się listing Friends zamiast Events**

Jak w temacie. Dodaj także test regresyjny (zwykły test, który pozwoli uniknąć tego błędu w przyszłości)

**11. Niezależnie jaki element menu kliknę, zawsze podświetlony jest element "Events"**

Jak w temacie
