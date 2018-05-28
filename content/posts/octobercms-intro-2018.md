---
title: "Octobercms Intro 2018"
date: 2018-05-24T11:39:01+07:00
draft: false
---

<script type="text/javascript" src="https://ssl.gstatic.com/trends_nrtr/1435_RC10/embed_loader.js"></script> <script type="text/javascript"> trends.embed.renderExploreWidget("TIMESERIES", {"comparisonItem":[{"keyword":"OctoberCms","geo":"","time":"today 5-y"},{"keyword":"wordpress","geo":"","time":"today 5-y"}],"category":0,"property":""}, {"exploreQuery":"date=today%205-y&q=OctoberCms,wordpress","guestPath":"https://trends.google.com:443/trends/embed/"}); </script> 

OctoberCMS jelas bukan platform CMS yang populer. Perbandingan google trends di atas sepertinya cukup membuktikan pernyataan tadi. 
Wordpress menang, dari segi popularitas. 

OctoberCMS adalah plaftorm CMS yang dibangun menggunakan fondasi Laravel. Framework PHP dengan 43K Stars di github di tahun 2018. 
Semakin banyak yang pakai, semakin banyak yang nemu error, semakin banyak yang betulin error nya, semakin banyak yang jago. Stable release keluar pada Juli 2016 dengan fondasi Laravel 5.1, kini 2018 sudah menerapkan Laravel 5.5 sebagai fondasinya. Jadi, walaupun OctoberCMS kalah telak dari segi popularitas dibanding Wordpress. Developer jangan takut buat mempercayakan proyeknya ke OctoberCMS. 

Ok, to start. Instalasi OctoberCMS terhitung sangat mudah. [ http://octobercms.com/docs/setup/installation ] 

Ada 2 cara:

- Installer Wizard 
 - Download: http://octobercms.com/download
 -
- Composer 
 - ``` composer create-project october/october myoctober ```

Favorit saya? Installer Wizard!
![OctoberCMS Install Page](/img/octo-install-page.png)

Dengan Installer wizard saya bisa sekalian lihat apakah environment nya sudah mencukupi requirement dari Core OctoberCMS. 
Instalasi di hostingan (via cPanel) juga lebih mudah atau lebih memungkinkan menggunakan installer wizard. 



Database yang di support MySQL, Postgres, SQLite, SQL Server
![OctoberCMS DB Setup Page](/img/octo-dbsetup-page.png)



Favorit saya SQLite, simple setup, tak perlu create database, create user, assign privilege, dsb dulu. Apalagi untuk proyek website yang tidak super kompleks. 
Seperti blogging, landing page, commerce site skala menengah ke bawah. Kata sqlite.org "Generally speaking, any site that gets fewer than 100K hits/day should work fine with SQLite" https://www.sqlite.org/whentouse.html. 


![OctoberCMS DB Sqlite Page](/img/octo-sqlite-page.png)


Database SQLite ini disimpan di satu file. Perlu di backup? Copy-paste aja filenya. Mau di restore? Copy-paste lagi aja filenya. Nanti tinggal set *fullpath* file nya di config/database.php

![OctoberCMS Admin Setup Page](/img/octo-adminsetup-page.png)

Ini untuk login ke backend area nya. 


![OctoberCMS Advance Setup Page](/img/octo-advance-page.png)

Kita juga bisa set custom backend URL, supaya lebih sulit ditebak aja. Encryption Code itu bawaan dari Laravel. 
Permission mask untuk folder yang akan di instalasi. Set 777 aja.

![OctoberCMS Get Started Page](/img/octo-getstarted-page.png)

- Start from scratch : Tenang, ga bakal kosong banget kok, opsi ini include sample code untuk themes dan plugin. All you need to start your new project.
- Start from a theme : Klik, pilih featured theme, nanti didownloadin sama installernya. Belum nemu yang disukain? Pilih Start from scratch aja, nanti bisa pilih theme lagi di https://octobercms.com/themes
- Use a project ID : Ini lebih canggih, kita set project di website Octobercms.com , pilih theme & plugin yang perlu diinstall disana, dapet project ID, masukin disini, nanti diinstallin sama installernya.


Buat yang mau belajar, pilih antara Start form scratch atau Start from a theme. Saya pribadi nyaranin pilih start from scratch dulu, karena code dan implementasi di setup opsi ini ga banyak. Tapi cukup buat mulai pelan-pelan memahami platform OctoberCMS ini. 

![OctoberCMS Success Page](/img/octo-success-page.png)

Next post kita coba cover soal themes.


```
    public function registerComponents(){
    return [
            'RedMarlin\Faq\Components\FaqList' => 'FaqList',
            'RedMarlin\Faq\Components\FaqAsk' => 'FaqAsk',
            'RedMarlin\Faq\Components\FaqLast' => 'FaqLast',
            'RedMarlin\Faq\Components\FaqFeatured' => 'FaqFeatured',
            'RedMarlin\Faq\Components\FaqAll' => 'FaqAll',
    ];
    }
```