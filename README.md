## **Rangkuman “Tableau for Data Science”**

Catatan ini adalah rangkuman dari kursus Udemy berjudul : [**Tableau A-Z : Hands-On Tableau Training for Data Science**](https://www.udemy.com/course/tableau10/)  karya **Kirill Eremenko, dkk**. Jika ingin belajar lebih detail, saya sarankan untuk belajar di kursus tersebut.

Baca Ulasan ini di Medium: [Part I](https://ahmadilhamhabibi.medium.com/rangkuman-tableau-for-data-science-part-i-8e56f9cc6d35) and [Part II](https://ahmadilhamhabibi.medium.com/rangkuman-tableau-for-data-science-part-ii-b8db5a01077c)
[Link Tableau Publik saya](https://public.tableau.com/app/profile/ahmad.ilham.habibi#!/)

**1. Pengenalan Tableau**
Tableau Desktop memberikan semua yang Anda butuhkan untuk mengakses, memvisualisasikan, dan menganalisis data Anda. Dengan antarmuka seret dan lepas (_drag and drop_) yang intuitif, Anda dapat mengungkap wawasan tersembunyi yang Anda butuhkan untuk membuat keputusan bisnis yang berdampak (_impacful_) secara lebih cepat, bahkan saat Anda offline. (tableau.com)

Ada berbagai produk yang ditawarkan Tableau untuk menganalisis dan memvisualisasikan data, yaitu: Tableau Desktop, Tableau Public, Tableau Online, Tableau Server, dan Tableau Mobile.

Pada tutorial kali ini, saya menggunakan versi gratis dari Tableau, yaitu Tableau Public. Untuk mengaksesnya bisa mengklik link berikut : [https://public.tableau.com/app/discover](https://public.tableau.com/app/discover)

**2. Tableau Basic: Your First Bar Chart**
Pada bagian kedua kita diberi tantangan bisnis, “Siapa yang berhak mendapatkan _annual bonus_?”. Sebuah perusahaan beroperasi di tiga wilayah, seorang _top-performing_ di setiap wilayah akan mendapatkan _annual bonus_. Penentuan _top-performing_ dilihat dari total penjualan (_sales($)_).

Pertama, buka Tableau Public kemudian masukkan data yang ingin dianalisis. Pada bagian kiri Tableau terdapat pilihan **Connect** yang bisa digunakan untuk menghubungkan data yang ingin dianalisis atau divisualisasikan. Ada beberapa jenis file yang dibisa dihubungkan dengan Tableau, diantaranya: Microsoft excel, Text file (csv, dll), JSON, Microsoft Access, PDF, dan lain sebagainya.

Pada tab **Data Source** kita bisa melihat informasi tentang data yang akan dianalisis. Seperti nama kolom, jenis data pada kolom, jumlah baris, dan lain sebagainya. Berikut adalah tampilan pada tab **Data Source** setelah menghubungkan data.

![Data Source](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/2.2-DataSource.jpg)

Pada tab **Data Source** ini kita juga bisa membuat hubungan antar data dan menggabungkan (_union_) data jika kita memasukkan lebih dari satu data. Mirip konsep **Data Modelling** pada Power BI.

**Membuat _Calculated Fields_**  
Pada Tableau kita juga bisa membuat _Calculated Fields_. Fungsinya adalah membuat _fields_ berdasarkan kolom yang ada menggunakan kaidah matematika. _Fields_ yang telah dibuat bisa digunakan untuk memvisualisasikan data secara berulang-ulang.

Pada tantangan bisnis diawal materi, kita diminta menentukan siapa yang mendapat _annual bonus_ berdasarkan nilai penjualannya berdasarkan total sales atau _revenue_ yang diperoleh. Sedangkan pada data tidak terdapat kolom _Sales_, namun ada kolom _Units_ dan _Unit Price_. Kita bisa membuat **Calculated Fields** dengan nama _TotalSales_ dengan mengalikan _Units_ dengan _Unit Price._

Letakkan _TotalSales_ pada **Rows** untuk memperoleh visualisasi yang sesuai degan tantangan bisnis yang ingin diselesaikan. Maka hasilnya akan seperti berikut ini:

![TotalSales](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/2.9-TotalSales.jpg)

**Menambahkan Warna dan Label**
Dengan memasukkan kolom _Region_ pada **Color** kita bisa membedakan warna pada setiap wilayah, karena kita ingin mencari _top-performance_ di setiap wilayah. Kemudian tambahkan label pada data agar lebih mudah dibaca. Pada wilayah _West_ puncak bar chart hampir menunjukkan nilai yang sama. Agar lebih terlihat jelas maka diberi label pada data yang berisi _TotalSales_ untuk masing-masing _sales person._

![Annual Bonus Analysis](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/2.10-AnnualBonusAnalysis.png)

Dari gambar diatas kita bisa menentukan siapa saja yang berhak mendapat annual bonus.  
- Central = Matthew, total sales : $3.1 K  
- East = Susan, total sales : $3.1 K  
- West = James total sales : $1.3 K

**3. Time Series, Aggregation, dan Filters**
_Time Series_ merupakan salah satu tipe data yang unik. Pada Tableau. tipe data _Time Serie_s bisa diekstrak menjadi jenis data _dimension_ (kategorikal) dan _measure_ (numerikal).

Letakkan _Period_ pada **Columns** dan _Unemployment_ pada **Rows.** Kolom _Period_ merupakan data dengan tipe **Time Series** bisa menampilkan _Year, Quarter, Month_, serta _Day_. Kolom _Period_ juga bisa diubah menjadi _dimension_ (warna biru) atau _measure_ (warna hijau).

![Time Series](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/3.1-UnEmploy.jpg)

**Membuat Area Chart**
Setelah mengubah **Marks** menjadi _Shape_, menambahkan kolom _Gender_ pada **Color**, serta menambahkan _Age_ pada **Details**, maka visualisasinya menjadi seperti berikut:

![Shape](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/3.5-Shape.jpg)

Dari visualisasi diatas kita bisa memperoleh informasi lebih detail tentang _Gender_ dan _Age_. Namun visualisasinya kurang enak dipandang dan menjadi lebih membingungkan. Mari kita ubah menjadi **Area Chart**, untuk memperoleh visualisasi yang lebih baik. Tambahkan _Age_ pada **Color** dan **Label** agar lebih mudah dipahami.

![Area Chart](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/3.6-Area.jpg)

Selanjutnya kita tambahkan kolom _Gender_ untuk memfilter data untuk berinteraksi dengan visualisasi yang telah kita buat. Masukkan kolom _Gender_ pada **Filters** di sebelah kiri. Klik kanan pada _Gender_, kemudian pilih **Show Filter**. Kemudian akan muncul filter pada bagian kanan atas visualisasi. Maka hasilnya akan menjadi seperti berikut:

![Final Area Chart](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/3.7-UnemploymentChart.png)

**4. Map, Scatterplots, dan Dashboard**
Kali ini kita juga akan dikenalkan dengan konsep JOIN pada Tableau. Pada dasarnya sama dengan konsep JOIN pada SQL maupun Power BI, ada Inner Join, Left Join, Right Join, serta Full Outer Join. Serta harus ada kolom yang sama pada masing-masing data yang akan dilakukan JOIN, seperti penentuan ON pada JOIN di SQL.

Pada Tableau proses JOIN dilakukan ketika proses menghubungkan data di **Data Source**.

![JOIN](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/4.1-JOIN.jpg)

Pada contoh diatas kita melakukan Inner Join pada tabel **ListOfOrder** dan **OrderBreakdown**, dengan kolom _Order ID_ sebagai acuannya. Setelah berhasil melakukan JOIN maka kedua kolom dari kedua tabel bisa dimanfaatkan untuk memvisualisakikan data.

Ketika kolom **Hierarchy** dimasukkan kedalam Working Area, kita bisa menentukan data yang ingin ditampilkan. Karena datanya merupakan data geography maka otomatis akan ditampilkan sebagai **Map**.

Ubah ukuran **Mark** dengan menambahkan kolom _Sales_ ke dalam **Size**. Maka visualisasi akan berubah menjadi seperti berikut:

![Add Size](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/4.5-AddSize.jpg)

Buat **Calculated Fields** dengan nama _Profit Margin_ yang menghitung total _Profit_ dibagi dengan total _Sales_. Kemudian masukkan kedalam Color untuk melihat _Profit Margin_ di setiap _State_.

![Add Color](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/4.6-AddColor.jpg)

Visualisasi Map telah selesai dibuat, selanjutnya kita akan membuat Scatterplot untuk melihat sebaran _Profit Margin_. Ubah nama sheet1 dengan nama **Map of Europe**. Buat sheet baru dengan nama **Customer Scatter Plot**.

Ketika membuat banyak visualisasi (lebih dari satu worksheet), kita bisa memanfaatkan satu filter saja. Tidak perlu membuat filter berulang-ulang pada setiap worksheet. Caranya klik kanan pada **Filter**, pilih A**pply to Worksheet**, kemudaian pilih **All Using This Data Source**.

![Filter](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/4.7-Filter.jpg)

Pada sheet **Customer Scatter Plot** letakkan  _Sales_  di **Columns,** _Profit_ di **Rows,** dan  _Customer Name_  di **Detail.** Maka kita akan mendapat visualisasi berupa Scatterplot yang menunjukkan posisi _Customer Name_ berdasarkan _Sales_ dan _Profit_. Tambahkan _Profit Margin_ yang telah kita buat sebelumnya pada **Color** untuk membedakan warna pada scatterplot.

![ScatterPlot](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/4.9-ScatterPlot.jpg)

Sampai tahap ini kita telah memiliki dua visualisasi, Map dan Scatterplot. Selanjutnya gabungkan kedua visualisasi tersebut kedalam Dashboar sederhana agar bisa mendapat informasi secara utuh. Untuk membuat dashboard kita cukup _drag and drop_ sheet yang ingin dimasukkan kedalam dashboard dan sesuaikan fitur yang ingin ditampilkan dalam dasboard.

Masukkan sheet **Map of Europe** dan **Customer Sactter** **Plot** kedalam dashboard, kemudian atur pada posisi _Vertical_. Di sisi kiri tambahkan filter untuk melihat sebaran data pertahun. Lakukan seperti pada sheet sebelumnya, tampilkan dalam **Single Value (slider)** serta  A**pply to Worksheet =>** **All Using This Data Source**.

![Dashboard](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/4.11-Dashboard.jpg)

Tableau punya fitur untuk berinteraksi dengan dashboard dengan menambahkan fitur **Filter** dan **Highlight**. Kedua fitur ini berguna untuk menampilkan data tertentu, misalnya ingin menampilkan data yang berasal dari Bavaria di Jerman.

**5. Joining, Blending, and Relationships**

Konsep JOIN pada Tableau sama dengan konsep JOIN pada SQL maupun Power BI, ada Inner Join, Left Join, Right Join, serta Full Outer Join. Serta harus ada kolom yang sama dimasing-masing data yang akan dilakukan JOIN, seperti penentuan ON pada JOIN di SQL.

Tableau punya fitur **Blending** yang hampir sama dengan JOIN. Namun, Blending tidak langsung menggabungkan data pada **Data Source**, tetapi digunakan untuk melakukan JOIN data pada worksheet. **Blending** disebut juga _Smart JOIN._ Dalam **Blending** berlaku LEFT JOIN, tabel pertama ditandai dengan warna hijau di depan tabel sedangkan tabel kedua ditandai dengan warna merah.

Ada dua alasan mengapa kita menggunakan **Blending** daripada JOIN. Pertama, ketika kita tidak ingin kehilangan informasi dari tabel, karena JOIN hanya akan menampilkan data yang sesuai dengan data pertama dan tidak menampilkan data kedua yang tidak sesuai. Kedua, ketika tabel berasal dari **Data Source** yang berbeda, misalnya dari dua file Excel.

Kali ini kita akan mempraktikan **Blending** pada Tableau menggunakan data dari dua tabel sederhana. Tabel **Arline1** dengan kolom _Period, Region, Revenue_ dan **Arline2** dengan kolom _Year, Region, Revenue._ Kolom _Period_ dan _Year_ sama-sama berisi data tahun, hanya beda nama kolom saja.

Disinilah kita perlu melakukan **Blending** untuk kolom _Period_ dan _Year_.  
- pada menu bar pilih **Data**  
- kemudian pilih **Edit Blending Relationships**  
- disini kita melihat telah dibuatkan **Blending** antara _Region_, kemudian ketik **Add** untuk menambah **Blending** baru  
- klik _Period_ pada tabel pertama dan _Year_ pada kolom kedua  
- klik **OK** untuk menerapkan Blending

Setelah dilakukan **Blending** maka datanya akan berubah sesuai dengan data yang ada, karena tabel kedua sudah mengenal _Period_ setelah dilakukan **Blending** dengan _Year_.

![Blending](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/5.6-AfterBlend.jpg)

Tableau secara otomatis melakukan **Blending** pada kolom yang memiliki nama yang sama, seperti pada kolom _Region_. Sedangkan kolom _Period_ dan _Year_ meniliki nama yang sama. Cara sederhana melakukan **Blending** adalah dengan menyamakan nama kolom. Misal sama-sama bernama _Period_ atau sama-sama _Year_. Maka akan otomatis dilakukan **Blending**.

Materi terakhir pada bagian ini adalah **Relationship**, yang berfungsi menghubungkan data antar tabel. Konsepnya sama dengan pada Power BI. Sebagai contoh kita akan membuat **Relationship** seperti _Data Schema_ berikut:

![Schema](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/5.7-DataSchema.png)

Cara membuat **Relationship** pada Tableau  juga cukup mudah, tinggal _drag and drop_ data yang ingin dihubungkan kemudian sesuaikan kolom yang dijadikan acuan untuk mambuat **Relationship.**

Sesuaikan tabel-tabel dan kolom yang ada hingga semua tabel terhubung. Maka hasilnya seperti pada gambar berikut:

![Relationship](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/5.9-RelationshipsFinal.jpg)

**6. Table Calculations, Advanced Dashboard, Storytelling**

Dengan **Story** kita bisa menceritakan _insight_ yang kita dapatkan menjadi sebuah laporan yang menarik.

**Set Geographical Role**  
Pertama kita akan membuat visualisasi berupa Map untuk wilayah United Kingdom berdasarkan kolom _Region_. Tetapi kolom _Region_ berupa data teks bukan data _geography_ (map). Kasus seperti ini sering kita jumpai ketika ingin membuat Map. Solusinya adalah dengan menentukan **Geographical Role** pada data yang ingin dibuat menjadi Map.  
- klik kanan pada kolom _Region_  
- klik **Geographical Role **
- pilih **state/province**

Setelah berhasil maka kolom _Region_ akan berubah menjadi data _geographic_ (tanda _globe_ pada awal kolom). Ubah **Marks** menjadi Map. Tambahkan kolom _Region_ ke dalam color untuk melihat batas masing-masing **state**. Tambahkan kolom _Count_ yang dibuat otomatis oleh Tableau untuk melihat jumlah pelanggan ada masing-masing **state**. 

![Map](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.4-Map.jpg)

**Tabel Calculation**
Selanjutnya kita akan membuat Pie Chart untuk melihat sebaran _Gender_ pada data. Kita juga akan memanfaatkan fitur **Tabel Calculation** untuk mengubah data yang ditampilkan. Buat Pie chart dengan memanfaatkan kolom _Gender_ dan kolom _Count_ untuk melihat jumlah datanya.

![Pie](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.5-PieChart.jpg)

Pada gambar diatas data ditampilkan dalam jumlah total. Kita bisa mengubah tampilan ini dengan memanfaatkan fitur **Table Calculation**.  
- klik kanan pada kolom _Count_  
- pilih **Edit Table Calculation**  
- pilih **Percent of Total**

Selain Percent of Total, juga terdapat pilihan lainnya seperti: Running Total, Difference, Percent Difference, Percentile, dan Moving Average.

Setelah diubah menjadi persen dan disesuaikan formatnya, maka visualisasinya menjadi seperti berikut:

![Pie Chart](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.7-PieChart.jpg)

**Membuat Bin**
Kali ini kita akan membuat **Bin** untuk melihat distribusi usia customer yang menggunakan jasa bank. Ketika kita menggunakan kolom usia untuk membuat visulisasi dan mengaturnya sebagai kategori maka data semua usia akan ditambilkan dalam bar chart. 

![Bar Chart](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.8-BarChart.jpg)

Gambar diatas memuat semua data usia mulai 18 tahun sampai 64 tahun. Tentu hal ini kurang efektif. Oleh karena itu kita bisa mengelompokkan datanya kedalam Bin.

Hanya kolom _measure_ yang bisa dibuat menjadi bin. Caranya:  
- klik kanan pada kolom _Age_  
- pilih **Create**  
- pilh **Bins**

Kemudian akan muncul prompt **Edit Bins**. Kali ini kita menentukan _Size of bins_ menjadi 5. Artinya data dikelompokkan kedalam 5 bagian (15–19, 20–24, 25–29, dst).

Setelah berhasil membuat bin, maka akan muncul kolom baru _Age (bin)_ dalam bentuk _dimention_. Kolom inilah yang akan kita gunakan untuk membuat visulisasi agar lebih mudah dipahami.

Buat beberapa perubahan pada Bar Chart untuk menambah informasi  
- ubah **Table Calculation** menjadi P**ercent of Total**  
- masukkan kolom C_ount_ pada color untuk melihat sebaran data

![Bin](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.11-Bin.jpg)

**Memanfaatkan Fitur Parameter**
Parameter merupakan pengembangan dari Bin. Dengan fitur Parameter kita bisa berinteraksi dengan mengubah-ubah jumlah Bin sesuai dengan kriteria yang telah ditentukan.

Setelah Parameter digunakan sebagai ukuran bin, maka kita bisa mengubah-ubah ukuran bin sesuai dengan nilai Parameter. Pada gambar pertama kita mengatur bin pada nilai 20.000, sedangkan pada gambar kedua kita mengatur bin pada nilai 10.000. Dari sini kita bisa melihat perbedaan dari keduanya.

![Bins20K](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.16-Bins20K.jpg)

![Bins10K](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.17-Bins10K.jpg)

Berikut contoh visulisasi yang menggunakan nilai paramaeter = 5.

![Age Bin](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.19-AgeBin.jpg)

**Membuat Tree Map**
Kali ini kita akan membuat Tree Map dengan memanfaatkan fitur **Show Me**.  
- letakkan kolom _Job Classification_ dan _Count_ pada working area  
- klik **Show Me**  
- pilih **Tree Map**

Sesuaikan visulisasi dengan mengubah warna, sesuaikan ukuran, dan menambahkan label.

![TreeMap](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.20-TreeMap.jpg)

**Advance Dashboard Interactivity**
Kita telah memiliki beberapa chart yang bisa digabungkan ke dalam dasboard.  Masukkan semua chart ke dashboard dan atur posisi agar sesuai dengan yang diinginkan. Berikut adalah dashboar yang berhasil kita buat:

![Dashboard](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.21-Dashboard.jpg)

Dari dashboard diatas kita bisa mengambil beberapa insight, diantaranya:  
- Urutan customer dari yang paling banyak: England, Scotland, Wales, Northern Ireland  
- Balance paling banyak antara 0–30K  
- Customer paling banyak diusia 30an  
- Job Clasificassion paling banyak White Collar

**Membuat Storyline**
Hasil analisis serta insight yang didapat dari dashboard bisa kita buat menjadi visulisasi berupa **Story**. Kali ini kita akan menggabungkan dashboard awal sebagai baseline, kemudian menambahkan insight yang didapat pada masing-masing region.

Pada bagian bawah Tableau terdapat pilihan untuk menambahkan **Story**. Kita bisa memasukkan worksheet dan dashboard kedalam **Story**. Namun kita tidak bisa menambahkan lebih dari satu worksheet seperti pada dashboard. **Story** bisa memiliki beberapa halaman, tetapi satu halaman hanya bisa diisi dengan satu visualisasi. Kelebihan **Story** adalah terdapat caption pada bagian atas untuk memberi judul atau memberi keterangan pada visualisasi yang ditampilkan.

![Storyline](https://github.com/ahmadilhamhabibi/Tableau-for-Data-Science/blob/main/images/6.29-Storyline.jpg)

[Storyline on My Tableau Public](https://public.tableau.com/app/profile/ahmad.ilham.habibi/viz/Recreate-StoryoftheBankCustomer/Storyline)
