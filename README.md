# graphql-playground on Github Pages

- <https://helphi.github.io/pages-graphql-playground/> or
- <https://helphi.github.io/pages-graphql-playground/?https://YOUR-API.com/graphql>

## scripts

```sh
wget https://raw.githubusercontent.com/prisma/graphql-playground/master/packages/graphql-playground-html/withAnimation.html -O index.html
wget http://cdn.jsdelivr.net/npm/graphql-playground-react/build/static/css/index.css
wget http://cdn.jsdelivr.net/npm/graphql-playground-react/build/favicon.png
wget http://cdn.jsdelivr.net/npm/graphql-playground-react/build/static/js/middleware.js
sed -i "s#//cdn.jsdelivr.net/npm/graphql-playground-react/build/static/css/index.css#index.css#g" index.html
sed -i "s#//cdn.jsdelivr.net/npm/graphql-playground-react/build/favicon.png#favicon.png#g" index.html
sed -i "s#//cdn.jsdelivr.net/npm/graphql-playground-react/build/static/js/middleware.js#middleware.js#g" index.html
sed -i 's#// you can add more options here#endpoint: window.location.search.substring(1) ? window.location.search.substring(1) : "https://api.github.com/graphql"#g' index.html
```