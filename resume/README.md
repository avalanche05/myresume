# Резюме

`resume.tex` — исходник, `resume.pdf` — собранный файл (на него ссылается `index.html`).

## Сборка

```sh
cd resume
latexmk -pdf resume.tex
```

Или однократно:

```sh
pdflatex resume.tex
```

После пересборки закоммить обновлённый `resume.pdf`.
