# OSDISoL

Pagina web a proiectului **OSDISoL** – *Infrastructură de date spațiale Open Source destinată cartografiei solului și administrării teritoriului* (Open Source Spatial Data Infrastructure for Soil Mapping and Land Management).

- **Cod proiect:** PN-III-P2-2.1-PED-2019-5436
- **Domeniul:** 3.2 – Mediu și schimbări climatice
- **Durata:** 2020–2022
- **Director de proiect:** dr. Bogdan Roșca
- **Instituție:** Academia Română, Filiala Iași – Centrul de Cercetări Geografice

## Structura site-ului

Site-ul este generat cu [Jekyll](https://jekyllrb.com/), folosind tema
[Petridish](https://github.com/peterdesmet/petridish) (Peter Desmet, MIT).

| Ce vrei să modifici | Fișier |
| :--- | :--- |
| Titlu, culori, logo, adresă | `_config.yml` |
| Meniul de sus | `_data/navigation.yml` |
| Subsolul paginii | `_data/footer.yml` |
| Membrii echipei | `_data/team.yml` |
| Paginile site-ului | `pages/*.md` |
| Noutăți / anunțuri | `_posts/AAAA-LL-ZZ-titlu.md` |
| Imagini | `assets/img/` |

## Rulare locală

```bash
bundle install
bundle exec jekyll serve
```

## Licență

Conținutul este publicat sub licența [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/).
Tema Petridish este publicată sub licența MIT (vezi `LICENSE`).
