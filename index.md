<html>
  <head>
    <meta charset="utf-8" />
    <title>Home</title>
  </head>
  <body>
    {% for product in site.data.products %}
    <h2>
      <a href="{{ product.product_name | datapage_url: 'products' }}">
        {{ product.product_name }}
      </a>
    </h2>
    <p>{{ product.content | markdownify }}</p>
    {% endfor %}
  </body>
</html>
