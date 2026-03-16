---
layout: landing-page
---

**Dates**  
**{{ site.tournament_date_individual }}**: Individual Tournament  
**{{ site.tournament_date_team }}**: Team Tournament

**Tournament Venue**  
{% if site.venue_determined == true -%}
{{ site.venue_address_1 }}  
{{ site.venue_address_2 }}  
{{ site.venue_address_3 }}  
{{ site.venue_address_4 }}  
{{ site.venue_address_5 }}  
{% else %}
{{ site.tournament_location_city_state }}
{% endif %}

Visit the [Info page](/info.html) for more information.

Please email [competition@auskf.org](mailto:competition@auskf.org?Subject=AUSKF%20Jr.%20Nationals%20{{ site.tournament_year }}) for more information.
