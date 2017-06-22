# Slide PDF Beamer

Buatlah *slide* PDF Beamer sesuai dengan contoh *file* `tugas.pdf` berikut.
Ganti nama penulis dengan nama anda dan silahkan pakai [tema](http://deic.uab.es/~iblanes/beamer_gallery/index_by_theme.html) apapun.
Gunakan *file* `[ref.bib](../ref/ref.bib)`, `[ipb.csl](../ref/ipb.csl)`, dan gambar yang disediakan berikut.
Kumpulkan dalam satu *file* PDF dengan nama `[NIM].pdf`.

### Kompilasi

```bash
pandoc input.md -o output.pdf -t beamer -F pandoc-citeproc
```

### Gambar

![Arduino Nano](nano.jpg)

![Raspberry Pi](raspi.jpg)
