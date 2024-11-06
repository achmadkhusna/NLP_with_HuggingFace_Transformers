<h1 align="center"> NLP With HuggingFace Transformers </h1>
<p align="center"> Berisi tentang pipeline dari HuggingFace Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white">
<img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white">

</div>

<ul><h2 align="center">Analisis</h2></ul>

<ol>
    <li>Zero-Shot Classification

  Model: Model yang digunakan  adalah model joeddav/xlm-roberta-large-xnli dan facebook/bart-large-mnli. Model ini dapat bekerja dengan berbagai bahasa, jadi sangat fleksibel. Disini, saya juga menggunakan modul pipeline dari library transformers, yang digunakan untuk mempermudah penggunaan model NLP.

  Fungsi: Model ini berfungsi untuk mengklasifikasi teks tanpa harus melatih model secara spesifik untuk menentukan label. Semisal, sebagai contoh teks yang saya gunakan adalah teks yang berbahasa Prancis tentang AI yang diujikan terhadap label seperti "teknologi" atau "pendidikan". Disini, model berhasil menjawab secara akurat yaitu label "teknologi" dengan persentasi 0.9954596161842346, yang mana ini menjadi nilai tertinggi dibanding dengan label- label lainnya.</li>
    <li>Text Generation

  Model yang Digunakan: gpt2.

  Fungsi: fungsinya yaitu untuk menghasilkan teks berdasarkan input yang diberikan. Pengaturan parameter seperti max_length, temperature, dan top_p memungkinkan pengendalian seberapa kreatif atau konservatif output yang akan dihasilkan.

  Contoh: Dengan input "The future of artificial intelligence is", model ini menghasilkan teks yang berkaitan dengan masa depan AI, dan model akan berusaha untuk memberi imbuhan kata/ kalimat yang sesuai dengan inputan yang diberikan.</li>
    <li>Fill-Mask

  Fungsi: Untuk mengisi bagian kata-kata yang menghilang yang ditandai dengan (masking).

  Contoh: Kalimat "Regular exercise like cycling and (masking) can improve heart health." mengidentifikasi kata yang paling tepat untuk menggantikan (masking), adalah "running" atau "swimming". Disini, model akan berusaha untuk untuk mengisi kata yang kosong yang sesuai dengan konteks pembahasan yang dibahas.</li>
    <li>Named Entity Recognition (NER)

  Fungsi: Fungsinya yaitu untuk Mengidentifikasi dan mengelompokkan entitas yang ada di teks, seperti nama orang, lokasi, atau organisasi.

  Contoh: Disini, saya menggunakan kalimat "Mr. Erick Thohir is the Chairman of BUMN". Dan disini, model berhasil mengidentifikasi dan mengelompokkan dengan akurat, yaitu Mr.Erick Thohir sebagai orang dan BUMN sebagai Organisasi. Semakin tinggi nilai persentasi yang diberikan  oleh model, semakin tinggi pula akurasi dari model yang dihasilkan.</li>
    <li>Question Answering

  Fungsi: Fungsinya yaitu adalah mengambil konteks dan pertanyaan yang diberikan, kemudian model akan menghasilkan jawaban yang relevan dari teks context dan questions.

  Contoh: Disini saya mengisi context nya berupa "Salah satu cabang olahraga populer di Indonesia adalah renang. Bagi orang yang tinggal dipedesaan olahraga ini dapat dilakukan di sungai, danau, atau pinggiran laut. Sedangkan di perkotaan olahraga ini biasa dilakukan di kolam renang yang dibuat khusus". Kemudian pertanyaan yang saya ajukan yaitu "renang adalah?", secara otomatis model akan berusaha menjawab pertanyaan tersebut menggunakan data yang diberikan kepada model berupa penjabaran singkat mengenai olahraga renang.</li>
    <li>Sentiment Analysis

  Fungsi: Fungsinya untuk menganalisis apakah kalimat yang diberikan bernilai Positif atau Negatif, maksut dari Positif-Negatif ini merujuk pada penilaian emosional atau reaksi yang terkandung dalam kalimat yang dianalisis.

  Contoh: Kalimat-kalimat positif seperti "Rafa graduated from college" akan mendapatkan skor yang tinggi untuk sentimen Positif. Sedangkan, "Mr. Husein lost his money when he was about to buy groceries at the store", mendapatkan sentimen Negatif.</li>
    <li>Summarization

  Fungsi: Fungsinya yaitu untuk meringkas kalimat yang kompleks dan menyederhakan teks tersebut dengan mengambil point-point pentingnya agar pembaca dapat dengan cepat memahami maksut dari teks tersebut tanpa membaca keseluruhannya. Kemudian, pada kode looping  for idx, sentence in enumerate(sentences, 1), digunakan  untuk melakukan analisis sentimen untuk setiap kalimat yang ada di daftar sentences untuk memastikan bahwa setiap elemen mendapatkan perhatian dan hasil analisis yang sesuai.
  Contoh: Dari kalimat yang saya jadikan contoh pada program diatas, menjabarkan tentang panduan praktis untuk menerapkan gaya hidup sehat guna meningkatkan kesehatan tubuh.Model secara otomatis akan berusaha meringkasnya menggunakan fungsi Summarization.</li>
    <li>Translation

  Model yang Digunakan: Helsinki-NLP/opus-mt-id-en.
  
  Fungsi: Fungsinya yaitu untuk menerjemahkan kalimat tersebut dari Bahasa Indonesia ke Bahasa Inggris dengan akurasi yang tinggi.

  Contoh: Kalimat sederhana seperti "Perkenalkan, nama saya Faiz." diterjemahkan dengan tepat menjadi "May I present, my name is faiz". Menggunakan fungsi translation.
</li>

<ul><h2 align="center">Kesimpulan</h2></ul>
Program diatas merupakan program yang menggunakan NLP atau pemrosesan bahasa alami yang dilakukan oleh model untuk mempermudah pekerjaan kita secara praktis, baik itu untuk mengklasifikasikan teks, mengenali entitas penting, hingga menganalisis sentimen dan menerjemahkan, semua fitur ini membuat kita lebih mudah berurusan dengan data teks. Dengan alat-alat ini, kita bisa dengan cepat menganalisis, membuat, dan menerjemahkan teks dalam berbagai bahasa. Ini sangat berguna di kehidupan sehari-hari, misalnya untuk menganalisis pasar, melakukan penelitian, atau berinteraksi dengan pengguna di platform digital.






