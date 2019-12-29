# IslamBot

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/1a7ae76848b7466a9133899c882f3ec0)](https://www.codacy.com/manual/galacticwarrior9/islambot?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=galacticwarrior9/islambot&amp;utm_campaign=Badge_Grade) 
[![Discord Bots](https://top.gg/api/widget/lib/352815253828141056.svg)](https://top.gg/bot/352815253828141056)
![Discord](https://img.shields.io/discord/610613297452023837?label=Support%20Server)
[![Discord Bots](https://top.gg/api/widget/status/352815253828141056.svg?noavatar=true)](https://top.gg/bot/352815253828141056)
![GitHub contributors](https://img.shields.io/github/contributors/galacticwarrior9/islambot?color=yellowgreen)

An Islamic bot for Discord, with support for:

* *Qur'an*, with 75 translations available
* *Hadith* from sunnah.com, in both English and Arabic
* *Tafsir* (Qur'anic commentaries), with 7 in English and 28 in Arabic
* Viewing the morphology of every word in the Qur'an
* Prayer times
* Conversions between the Hijri and Gregorian calendars
* A custom search engine
* Visualisation of Qur'an verses on a virtual *mushaf*

IslamBot is licensed under the [GNU General Public License v3.0](https://github.com/galacticwarrior9/islambot/blob/master/LICENSE). You may use and modify its code for your own purposes as long as credit is given and it is made open source. 


Created by Zaify#6850. Contributors: ala and Caleb.


## Qu'ran 


### -quran

**-quran** allows you to quote Qu'ran verses in English, with an optional translation.


```

-quran <surah>:<verse(s)> [translation]

```


For example:


```

-quran 1:1-7 yusufali 

```

The above command would quote Surah 1, Verses 1-7 (Surah al-Fatihah) using the translation of Yusuf Ali.


#### Valid translation editions


[Click here for a list of valid translations.](https://github.com/galacticwarrior9/islambot/blob/master/Translations.md)

#### -settranslation


This command allows you to change the default translation of `-quran` on your server. You must have the `Manage Server` or `Administrator` permission to use this command. 


```

-settranslation <translation>

```


For example:


```

-settranslation sahih 

```

The above command would set the default Qur'an translation to Sahih International. 

[Click here for a list of valid translations.](https://github.com/galacticwarrior9/islambot/blob/master/Translations.md)

### -aquran

**-aquran** functions in the same way as **-quran**, but quotes the verse in Arabic.


For example, to quote the first verse of the Qu'ran:

```

-aquran 1:1

```


### -morphology

**-morphology** allows you to analyse the Arabic morphology of any word in the Qur'an.


```

-morphology surah:verse:word number

```


For example:

```

-morphology 1:2:4

```

The above would analyse the morphology of the 4th word of the 2nd verse of the 1st chapter of the Qur'an. 


### -mushaf

**-mushaf** fetches the image of the page on which a verse would be on a standard *Medina Mushaf*. 


```

-mushaf <surah>:<verse>

```


For example:

```

-mushaf 1:2

```

The above would send an image of the page containing Qur'an 1:2 on a *Medina Mushaf*. 

## Tafsir (Commentaries on the Qur'an) 


### -atafsir

**-atafsir** allows you to quote from over 26 Arabic *tafaseer* (commentaries on the Qurʾān). A list of valid *tafaseer* is available [here](https://github.com/galacticwarrior9/islambot/blob/master/Tafsir.md).


```

-atafsir <surah>:<verse(s> [tafsir]

```


For example:


```

-atafsir 2:255 tabari

```


The above command would quote the tafsir of Ayatul Kursi from Tafsir al-Tabari.



### -tafsir

**-tafsir** allows you to quote the English tasfir (commentary) of verses from Tafsīr al-Jalālayn (`jalalayn`), Tafsīr Ibn Kathīr (`ibnkathir`), Tafsīr al-Tustarī (`tustari`), Rashīd al-Dīn Maybudī's Kashf al-Asrār (`kashf`), al-Qurayshi's Laṭāʾif al-Ishārāt (`qurayshi`), Tafsīr ʿAbd al-Razzāq al-Kāshānī (`kashani`) and al-Wahidi's Asbāb al-Nuzūl (`wahidi`). It works in the same manner as **-atafsir**.


```

-tafsir <surah>:<verse> <jalalayn/ibnkathir/kashf/tustari/qurayshi/kashani/wahidi>

```


For example:


```

-tafsir 1:1 ibnkathir

```

The above command would quote the tafsir of Surah al-Fatihah, verse 1 from Tafsir Ibn Kathir. 


## Hadith 


### -hadith

**-hadith** allows you to quote hadith from sunnah.com in English.


```

-hadith <hadith book name> <chapter number>:<hadith number>

```


For example, to quote the second hadith in Chapter 1 of Sahih Bukhari:

```

-hadith bukhari 1:2

```

The above would scrape the hadith from https://sunnah.com/bukhari/1/2

#### Valid hadith book names 

* bukhari = Sahih al-Bukhari
* muslim = Sahih Muslim
* tirmidhi = Jami` at-Tirmidhi
* abudawud = Sunan Abi Dawud
* nasai = Sunan an-Nasa'i
* ibnmajah = Sunan Ibn Majah
* malik = Muwatta Imam Malik
* riyadussaliheen = Riyad as-Salihin
* adab = Al-Adab al-Mufrad
* bulugh = Bulugh al-Maram
* qudsi = 40 Hadith Qudsi
* nawawi = 40 Hadith Nawawi

40 Hadith Qudsi or Nawawi are both only 40 hadith long and therefore do not use a chapter number.


For example:

```

-hadith qudsi 32

```


Not all hadith are indexed correctly on sunnah.com, and not all use the same numbering as in the books - so please keep this in mind.


### -ahadith

**-ahadith** is the same as -hadith, but allows you to quote the hadith in Arabic. 


## Prayer (Salaah) Times


The bot can also fetch the prayer times for any location. More precise locations (e.g. addresses) will yield more precise prayer times. 


```

-prayertimes <location>

```


For example:

```

-prayertimes Los Angeles

```


..would fetch prayer times in the general area of Los Angeles. 

## Hijri Calendar


The bot can also (rather inaccurately) convert both ways between the Hijri and Gregorian calendars.


### -converttohijri

Converts a Gregorian date to its corresponding Hijri date.


```

-converttohijri DD-MM-YY 

```


For example:

```

-converttohijri 31-08-2017

```


### -convertfromhijri

Converts a Hijri date to its corresponding Gregorian date.


For example, to convert 17 Muharram 1407:

```

-convertfromhijri 17-01-1407

```


## Search


The bot can search several Islamic websites, including islamqa.org, islamqa.info and seekershub.org.


### -search

Search Islamic websites for a given query.


```

-search <search query>

```


For example:

```

-search Can Hanafis eat shrimp? 

```





