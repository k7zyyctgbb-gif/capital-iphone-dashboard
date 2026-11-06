# Capital · iPhone-dashboard

Deze openbare repository is uitsluitend een **alleen-lezen GitHub Pages-dashboard** voor Capital.com DEMO V14.9.

De handelsbot draait afzonderlijk in de **privé-repository** `Capital.com-demo-v149`. Hier worden geen API-sleutels, wachtwoorden, rekeningbalansen, individuele posities of orderreferenties gepubliceerd.

## Online zetten

1. Open **Settings → Pages → Build and deployment** en selecteer bij **Source** `GitHub Actions`.
2. Open **Actions → Publish Capital iPhone dashboard** en start de workflow indien nodig met **Run workflow**.
3. Het verwachte adres is https://k7zyyctgbb-gif.github.io/capital-iphone-dashboard/.

De pagina begint met een lege status totdat de privébot een gefilterd `status.json`-bestand publiceert. Het dashboard kan geen orders plaatsen of de bot in- of uitschakelen.

## Veilige gegevensoverdracht

De privébot exporteert uitsluitend een beperkte, gesaniteerde status via een apart GitHub-token dat **alleen schrijfrechten voor de dashboard-repository** heeft. De eigenaar voegt dit token zelf toe aan de privébot als secret `CAPITAL_DASHBOARD_TOKEN`. Het token mag nooit in deze openbare repository worden geplaatst.

**Let op:** iedereen op internet kan de inhoud van deze repository en de GitHub Pages-website bekijken, inclusief `status.json`.
