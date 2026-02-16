Projekti: onko pelien pituus kasvanut vuosien myötä?

1. Ensin latasin kagglesta csv tiedoston steam peleihin liittyen. https://www.kaggle.com/datasets/gruffgemini/steam-games-dataset
2. Sitten tein databasen ja sinne tablen "games" ![[Pasted image 20260207125012.png]]
3. Pari tuntia meni koittaessa tuoda sql komennoilla csv tiedostoa databaseeni kunnes tajusin että voin käyttää mysql:än table data import wizardia!![[Pasted image 20260207165252.png]]
4. Sitten silläkään en saanut kaikkia rivejä joten jouduin korjaamaan local infile ongelman jotta sain kaikki 60 000 riviä tableeni. ![[Pasted image 20260208112840.png]]
 5. sitten tein hieman countteja mistä selvisi että tästä csv tiedostosta puuttui paljon tietoa, eli oli paljon nollia ![[Pasted image 20260208181615.png]]
 6. ![[Pasted image 20260208182048.png]]tällä komennolla saatiin selville että on kumminkin yli 15 tuhatta peliä mistä on peliaika dataa.
 7. tällä komennolla tehtiin VIEW ![[Pasted image 20260208182432.png]]
 8. sitten katsotaan viewiä ![[Pasted image 20260208182648.png]]
 9. ![[Pasted image 20260211135352.png]] tällä komennolla saatiin kaikki hours_main nullit pois.
 10. ![[Pasted image 20260211135909.png]] sitten laitettiin nuo komennot että saadaan vuosittain average hourit mutta sinne tuli year 0 joten se pitää vielä poistaa.
 11. sen sai pois laittamalla tämän komennon ![[Pasted image 20260211140122.png]]
 12. ![[Pasted image 20260211140255.png]] tästäkin tehtiin vielä oma view.
 13. seuraava vaihe on tämän vienti power bi:hin ![[Pasted image 20260211141511.png]]
 14. ![[Pasted image 20260216184324.png]] tämän näköinen viivakaavio saatiin, tässä pitää toki muistaa että data oli vähän huonoa ja sen takia tuolla on "games_with_lenght" mikä näyttää kuinka monta peliä on sinä vuonna otettu huomioon.
 15. tein siitä hieman paremman laittamalla toisen kaavion mikä näyttää kuinka monta peliä sinä vuonna oli datan mukaan.![[Pasted image 20260216184823.png]]
 16. Saadaan siis tulos että pelien pituus olisi laskenut ajan kanssa, mutta se on vain tämän datasetin kanssa. En usko että se pitää paikkansa.
