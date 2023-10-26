---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# Socijalni inžinjering ![](https://i0.wp.com/www.zastitapodataka.com/wp-content/uploads/2012/07/soc-inzenjering.jpg)
---
# Definicija
* Socijalni inžinjering predstavlja tehniku manipulacije ljudima koja se zasniva na ljudskoj nepažnji ili neznanju.
* Cilj napadača uglavnom nije žrtva sama, već neki resursi koji su napadaču interesantni
* čovek najslabija karika u lancu bezbednosti informacionog sistema
* Radionica će obuhvatiti stvari koje ne uključuje definicija

---

![h:600](https://d12qk6n9ersps4.cloudfront.net/168663/big-clean.jpg)

---

# Kevin Mitnik 
Knjige: 
  * Umetnost prevare
  * Umeće provale
  * Ghost in the wires 
---
  
---
# Viktor Lustig
![h:400](https://www.dnevno.rs/wp-content/uploads/2018/05/47489-ajfelov-toranj.jpg)

---
# Deca
![h:500](https://static.makeuseof.com/wp-content/uploads/2017/01/Child-Hacker-Featured-670x335.jpg)

---
# Neke tehnike socijalnih inzinjera
* Kopanje po kontejneru (Dumpster diving)
* Shoulder surfing
* Impersonation
* Maliciozne kopije sajtova

---
![h:400](https://mainehost.com/wp-content/uploads/2017/10/phishing03_web-1024x576.png)

# Fišing (Spear-phishing and Whaling)

---

# Smishing ![](https://www.kurir.rs/data/images/2017/10/10/16/1300067_1a1226c1b334456080b30c9733711dd6_ff.jpg?ver=1507645349)

---

# Vishing 

![](https://i0.wp.com/thevpn.guru/wp-content/uploads/2018/05/What-Is-Vishing-How-to-Stay-Safe.jpg?resize=869%2C551&ssl=1)

---

# Baiting

* Postavljanje klopke
* "Izgubljeni fleš", CD, DVD
* Preuzimanje zaraženih fajlova sa interneta
* Bluetooth

---

# Tailgating (Uhođenje)

* Pristup prostorijama za koje nema dozvolu
* Ući sa grupom, sa nekim ko ima dozvolu
* Duvan je štetan za bezbednost firme
* Drugacije oblačenje (glumiti zauzetost)
* Pozajmljivanje uređaja

---

# Psihologija
* Facijalna ekspresija
* Govor tela
	* [Bombards body language](https://bombardsbodylanguage.com)
* Emotional hijacking
* Misdirection
* => Neurolingvističko hakovanje

---

# Psihologija
*   Pretexting (izmišljanje scenarija)
*   Quid pro quo (usluga za uslugu)
*   Poverenje
*   Želju osoba da nekom pomognu
*   Želju za odredjenom materijalnom ili nematerijalnom koristi
*   Znatiželju
*   Strah od nepoznatog
*   Strah od gubitka
*   Nemarnost
*   Ignorisanje pravila

---
![h:600](https://preview.redd.it/16mbnhk78yy01.jpg?width=640&crop=smart&auto=webp&s=db1d67bfc5bdb2c55cc2d7260b1c9a871ce1a23e)

---
# Google-fu
![h:500](https://cdn-images-1.medium.com/max/1200/1*qjoBOz-6Gh-wYIZ4Ki9fUw.jpeg)

---

# Napredne tehnike pretrage
* Najmoćniji alat
* [Napredni gugl](https://www.google.com/advanced_search)
* site:
* type:
* -tekst , iskljucuje rezultate koji sadrze tekst nakon -
* allinurl: allintitle: allintext:
---

# Maltego
* Vizuelizacija povezanosti izmedju razlicitih informacija
* https://www.maltego.com/ (Postoji vec u Kali Linuksu)
* Novi graf (ctrl+T)
* Domen -> DNS from Domain

---
# Recon-NG
* https://github.com/lanmaster53/recon-ng
* ```./recon-ng --no-check```
* ```workspaces add target.com```
* ```show modules```
* ```use netcraft```
* ```run```
---

![h:600](https://external-preview.redd.it/6gAENgFfdHgRLUj753RLzaZuQKaOB1pTIbb9h3R1Lyk.jpg?auto=webp&s=b384a75c65665d52fd7b7176a3d5418ffb5dd349)

---
# Targeting
* Prikupljanje informacija je kljucno
* Presonalizovanje napada
* Alati:
	* SET (Social Engineering Toolkit)
    * Cupp
    * Cewl
    * Shodan
    * Scythe
    * Creepy
---
# SET (Social Engineering Toolkit)
* https://github.com/trustedsec/social-engineer-toolkit
* tinyurl
* kopija gugla
---
# Cupp
* https://github.com/Mebus/cupp
* Common user passwords profiler
* Generise dictionary za dicitionary attack
 * Odgovaranjem na pitanja formira se personalizovan rečnik
* ``` ./cupp.py -l```
* ``` ./cupp.py -i```
 
---
# Cewl
* https://github.com/digininja/CeWL
* ```./cewl.rb --write output.txt --email --email_file email.txt --verbose https://www.website.org/```

---
# Shodan
* https://www.shodan.io/
* Libre tekstovi ([tekst 1](https://libre.lugons.org/index.php/2018/05/mracni-pretrazivac-sodan/), [tekst 2](https://libre.lugons.org/index.php/2018/12/pasivno-prikupljanje-informacija-nmap-i-sodan/))
* Registracija
* explore
* webcamXP

---
# Scythe
* https://github.com/ChrisJohnRiley/Scythe
* accountfile.txt
* ```./scythe.py --category social --summary --output output.txt```
---
# Creepy
* https://github.com/ChrisJohnRiley/Scythe
* Potreban je tviter nalog


---
# Zaštita:
* Edukacija na prvom mestu
* [';--have i been pwned?](https://haveibeenpwned.com/)
* Dvostepena autentifikacija
* Smanjite digitalni otisak
* Pazite koje informacije odajete
 * Ako vas neko požuruje - nije dobro
---

# Zaštita: jake šifre i menadžeri za šifre

![h:500](https://static1.squarespace.com/static/52ae955ce4b04f67f91b6df5/54aae3e9e4b041b86b038185/5c50dbf3b91c916b35790998/1592312294538/passwordmanagers2.png?format=1500w)


---
# Zanimljivi video snimci
* [The art of misdirection | Apollo Robbins](https://www.youtube.com/watch?v=GZGY0wPAnus&t=303s)
* [Primer vishing-a](https://www.youtube.com/watch?v=lc7scxvKQOo)