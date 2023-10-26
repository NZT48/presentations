---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# Bash scripting
![](https://cdn-images-1.medium.com/max/1200/1*v4o2AXLIJaHSZmqYZk26qA.jpeg)

---

# Sadržaj
* Uvod
* Kontrole toka
* Prosleđivanje parametara skripti
* Funkcije
* Regularni izrazi
* Crontab
* Finalna skripta

---
# Uvod

* #!/bin/bash
* Demo: inic skripta
  * Kreira direktorijum i par fajlova u tekucem direktorijumu
  
---
![](https://pics.me.me/didnt-chmod-755-your-new-bash-script-yeah-thatll-work-2568500.png)
---
# Uvod
* pipes |
* Demo: infoGather skripta
  * Pretpostavka: imamo root pristup nekom Linuks serveru
  * Skripta će prikupiti neke zanimljive informacije
* ssh hacker@server 'bash -s' < infoGather.sh
---
# Kontrole toka
![w:1000 h:500](https://3.bp.blogspot.com/-8O3l5veDajk/VK8JFFUfcJI/AAAAAAAAAU4/OzY46kmpdMA/s1600/Flowchart_FlowControl.png)

---
# IF

```
[ $var = 5 ]; echo $?
test $var = 5; echo $?
```
* Rezultat obrnut od očekivanog
* Za numeričko poređenje: -gt -lt -eq -geq -leq 
* -a za and, -o za or

```
[ -f f1.txt ]; echo $?
```
* -f file, -d dir, -z zero, -r read, -x exec

---

```
if [ $var -eq 1 ]
then
  cat f1.txt
else
  cat f2.txt
fi
```
* Demo: skripta rootCheck
  * Skripta koja proverava da li korisnik koji ju je pozvao ima root privilegije

---
# FOR

```
for i in $(cat f1.txt)
   do command
done
```
* Demo: skripta pingList
  * Pozvaćemo komandu ping za spisak domena iz fajla domains.txt

---

* Mogucnosti za for petlju:

```
for i in $(cat f1.txt)
for i in {1..5}
for i in {0..10..2}
for (( c=1; c<=5; c++ ))
for (( ; ; ))
```
* IFS - Internal Field Separator
 * default value = ```<space><tab><newline>```
 * ako želimo da nešto drugo bude delimiter
 ```
 oldIFS=$IFS
 IFS=:
 ```
---

# WHILE
```
v=1
while [ $v -lt 5 ]
do 
  echo $v; let v++; 
done
```
---

# Prosleđivanje parametara
* $1, $2 - parametri prosleđeni skripti
* $0 - komanda za pokretanje
* $# - broj prosleđenih parametara
* $@ - dohvata sve parametre (zna koji su odvojeni)
* $* - svi parametri spojeni u string

---

* Demo: nmapRead skripta
  * interaktivno uzimanje i prosleđivanje parametara Nmap-u
  * nmap -sT 147.91.79.140- 147.91.79.143 -p 80 -oG res.log

* Demo: scriptStarter skripta
  * pokreće skripte koje se nalaze u prosleđenom direktorijumu

---
# Opcioni parametri
```
while getopts a:b opt; do
  case $opt in
    a) param = $OPTARG;;
    b) echo "op -b"
       b=1;;
    *) echo "ERROR"
      exit -1;;
  esac
done
```
---
# Funkcije

```
function function_name {
  <commands>
}
```

```
function_name() {
  <commands>
}
```
* Argumenti se šalju kroz $1, $2 ...
* Povratna vrednost se šalje kroz $?

---
# Regularni izrazi (Regex)

* . - jedan karakter, * - nula ili nekoliko karaktera, <br>? - prethodni karakter 0 ili 1
* {3} - tačno tri karaktera
* [a-d]{4} - četiri karaktera, svaki iz skupa {a,b,c,d}
* Sed - Stream Editor
* Razlika Sed vs Awk?

---

# Crontab
* Zakazivanje izvršavanja skripti
* crontab -l
* crontab -e

![h:300](https://process.filestackapi.com/cache=expiry:max/resize=width:1050/gE30XyppQqyNCnNB4a5c)

---

# Demo: specScan skripta
* Skriptu može da pokrene samo korisnik sa root privilegijama
* Skripta se pokreće sa: ./specScan website.com -o -r report.txt -s
* -o je opcioni parametar za skeniranje OS na serveru na kom je prosleđen sajt
* -s je opcioni parametar za pokretanje pajton programa Sublister koji pronalazi podomene
---
![h:600](https://i.imgur.com/rv3qzKk.png)

---
# Bash vs Python

* Bash skripte ce biti krace nego kratki Pajton programi
* Bash skripte ce biti duze od duzih Pajton programa
* Brzina, isti princip
* Pipes
* Malo grananja u programu
* Automatizacija 
* Nisu potrebne strukture podataka
* EH mora znati oba!