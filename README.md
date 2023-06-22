# CeneoScrapper

## Selektory CSS składowych opinii w serwisie [Ceneo.pl](https://www.ceneo.pl/)

| składowa                               | nazwa                  | selektor                                                            |
| -------------------------------------- | ---------------------- | ------------------------------------------------------------------- |
| opinia                                 | opinion/single_opinion | div.js_product-review                                               |
| identyfikator opinii                   | opinion_id             | [data-entry-id]                                                     |
| autor                                  | author                 | span.user-post\_\_author-name                                       |
| rekomendacja                           | recommendation         | span.user-post\_\_author-recomendation \> em                        |
| liczba gwiazdek                        | stars                  | span.user-post\_\_score-countspan.score-marker[style]               |
| czy opinia jest potwierdzona zakupem   | purchased              | div.review-pz                                                       |
| data wystawienia opinii                | opinion_date           | span.user-post\_\_published \> time:nth_child(1)[datetime]          |
| data zakupu produktu                   | purchase_date          | span.user-post\_\_published \> time:nth_child(2)[datetime]          |
| ile osób uznało opinię za przydatną    | usefull_count          | button.vote-yes[data-total-vote]button.vote-yes \> span             |
| ile osób uznało opinię za nieprzydatną | unusefull_count        | button.vote-no[data-total-vote]button.vote-no \> span               |
| treść opinii                           | content                | div.user-post\_\_text                                               |
| listę zalet                            | pros                   | div.review-feature\_\_title--positives ~ div.review-feature\_\_item |
| listę wad                              | cons                   | div.review-feature\_\_title--negatives ~ div.review-feature\_\_item |

## Wykorzystane biblioteki Python'a

- Requests
- BeautifulSoup4
