---


---

<p>Terminé la parte de hacer scraping a la página inicial de un área en Airbnb, de hecho usé 4 zonas del área de Mazatlán, Sinaloa, para aumentar la cantidad de listings para hacer scraping.</p>
<p>El archivo con el que se inicia es <code>scrape_page.py</code>, el cual toma 4 links de Airbnb y les hace el scraping tanto a la página inicial como hasta 10 páginas máximo del paginado; se mandan parámetros de 30 días en el futuro, 3 noches de estancia y 2 huéspedes.</p>
<p>Para obtener el código donde residen los datos de los listings, ví que se manda dentro de un script en formato json:</p>
<p><code>scripts = soup_html.find_all("script", attrs={"type":"application/json", "id":"data-injector-instances"})</code></p>
<p>Y cada listing se obtiene en el siguiente nodo:</p>
<pre><code>results = node["root &gt; core-guest-spa"][1][1]["niobeMinimalClientData"][1][1]["data"]["presentation"]["staysSearch"]["results"]["searchResults"]
</code></pre>
<p>Así se ve el listing procesado a json:<br>
<a href="https://postimg.cc/HVW9C36y"><img src="https://i.postimg.cc/WbgWgHrX/temp-Imager-Pi-Uyd.avif" alt="temp-Imager-Pi-Uyd.avif"></a></p>
<p>Después de hacer el scraping completo de las 4 páginas base, se obtuvo un total de 1,692 registros, con los que haré Exploratory Data Analisys (EDA) en los siguientes posts, en los cuales inicialmente tendré que realizar las siguientes actividades:</p>
<ul>
<li>Ver que los acentos se vean correctamente cuando los cargue en un DataFrame</li>
<li>estandarizar el campo roomTypeCategory</li>
<li>separar los valores del campo rating (calificación y evaluaciones)</li>
<li>análizar el campo de camas</li>
<li>cambiar el valor de price a número</li>
<li>analizar valores repetidos</li>
</ul>

