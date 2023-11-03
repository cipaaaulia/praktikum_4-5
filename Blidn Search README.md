# Praktikum_4 Teknik Pencarian Blind search
Andi Siti Syifa Aulia

5311421109

Tujuan Praktikum


Mampu memahami konsep blind search dan dapat mengimplementasikan program salah satu algoritma blind search pada kasus tree.


1. Menentukan bagaimana algoritma BFS di atas dapat menentukan node ke 8, 6, dan 7.
   Algoritma BFS (Breadth-First Search) pada kode di atas digunakan untuk menjelajahi graf yang direpresentasikan dalam bentuk adjacency list. Untuk menentukan bagaimana algoritma BFS menemukan node 8, 6, dan 7, mari kita periksa langkah-langkahnya:
   1. Algoritma BFS dimulai dengan node awal, yang dalam kasus ini adalah node n3. Pada awalnya, semua node dalam graf diberi warna putih (WHITE) dan jarak (distance) yang sangat besar (Integer.MAX_VALUE) kecuali node awal n3.
   2. Node n3 diberi warna abu-abu (GRAY) karena itu adalah node awal yang sedang diproses, dan jaraknya diatur menjadi 0. Ini menunjukkan bahwa node n3 adalah titik awal pencarian.
   3. Node n3 dimasukkan ke dalam antrian (queue) q.
   4. Selama antrian q tidak kosong, algoritma BFS akan terus berjalan. Pada setiap iterasi, algoritma mengambil node u dari antrian q.
   5. Kemudian, algoritma mengambil semua tetangga (adjacents) dari node u yang belum pernah dikunjungi (berwarna putih). Jika tetangga tersebut belum pernah dikunjungi, maka tetangga tersebut diubah warnanya menjadi abu-abu (GRAY), jaraknya diperbarui dengan jarak node u ditambah satu, dan node u dijadikan sebagai pendahulu tetangga tersebut.
   6. Node u akhirnya diberi warna hitam (BLACK) setelah semua tetangga telah diproses.
   7. Hasil dari algoritma BFS adalah pencarian yang meluas dari node awal n3 ke seluruh bagian graf yang terhubung dengan n3. Algoritma ini akan mengunjungi semua node yang dapat dijangkau dari n3 dalam urutan yang lebih dalam terlebih dahulu (level per level).

Ketika algoritma BFS selesai, Anda akan dapat menemukan node 8, 6, dan 7 dengan cara berikut:
1. Node 8: Node ini terhubung ke node 6 melalui satu langkah (edge) langsung. Jadi, node 8 berada dalam level yang lebih dalam dari node 6. Algoritma BFS akan menemukan node 8 setelah semua node dalam level yang lebih dekat (termasuk 6) telah diproses.
2. Node 6: Node ini berada dalam level yang lebih dekat dari node 8. Oleh karena itu, algoritma BFS akan menemukan node 6 sebelum node 8 dalam proses pencarian, karena node 6 adalah salah satu tetangga dari node 3 yang berwarna abu-abu saat pertama kali dimasukkan ke dalam antrian.
3. Node 7: Node ini juga terletak di level yang lebih dalam dari node 3, dan karena itu, algoritma BFS akan menemukan node 7 setelah node 6. Node 7 juga merupakan salah satu tetangga dari node 6 yang berwarna abu-abu saat pertama kali dimasukkan ke dalam antrian.

Dengan demikian, algoritma BFS akan menemukan node 8, 6, dan 7 secara berurutan sesuai dengan level kedekatan mereka dengan node awal n3 dalam graf yang direpresentasikan dalam kode di atas.

![ai 1](https://github.com/cipaaaulia/ai-1/blob/a4ac139f20adc9841f86badc0b1756c5c294132b/ai%201.png)

2. Mengubah  method static void main sehingga bentuk tree seperti Gambar 4.4 dapat dibentuk. Kemudian menentukan bagaimana algoritma BFS dapat menemukan node 5.
   ![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/b56db695-78fb-43fe-a19b-5bd76ec89252)
   1. Algoritma BFS dimulai dengan memasukkan node awal (dalam kasus ini, node 1) ke dalam antrian atau queue.
   2. Node 1 adalah node awal dan akan mulai mengeksplorasi node-node yang langsung terhubung dengannya, yaitu node 2 dan node 3, yang berada pada kedalaman tingkat 1.
   3. Selanjutnya, node 3 akan melanjutkan dengan mengeksplorasi node-node yang memiliki jarak atau kedalaman 2. Ini berarti node 3 akan memeriksa node-node seperti node 4, node 5, node 6, dan node 7.
   4. Algoritma BFS akan terus berlanjut hingga semua node yang terhubung dengan node awal telah diperiksa. Oleh karena itu, node 5 akan ditemukan dan diproses sesuai dengan aturan algoritma BFS.
![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/a2083187-825b-4f85-94e6-2405d511e6ac)

3. Mengubah method static void main sehingga bentuk tree seperti Gambar 4.5 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node 9.
   ![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/962c2757-e336-453f-b2af-139ec55607fe)
   1. Membuat objek AdjacencyList yang mewakili graf. Selanjutnya, kami membuat node-node dengan nomor sesuai dengan gambar tree yang diinginkan. Node-node ini adalah simpul-simpul dalam struktur tree.
   2. Menambahkan edge (hubungan) antara node-node agar sesuai dengan struktur tree yang diinginkan. Pada contoh di atas, node 1 adalah root (akar) tree, dan menambahkan anak-anak dan cucu sesuai dengan hubungan parent-child yang ditunjukkan dalam gambar tree.
   3. Kemudian, kami menjalankan algoritma BFS dari node 1 (root) dengan memanggil
![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/84cfc634-5eb5-43ab-8c11-895ccf1eac44)
Hasil BFS traversal adalah sebagai berikut:
![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/4794b45e-8e76-4bc4-914c-bc823be255d4)
   4. Penjelasan tentang hasil BFS:
      Algoritma BFS dimulai dari node 1 (root) dengan jarak (distance) 0.
      1. Node 1 (d=0) mengeksplorasi node 2 (d=1) dan node 3 (d=1) yang langsung terhubung.
      2. Node 2 (d=1) mengeksplorasi node 4 (d=2) dan node 5 (d=2).
      3. Node 3 (d=1) mengeksplorasi node 7 (d=2) dan node 8 (d=2).
      4. Node 8 (d=2) kemudian mengeksplorasi node 9 (d=3) karena node 9 adalah anak dari node
Dengan demikian, algoritma BFS menemukan node 9 dengan jarak 3 dari node 1 sesuai dengan hasil yang diberikan. Node-node lain juga ditampilkan dalam urutan traversal BFS.
   
5. Mengubah kode program di atas sehingga bentuk tree seperti Gambar 6 dapat dibentuk. Kemudian menentukan bagaimana algoritma BFS dapat menemukan node C.
   Untuk membentuk tree seperti Gambar 6 dan menjalankan algoritma BFS untuk menemukan node C, Anda perlu mengubah struktur tree dan kode program. Gambar 6 adalah contoh tree yang lebih kompleks dibandingkan dengan yang sebelumnya. 
   ![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/2619d4c2-5063-42e2-842e-f2b9de393563)
   1. Algoritma BFS dimulai dengan memasukkan node 6 (F) ke dalam antrian.
   2. Node 6 akan mengeksplorasi node 2 (B) dan node 7 (G), yang terhubung langsung dengan node 6 atau memiliki kedalaman tingkat 1.
   3. Selanjutnya, node 7 akan memeriksa node yang memiliki kedalaman 2, dimulai dari pemeriksaan node 1 (A), node 4 (D), dan node 9 (I).
   4. Node 9 akan memeriksa node 3 (C). Setelah menemukan node 3 (C), proses akan terus berlanjut untuk memeriksa node 5 (E) dan node 8 (H) hingga semua node yang terhubung dengan node awal telah diperiksa.
   5. Hasil BFS traversal dimulai dari node 6 adalah sebagai berikut:
![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/032aa220-6f14-40ac-aa99-2f70ab3ae8df)
