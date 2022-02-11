# projekt-notatki

Projekt został zrealizowany przez Magdalenę Staniec oraz Szymona Pusza z grupy N32-31.  Głównym celem aplikacji, jest zbiór notatek, które jesteśmy w stanie dodawać, usuwać oraz edytować.
Na stronie głównej widnieje lista z notatkami, wraz z opcjami ich edycji oraz usunięcia. Jest również opcja dodania nowej notatki. Szczegóły danej notatki są wyświetlane po kliknięciu na nią.
Przy dodawaniu nowej notatki pojawia nam się okienko z tytułem notatki oraz szczegółami. Została zastosowana walidacja zarówno po stronie front-endu oraz back-endu, w celu uniknięcia sytuacji w których np. na liście notatek będzie widniała notatka, która zniknie po odświeżeniu strony oraz nie zapisze się z bazie danych MongoDB. Po dodaniu notatki, okienko ze szczegółami notatek zniknie nam automatycznie.
W przypadku edycji notatki, wyświetli nam się okienko z edycją notatki, jednak w inputach widnieć będą aktualne dane, które możemy usunąć/nadpisać.
Aplikacja po stronie back-endu wykorzystuje Node.js, wzbogacony o modale i parę przydatnych bibliotek, utworzone API oraz MongoDB, oraz responsywny front-end zbudowany za pomocą komponentów w React.js.

# Frontend
Zbudowany z komponentów znajdujących się w folderze projekt-notatki/frontend/src/components/Notes
Odpowiednio:
EditNote – komponent odpowiadający za edycję danej notatki
NewNote – odpowiada za utworzenie nowej notatki
Note ¬– zawiera informacje o danej notatce
Notes – akcje związane z notatkami
Zainstalowana została biblioteka react-modal, modal został umieszczony w stanie (notes.js)
Wszystkie moduły są niezależne od siebie
Szczegóły notatki wyświetlają się po jej kliknięciu, dzięki zaimplementowanej funkcji UseState (w pliku note.js)
Również przy jej wykorzystaniu, edytując notatkę, aktualne informacje są widoczne.
Biblioteka axios do wykonywania requestów w celu połączenia z backendem
Po dodaniu notatki, formularz się ukrywa, aby mógł zostać ponownie wywołany poprzez kliknięcie przycisku Nowa notatka.
Wtyczka react-notifications informująca nas o błędach, zwracająca info o statusach



# Backend
Zbudowany na node.js, z expressem w celu utworzenia API,
Projekt wykorzystuje bazę danych MongoDB. Połączenie znajduje się w folderze backend/app/db.
Zawarte zostały endpointy ze statusami, takimi jak:
-do pobierania notatki
-do zapisywania notatki
-do edytowania notatki
-do usunięcia notatki
Znajdują się one w folderze /backend/app/actions/api/noteActions.js
