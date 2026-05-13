---
layout: default
title: Energie sichtbar, steuerbar und wirtschaftlich
description: Ingenieurbüro Jörg Wünnenberg in Staufen im Breisgau — Energieberatung, Gebäudeautomation nach §71a GEG, Monitoring und Anlagentechnik aus einer Hand.
---

<section class="hero">
  <div class="container">
    <h1>Energie sichtbar, steuerbar und&nbsp;wirtschaftlich.</h1>
    <p class="hero-lede">{{ site.data.site.kernsatz }}</p>
    <div class="hero-actions">
      <a class="btn btn-primary" href="mailto:{{ site.data.site.email }}">E-Mail schreiben</a>
      <a class="btn btn-secondary" href="{{ site.data.site.booking_url }}" rel="noopener" target="_blank">30-Min-Gespräch buchen</a>
    </div>
  </div>
</section>

<section id="leistungen">
  <div class="container">
    <h2>Was ich für Sie tue</h2>
    <p class="section-lede">Messtechnik und Umsetzung aus einer Hand — vom ersten Messaufbau bis zur laufenden Optimierung im Betrieb.</p>
    <div class="cards">
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <path class="card-icon-bg" d="M3 17a9 9 0 0 1 18 0z"/>
          <path class="card-icon-fg" d="M3 17a9 9 0 0 1 18 0"/>
          <path class="card-icon-fg" d="M12 17l4.8-3.8"/>
          <circle class="card-icon-dot" cx="12" cy="17" r="1.5"/>
        </svg>
        <h3>Energiesystem-Analyse</h3>
        <p>Wissen, wo Energie verloren geht — und was eine Verbesserung wirklich bringt. Vollständige Abbildung von Erzeugung, Speicherung, Verteilung und Verbrauch mit Wirtschaftlichkeits- und CO₂-Bewertung.</p>
      </div>
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <rect class="card-icon-bg" x="3" y="5" width="18" height="14" rx="2"/>
          <rect class="card-icon-fg" x="3" y="5" width="18" height="14" rx="2"/>
          <path class="card-icon-fg" d="M6 15l3-3 3 2 5-6"/>
          <circle class="card-icon-dot" cx="17" cy="8" r="1.25"/>
        </svg>
        <h3>Monitoring &amp; Datenintegration</h3>
        <p>Sehen, was Ihre Anlage wirklich verbraucht — und wann. PV, BHKW, Wärmepumpe, Biomasse: Daten erfasst, visualisiert und als Entscheidungsgrundlage nutzbar gemacht.</p>
      </div>
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <path class="card-icon-bg" d="M3 21V7l7-3v3h11v14z"/>
          <path class="card-icon-fg" d="M3 21V7l7-3v3h11v14H3z"/>
          <path class="card-icon-dot" d="M14 9.5l-2.6 4.7h2.1l-1 3.6 3.1-5.1h-2.1z"/>
        </svg>
        <h3>Gebäudeautomation nach §71a GEG</h3>
        <p>Gesetzeskonform und wirtschaftlich nachrüsten — aus einer Hand. Komplettlösung von der Messtechnik bis zur Regelung. Die EU-EPBD-Novelle senkt die Schwelle perspektivisch auf 70 kW.</p>
      </div>
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <rect class="card-icon-bg" x="5" y="5" width="14" height="16" rx="2"/>
          <rect class="card-icon-fg" x="5" y="5" width="14" height="16" rx="2"/>
          <rect class="card-icon-fg" x="9" y="3" width="6" height="3.5" rx="1"/>
          <path class="card-icon-fg" d="M9 13.5l2 2 4-5"/>
        </svg>
        <h3>Quick-Check Energie</h3>
        <p>Vor-Ort-Messung und Statusaufnahme in 2–3 Tagen — zum Festpreis. Konkrete Handlungsempfehlungen, kein langes Vorlaufprojekt. Der unkomplizierte Einstieg.</p>
      </div>
    </div>
  </div>
</section>

<section id="branchen">
  <div class="container">
    <h2>Für Ihre Branche</h2>
    <p class="section-lede">Für Branchen mit wiederkehrenden Energiethemen gibt es eigene Profile — mit branchenspezifischem Vorgehen und passenden Referenzen.</p>
    <div class="branchen-buttons">
      {% for b in site.data.branchen %}
      <a class="btn btn-secondary btn-lg" href="{{ b.url }}">{{ b.name }} <span aria-hidden="true">→</span></a>
      {% endfor %}
    </div>
  </div>
</section>

<section id="ueber-mich">
  <div class="container">
    <div class="ueber-grid">
      <div>
        <h2>Wer optimiert</h2>
        <p>Mein Schwerpunkt liegt in der Praxis: Messtechnik und Datenerfassung vor Ort, SPS-Programmierung, Schaltschrankbau, Inbetriebnahme und Monitoring. Ich liefere Einsparungen, die sich im laufenden Betrieb tatsächlich messen lassen.</p>
        <p>Brauchen Sie ein normkonformes Energieaudit nach DIN EN 16247 oder einen BAFA-Förderantrag? Ich übernehme die Vor-Ort-Begehung und Messdatenaufnahme — Auswertung, Bericht und Antrag erstellt das <a href="https://www.ib-wuennenberg.de" rel="noopener" target="_blank">Ing.-Büro Wünnenberg</a>. Ein Kontakt, zwei Experten.</p>
        <p>Mein Name ist Jörg Wünnenberg — Dipl.-Ing. (FH) Elektrotechnik, begonnen als Mess- und Regelmechaniker in der chemischen Industrie. <strong>Seit 2003</strong> führe ich mein eigenes Ingenieurbüro in Staufen im Breisgau.</p>

        <h3>Anerkannt und gelistet</h3>
        <ul class="badges">
          {% for q in site.data.site.qualifikationen %}
          <li><a href="{{ q.url }}" rel="noopener" target="_blank">{{ q.name }}</a></li>
          {% endfor %}
        </ul>
      </div>
      <img
        src="/assets/portrait.jpg"
        alt="Jörg Wünnenberg vor einem Steuerungsschrank"
        class="ueber-portrait"
        width="300"
        height="400"
        loading="lazy"
      >
    </div>
  </div>
</section>

<section id="referenzen">
  <div class="container">
    <h2>Referenzen</h2>
    <p class="section-lede">Projekte seit 2003, quer durch Branchen und Größenklassen — von Gewerbe, Campingplätzen und Sparkassen bis zur Trainingsanlage in der Schweizer Wasser- und Ölwirtschaft.</p>
    <ul class="ref-list">
      {% for r in site.data.referenzen %}
      <li>
        <span class="ref-name">{{ r.name }}</span>
        <span class="ref-cat">{{ r.kategorie }}</span>
        <span class="ref-desc">{{ r.beschreibung }}</span>
      </li>
      {% endfor %}
    </ul>
  </div>
</section>

{% include cta.html %}
