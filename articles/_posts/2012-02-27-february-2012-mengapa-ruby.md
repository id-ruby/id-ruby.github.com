---
layout: post
title: Mengapa Ruby? Pandangan dari Aspek Bisnis
cat: articles
author: Fajrin Rasyid
excerpt: Berbicara soal pemrograman web, tidak dapat dipungkiri PHP masih merupakan bahasa yang paling populer digunakan, setidaknya di Indonesia.  Apabila kita bertanya, “Apakah Anda menguasai Ruby?” secara random kepada programmer web yang kita temui, kemungkinan besar akan menjawab tidak.
---

> Tulisan ini adalah rangkuman presentasi Jakarta.rb yang diberikan oleh Fajrin Rasyid pada Februari 2012.

Berbicara soal pemrograman web, tidak dapat dipungkiri PHP masih merupakan bahasa yang paling populer digunakan, setidaknya di Indonesia. Apabila kita bertanya, “Apakah Anda menguasai Ruby?” secara random kepada programmer web yang kita temui, kemungkinan besar akan menjawab tidak. Saya sendiri baru mengenal Ruby sekitar tiga tahun lalu, ketika [Bukalapak.com](http://www.bukalapak.com), yang merupakan salah satu produk awal kami ([Suitmedia](http://www.suitmedia.com)), mulai dirintis.

Faktanya, memang sulit bagi perusahaan (termasuk kami di Suitmedia) untuk mencari programmer Ruby, dan sebaliknya, sulit bagi programmer Ruby untuk mencari perusahaan yang bagus untuk bekerja. [Udemy](http://www.udemy.com/blog/modern-language-wars/) pernah membuat laporan terkait hal ini. Bagi programmer Ruby yang mencari tempat bekerja, Udemy merangkum dari Craigslist bahwa dari seluruh lowongan pekerjaan yang tersedia untuk programmer, hanya 3% lowongan bagi programmer Ruby, bandingkan misalnya dengan PHP (21%), C++ (12%),  atau C (10%).  Sementara itu, bagi perusahaan yang mencari programmer Ruby, Udemy menyatakan bahwa di LinkedIn hanya terdapat sekitar 700 programmer Ruby, bandingkan dengan PHP (19000) dan Python (1300).

Terlepas dari fakta bahwa banyak informasi lowongan ataupun SDM Ruby yang tidak terafiliasi dengan kedua situs tersebut, sepertinya fakta diatas tidak dapat dihindari. Lantas, apakah itu berarti Ruby adalah bahasa pemrograman yang kurang potensial? Tidak juga. Berikut beberapa hal yang menunjukkan bahwa Ruby adalah salah satu bahasa pemrograman yang efektif.

## 1. Ruby itu menyenangkan

  Kembali ke cerita diatas, ketika Suitmedia mulai mengembangkan Bukalapak.com, Nugroho (CTO Bukalapak, eks CTO Suitmedia) menyarankan untuk menggunakan Ruby karena menurutnya Ruby itu menyenangkan dan elegan. Beliau lantas membandingkan contoh kode yang diperlukan dalam bahasa Java dan Ruby untuk membuat beberapa fungsi yang sama sebagai berikut.

  Fungsi 1 – Java
  <pre>
    {% highlight java linenos %}
    class ThisIsAClassIDontReallyWantToNameButJavaMakesMe
    {
      public static void main() {
        System.out.println("Hello World");
      }
    }
    {% endhighlight %}
  </pre>

  Fungsi 1 – Ruby
  <pre>
    {% highlight ruby linenos %}
    puts ‘Hello World’
    {% endhighlight %}
  </pre>

  Fungsi 2 – Java
  <pre>
    {% highlight java linenos %}
    import java.io.File;
    import java.io.InputStream;
    // ... declare class, etc., then ...
    public byte[] justReadMeAFilePlease() {
      try {
        file = new File("my-file.txt");
        fis = new FileInputStream(file);
        byte[] b = new byte[(int) file.length()];
        fis.read(b);
        return b;
      } catch (Exception e) {
        e.printStackTrace();
      }
    }
    {% endhighlight %}
  </pre>

  Fungsi 2 – Ruby
  <pre>
    {% highlight ruby linenos %}
    contents = File.read ‘my-file.txt’
    {% endhighlight %}
  </pre>

  Pada akhirnya kami yakin bahwa Ruby memang elegan dan menyenangkan, khususnya bagi programmer yang sepenuhnya berinteraksi (membaca dan menulis) dalam bahasa tersebut. Oleh karena itu, kami sepakat untuk mengembangkan Bukalapak.com dalam bahasa Ruby karena iklim/suasana kerja yang menyenangkan adalah faktor terbesar dalam meningkatkan produktivitas kerja (dan karena itu baik bagi bisnis).

## 2. Ruby mudah dipergunakan kembali

  Masih bersumber dari Udemy, kebanyakan mengakui bahwa Ruby merupakan bahasa yang elegan dan powerful. Ruby sangat mudah dipergunakan kembali sesuai dengan prinsipnya yang seminimal mungkin menimbulkan kebingungan. Salah satu dampaknya adalah, mudah bagi programmer Ruby untuk mempelajari kode yang dibuat oleh programmer Ruby lainnya. Secara bisnis, ini akan mempermudah dalam maintenance produk yang dikembangkan. 

## 3. Meskipun tidak banyak, tetapi programmer Ruby biasanya adalah orang yang benar-benar suka membuat program

  Sederhananya, karena jumlah lowongan kerja Ruby jauh lebih sedikit dibandingkan lainnya, biasanya orang-orang mempelajari Ruby bukan untuk memperoleh pekerjaan, melainkan karena telah berinteraksi dengan dunia pemrograman cukup lama dan tidak puas dengan bahasa yang mereka sudah kenal. Hal ini melahirkan dua paradoks:

  Paradoks 1: “Apabila perusahaan mengembangkan program dalam bahasa yang tidak umum, maka perusahaan itu
  berpeluang untuk merekrut programmer berkualitas baik, karena programmer bahasa tersebut adalah
  orang-orang yang peduli untuk mempelajari dan mendalami bahasa pemrograman tersebut (bukan sekadar orang-orang yang mencari pekerjaan)”

  Paradoks 2: “Bahasa yang baik untuk dipelajari apabila Anda ingin mendapat pekerjaan, adalah bahasa yang dipelajari tidak hanya untuk mendapat pekerjaan”

  Kedua paradoks diatas memang tidak dapat dibuktikan secara ilmiah. Faktanya, tidak banyak perusahaan yang menyadari hal tersebut. Namun menariknya, perusahaan yang menyadari hal ini adalah perusahaan yang memang dicari oleh orang-orang. Tengok saja Twitter, Groupon, Github, Scribd, dan lain-lain yang berbasiskan Ruby. Singkatnya, meskipun jumlah lowongan ataupun SDM Ruby sedikit, kemungkinan besar kualitasnya akan berada diatas rata-rata.

## 4. Poin tambahan bagi startup

  Mungkin sebagian dari pembaca terlibat dalam startup, entah itu founder, tim, ataupun setidaknya pemerhati :) Dunia startup memang booming di Indonesia sejak beberapa tahun terakhir, dan salah satu karakteristik penting di dalam bidang ini adalah “all or nothing”. Artinya, tidak seperti perusahaan besar yang grafik pertumbuhannya tidak tajam, startup dapat tumbuh sekian kali lipat dalam waktu singkat, tetapi sebaliknya dapat hancur seketika. Dalam kondisi seperti ini, memiliki sesuatu yang berbeda bagi suatu startup adalah salah satu nilai lebih apabila dibandingkan dengan kompetitor, dan memiliki sistem berbasis Ruby adalah salah satu contohnya. 

Suitmedia sendiri mengalami beberapa poin diatas, contohnya ketika Nugroho harus berfokus di Bukalapak.com sehingga proyek-proyek yang sebelumnya ditanganinya di Suitmedia harus dialihkan ke programmer lain (dalam hal ini yaitu Dimas), hal tersebut dapat berjalan lancar dan cepat. Pun ketika Dimas harus berfokus di produk lain sehingga ia harus menyerahkan kembali proyek-proyek tersebut ke programmer lain (dalam hal ini yaitu Agung).

Tentunya, pembaca dapat mengalami hal-hal berbeda (ataupun sama) dengan yang tertulis disini. Oleh karena itu, silakan komentari, terima kasih :)
