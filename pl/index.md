---
layout: default
lang: pl
---

{% assign forecasts = site.prognosis_pl | reverse %}

{% for forecast in forecasts limit: 1 %}

<section id="banner">
    <div class="content">
      <header>
        <h1>{{ forecast.title }} </h1>
        <p>najnowsza prognoza</p>
      </header>
      <p>{{ forecast.teaser }}</p>
      <ul class="actions">
        <li><a href="{{ forecast | absolute_url }}" class="button big">Więcej</a></li>
      </ul>
    </div>
    <span class="image object">
      <img src="{{ forecast.image_teaser }}" alt="" />
    </span>
  </section>

{% endfor %}

<!-- Section -->
<section>
	<header class="major">
		<h2>Nasza praca, to nie tylko prognozy:</h2>
	</header>
	<div class="features">
		<article>
			<span class="icon fa-diamond"></span>
			<div class="content">
				<h3><a href="/pl/recommendations.html">Aktualne rekomendacje</a></h3>
				<p>Nie wiesz jak minimalizować ryzyko? Jesteś premierem, ministrem, albo prezydentem miasta i nie wiesz co robić?
				</p>
			</div>
		</article>
		<article>
			<span class="icon fa-question"></span>
			<div class="content">
				<h3><a href="https://www.socjologia.uni.wroc.pl/Aktualnosci/Ankieta-Spoleczne-uwarunkowania-postaw-wobec-epidemii-koronawirusa">Ankieta badawcza</a></h3>
				<p>Razem z Instytutem Socjologii Uniwersytetu Wrocławskiego badamy Wasze zachowania, aby lepiej modelować przebieg pandemii. Jeśli chcesz pomóc - wypełnij ankietę!</p>
			</div>
		</article>
		<article>
			<span class="icon fa-calculator"></span>
			<div class="content">
				<h3><a href="/pl/risk.html">Ocena indywidualnego ryzyka COVID-19</a></h3>
				<p>Interesuje Cię oszacowanie indywidualnego prawdopodobieństwa warunkowego śmierci lub hospitalizacji? 
				Członkowie grupy MOCOS zbudowali model ryzyka na podstawie danych z pierwszej połowy roku.</p>
			</div>
		</article>
		<article>
			<span class="icon fa-line-chart"></span>
			<div class="content">
				<h3><a href="/pl/automatic.html">Automatyczna prognoza krótkoterminowa rozwoju pandemii</a></h3>
				<p>Model grupy MOCOS jest częścią German & Polish COVID-19 Forecast HUB. Znajdziesz tam prognozy rozwoju epidemii na najbliższe 2 tygodnie dla Polski. </p>
			</div>
		</article>
	</div>
</section>

<!-- Section -->
<section>
	<header class="major">
		<h2>Analizy</h2>
	</header>

{% assign analyses = site.analysis_pl | reverse %}
<div class="posts">
{% for analysis in analyses %}	
		<article>
			<a href="{{ analysis | absolute_url }}" class="image"><img src="{{ analysis.image_teaser }}" alt="" /></a>
			<h3>{{ analysis.title }}</h3>
			<p>{{ analysis.teaser }}</p>
			<ul class="actions">
				<li><a href="{{ analysis | absolute_url }}" class="button">Więcej</a></li>
			</ul>
		</article>
{% endfor %}
</div>

</section>