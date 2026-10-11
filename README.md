# cards-vitrine

Pagina publica de cartas a venda. **Este repositorio e PUBLICO e so pode conter:**

```
index.html        a vitrine
.nojekyll         o GitHub Pages serve os arquivos como estao
fotos/V*_f.jpg    frente da carta, 640px
fotos/V*_v.jpg    verso da carta, 640px
README.md         este arquivo
```

Qualquer outro arquivo faz a publicacao **parar antes do push** - a conferencia e por lista
branca, no `conferir_publicaveis()` do `scripts/24_vitrine_html.py`.

O que **nunca** entra aqui: `.env`, `Inventory/`, `Checklists/`, `Raw/`, `Scans/`, banco,
CSV, valor em dolar, valor do acervo, `card_id`. As fotos sao nomeadas pelo CODIGO da carta
(`V01`), nao pelo `card_id`, para que nem o nome do arquivo conte de onde a foto veio.

## Como publicar

No repositorio do pipeline (privado):

```
python scripts/24_vitrine_html.py --site --publicar
```

O comando regenera a pagina, copia para ca, confere a lista branca, commita e empurra.

## Identidade dos commits

`user.email` esta como `vitrine@localhost` de proposito: sem isso o git usaria o nome da
maquina (`filomeno@MacBook-Pro-AF.local`), que ficaria visivel em repositorio publico.
Troque por outro endereco se quiser.
