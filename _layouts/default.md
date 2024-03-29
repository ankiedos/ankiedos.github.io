<!DOCTYPE html>
<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    <meta charset='utf-8'>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="{{ '/assets/css/style.css?v=' | append: site.github.build_revision | relative_url }}">
    <link rel="stylesheet" href="{{ 'assets/css/styles.css' | relative_url }}">
	  <script language="javascript" type="text/js" href="{{ '/assets/js/script.js' | relative_url }}"></script>
    <link rel="sitemap" type="application/xml" title="Sitemap" href="{{ site.url }}/sitemap.xml" />
    {% feed_meta %}
    {% seo %}
  </head>

  <body>
    <header>
      <div class="container">
        <a id="a-title" href="{{ '/' | relative_url }}">
          <h1>{{ site.title | default: site.github.repository_name }}</h1>
        </a>
        <h2>{{ site.description | default: site.github.project_tagline }}</h2>
        <section id="downloads">
          {%- if site.show_downloads -%}
            <a href="{{ site.github.zip_url }}" class="btn">Download as .zip</a>
            <a href="{{ site.github.tar_url }}" class="btn">Download as .tar.gz</a>
          {%- endif -%}
          <a href="{{ site.github.repository_url }}" class="btn btn-github"><span class="icon"></span>View on GitHub</a>
        </section>
      </div>
    </header>
    <div class="container">
      <section id="main_content">
            {{ content }}
            <hr>
            {%- include navigation.md -%}
            <footer>
                <h6><small>Możesz zasubskrybować przez RSS: <a href="/feed.xml">feed.xml</a></small></h6>
	        <h6>Widzisz literówkę? Popraw i zgłoś: <a href="https://github.com/ankiedos/ankiedos.github.io">https://github.com/ankiedos/ankiedos.github.io</a></h6>
                <h6><small>Autorem jest Antoni Kiedos | 2021 - {{ "now" | date: "%Y" }}</small></h6>
                <h6><small>Autorem szablonu hacker jest <a href="https://github.com/pages-themes">pages-themes</a></small></h6>
                <h6><img src="https://static.fsf.org/nosvn/associate/crm/5608797.png" alt="FSF Associate member since December 2022"></h6>
            </footer>
      </section>
    </div>
{%- if site.google_analytics -%}
    <script>
      (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
      (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
      m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
      })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
      ga('create', '{{ site.google_analytics }}', 'auto');
      ga('send', 'pageview');
    </script>
{%- endif -%}
  </body>
</html>