---
layout: default
title: Energy sichtbar, steuerbar und wirtschaftlich
description: Ingenieurbüro Jörg Wünnenberg in Staufen im Breisgau — Energieberatung, Gebäudeautomation nach §71a GEG, Monitoring und Anlagentechnik aus einer Hand.
---

<section class="hero">
  <div class="container">
    <h1>Energie sichtbar, steuerbar und&nbsp;wirtschaftlich.</h1>
    <p class="hero-lede">{{ site.data.site.kernsatz }}</p>
    <div class="hero-actions">
      <a class="btn btn-primary" href="mailto:{{ site.data.site.email }}">E-Mail schreiben</a>
      <a class="btn btn-secondary" href="{{ site.data.site.cal_url }}" rel="noopener" target="_blank">30-Min-Gespräch buchen</a>
    </div>
  </div>
</section>

<section id="leistungen">
  <div class="container">
    <h2>Was ich für Sie tue</h2>
    <p class="section-lede">Beratung und Umsetzung aus einer Hand — vom ersten Messaufbau bis zur laufenden Optimierung im Betrieb.</p>
    <div class="cards">
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <path class="card-icon-bg" d="M3 17a9 9 0 0 1 18 0z"/>
          <path class="card-icon-fg" d="M3 17a9 9 0 0 1 18 0"/>
          <path class="card-icon-fg" d="M12 17l4.8-3.8"/>
          <circle class="card-icon-dot" cx="12" cy="17" r="1.5"/>
        </svg>
        <h3>Energiesystem-Analyse</h3>
        <p>Vollständige Abbildung Ihrer Energieversorgung: Erzeugung, Speicherung, Verteilung, Verbrauch — mit Wirtschaftlichkeits- und CO₂-Bewertung.</p>
      </div>
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <rect class="card-icon-bg" x="3" y="5" width="18" height="14" rx="2"/>
          <rect class="card-icon-fg" x="3" y="5" width="18" height="14" rx="2"/>
          <path class="card-icon-fg" d="M6 15l3-3 3 2 5-6"/>
          <circle class="card-icon-dot" cx="17" cy="8" r="1.25"/>
        </svg>
        <h3>Monitoring &amp; Datenintegration</h3>
        <p>Verbrauchs- und Erzeugungsdaten aus PV, BHKW, Wärmepumpe oder Biomasse werden erfasst, visualisiert und für Entscheidungen nutzbar gemacht.</p>
      </div>
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <path class="card-icon-bg" d="M3 21V7l7-3v3h11v14z"/>
          <path class="card-icon-fg" d="M3 21V7l7-3v3h11v14H3z"/>
          <path class="card-icon-dot" d="M14 9.5l-2.6 4.7h2.1l-1 3.6 3.1-5.1h-2.1z"/>
        </svg>
        <h3>Gebäudeautomation nach §71a GEG</h3>
        <p>Komplettlösung für die Nachrüstpflicht großer Nichtwohngebäude — von der Messtechnik bis zur Regelung. EU-Novelle senkt die Schwelle perspektivisch auf 70 kW.</p>
      </div>
      <div class="card">
        <svg class="card-icon" viewBox="0 0 24 24" aria-hidden="true" focusable="false">
          <rect class="card-icon-bg" x="5" y="5" width="14" height="16" rx="2"/>
          <rect class="card-icon-fg" x="5" y="5" width="14" height="16" rx="2"/>
          <rect class="card-icon-fg" x="9" y="3" width="6" height="3.5" rx="1"/>
          <path class="card-icon-fg" d="M9 13.5l2 2 4-5"/>
        </svg>
        <h3>Quick-Check Energie</h3>
        <p>2–3 Tage vor Ort, temporäre Messung, Ergebnisbericht mit drei Sofortmaßnahmen — zum Festpreis. Der unkomplizierte Einstieg.</p>
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
    <h2>Wer das macht</h2>
    <p>Mein Name ist Jörg Wünnenberg. Ich bin Dipl.-Ing. (FH) für Elektrotechnik mit Schwerpunkt Energieerzeugung und -verteilung, begonnen als Mess- und Regelmechaniker in der chemischen Industrie. <strong>Seit 2003</strong> führe ich mein eigenes Ingenieurbüro in Staufen im Breisgau.</p>
    <p>Was mich von reinen Beratern und reinen Automatisierern unterscheidet: Ich mache beides. Energieaudit nach DIN EN 16247 und BAFA-Antrag. SPS-Programmierung und Schaltschrankbau. Inbetriebnahme und Monitoring. Genau an der Lücke, an der sonst Beratungsberichte und Umsetzung auseinanderfallen.</p>

    <h3>Anerkannt und gelistet</h3>
    <ul class="badges">
      {% for q in site.data.site.qualifikationen %}
      <li><a href="{{ q.url }}" rel="noopener" target="_blank">{{ q.name }}</a></li>
      {% endfor %}
    </ul>
  </div>
</section>

<section id="referenzen">
  <div class="container">
    <h2>Referenzen</h2>
    <p class="section-lede">Gewerbe, Campingplätze, Sparkassen, Industrie — vom Kindergarten bis zur Trainingsanlage im Bereich Wasser- und Ölwirtschaft in der Schweiz.</p>
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
