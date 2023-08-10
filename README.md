# Dokumentacja REST API Obiekty

## Bazowy adres URL

htts://examplehotels.com

## Wyszukiwanie obiektów

### Endpoint: `/search`

#### Request

- **Metoda:** GET
- **URL:** `/search`
- **Query Parameters:**
  - `name` (opcjonalne): Wyszukaj obiekt po nazwie (autcomplete, po naciśnięciu enter wybór zatwierdza się)
  - `objectCode` (opcjonalne): Wyszukaj obiekt na podstawie kodu obiektu.
  - `objectType`(opcjonalne) : Wyszukaj obiekt na podstawie typu obiektu (wybór z listy).

#### Response

- **Status Code:** 200 OK
- **Format odpowiedzi:** JSON

```

   [
        {
            "objectId": 1,
            "name": "Hotel Przykładowy 1",
            "objectCode": "Kod1",
            "objectType": "Typ X"
        },
        {
            "objectId": 2,
            "name": "Hotel Przykładowy 2",
            "objectCode": "Kod2",
            "objectType": "Typ Y"
        }

    ]

```

## Tworzenie nowego obiektu

### Endpoint: `/create`

#### Request

- **Metoda:** POST
- **URL:** `/create`

#### Body parameters

- **name** - Zawiera nazwę hotelu - wymagane
- **objectType** - Zawiera typ hotelu - wymagane

#### Treść zapytania

```
        {
            "name": "Hotel Przykładowy 10",
            "objectType": "Typ X"
        },

```

#### Odpowiedź

- **Status Code:** 201 Created
- **Format odpowiedzi:** JSON

```
        {
            "objectId": 1,
            "name": "Hotel Przykładowy 10",
            "objectCode": "Kod1",
            "objectType": "Typ X"
        },

```
- **Status Code:** 201 Created
- **Format odpowiedzi:** JSON
