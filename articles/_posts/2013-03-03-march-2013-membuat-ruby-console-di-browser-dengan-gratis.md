---
layout: post
title: Cara Membuat Ruby Console di Browser dengan Gratis
cat: articles
author: Nia Mutiara
excerpt: Halo komunitas Ruby Indonesia! Apa kabar? Moga-moga makin rame aja yah! Saya baru selesai membuat tutorial Ruby yang lumayan interaktif. Pada tutorial tersebut, kamu bisa menjalankan kode Ruby dan mengubahnya sesuka hati, kemudian kamu jalankan kodemu sendiri. Biaya buat servernya gratis, tetapi cukup scalable. Kok bisa? Caranya?
---

Halo komunitas Ruby Indonesia! Apa kabar? Moga-moga makin rame aja yah! :D

Saya baru selesai membuat [tutorial Ruby yang lumayan interaktif](http://nyan.catcyb.org/mengenal-ruby). Pada tutorial tersebut, kamu bisa menjalankan kode Ruby dan mengubahnya sesuka hati, kemudian kamu jalankan kodemu sendiri. Biaya buat servernya gratis, dan moga-moga cukup scalable.

Kok bisa? Caranya?


## Yang Diperlukan

1. Sebuah halaman statis yang punya text editor web. [Ace](http://ace.ajax.org/) dapat diembed sebagai text editor web.
2. Sebuah server Ruby untuk menerima respons AJAX, menjalankan kode Ruby dan mengembalikan respons HTTP. Framework Sinatra cukup cocok untuk tujuan ini.<br/>
   Jika halaman statis berada pada domain (termasuk subdomain dan port) yang berbeda, perlu utak-atik aturan [CORS](http://en.wikipedia.org/wiki/Cross-origin_resource_sharing) sedikit.
3. Sebuah server untuk meng-cache hasil evaluasi server Ruby di atas. Tentunya, kita tidak mau server mengevaluasi hal yang sama berulang-ulang.

Nomor 1 gratis kalau pakai [Halaman Github](https://help.github.com/categories/20/articles). Nomor 2 dan 3 gratis juga kalau pakai [Heroku](http://www.heroku.com/).

## Langkah-Langkah

**Menyiapkan Halaman Statis:**

1. Buat halaman statis yang memiliki text editor web. Cara termudah adalah dengan mengembed editor [Ace](http://ace.ajax.org/). \[[Kode](https://gist.github.com/catcyborg/5074620) | [Demonstrasi](http://codepen.io/nmutiara/pen/KFBqm)\]
1. Taruh tombol untuk kirim permintaan HTTP POST dengan isi kode pada editor melalui AJAX. Saya pakai [jQuery](http://jquery.com/) di sini. \[[Kode](https://gist.github.com/catcyborg/5074620#file-main-js-L24)]
1. Siapkan kode kamu untuk [dihost di GitHub](https://help.github.com/articles/creating-project-pages-manually). \[[Kode](https://github.com/catcyborg/text-editor-web) | [Demonstrasi](http://nyan.catcyb.org/text-editor-web/)\]

**Menyiapkan Server Ruby dan Cache:**

1. [Sign up akun Heroku](https://api.heroku.com/signup), kemudian siapkan server [Sinatra di Heroku](https://devcenter.heroku.com/articles/rack#frameworks) untuk mengevaluasi kode Ruby. \[[Kode](https://gist.github.com/catcyborg/5074953)\]
1. Tambahkan [add-on](https://addons.heroku.com) [Memcachier gratis](https://addons.heroku.com/memcachier). Kamu juga perlu menginstal memcached di komputermu.
1. Siapkan kode untuk menghandle permintaan POST. \[[Kode](https://github.com/catcyborg/mengenal-ruby-eval/blob/master/app.rb#L20)\]
1. Cache hasil evaluasi. Gunakan SHA1 dari snippet sebagai kunci cache. \[[Kode](https://github.com/catcyborg/mengenal-ruby-eval/blob/master/app.rb#L33)\]
1. Tambahkan aturan CORS pada header dari respons. \[[Kode](https://github.com/catcyborg/mengenal-ruby-eval/blob/master/app.rb#L22)\]

Untuk lebih cepatnya, langsung saja host [kode ini untuk server Rubynya](https://github.com/catcyborg/mengenal-ruby-eval).

<hr/>

Setelah semuanya selesai, kunjungi halaman statis yang kamu buat dan... Hore! Sekarang kamu bisa membuat tutorial interaktif sendiri dan share ke teman-teman yang ingin belajar Ruby.
