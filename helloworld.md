## helloworld
<title>
 {{ page.title }}
</title>

<main>
  <section>
    <header>
      <h2>投稿一覧</h2>
    </header>

    {% for post in site.posts %}
      <aside>
        <a href="{{ post.url }}"><h3>{{ post.title }}</h3></a>
        <p>{% if post.desc %}{{ post.desc }}{% else %}{{ post.content | strip_html | truncate: 130 }}{% endif %}</p>
      </aside>  
    {% endfor %}
  </section>
</main>
