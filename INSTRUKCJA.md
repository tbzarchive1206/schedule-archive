# Instrukcja edycji

## Miniatura wydarzenia

Wgraj obraz do folderu `assets/events/`, a następnie dodaj do wpisu:

```js
thumbnail: "assets/events/nazwa-pliku.jpg",
```

Można też użyć bezpośredniego adresu URL, ale lokalne pliki są stabilniejsze.

## Rozbudowany opis

Pole `content` przyjmuje dowolną liczbę bloków:

```js
content: [
  {
    type: "heading",
    text: { en: "Event information", ko: "행사 안내" }
  },
  {
    type: "text",
    text: {
      en: "Longer paragraph of information.",
      ko: "자세한 안내 문단입니다."
    }
  },
  {
    type: "image",
    src: "assets/events/details-photo.jpg",
    alt: "Description of the image",
    caption: {
      en: "Optional image caption.",
      ko: "선택 사항인 이미지 캡션."
    }
  }
]
```

Obsługiwane typy:

- `heading` — nagłówek,
- `text` — akapit,
- `image` — zdjęcie z opcjonalnym podpisem.

Bloki można mieszać i powtarzać. Starsze pole `description` nadal działa jako prosty opis, gdy `content` nie istnieje.
