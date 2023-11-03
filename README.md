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
 



3. Mengubah  method static void main sehingga bentuk tree seperti Gambar 4.4 dapat dibentuk. Kemudian menentukan bagaimana algoritma BFS dapat menemukan node 5.
4. Mengubah method static void main sehingga bentuk tree seperti Gambar 4.5 dapat dibentuk. Kemudian tentukan bagaimana algoritma BFS dapat menemukan node 9.
5. Mengubah kode program di atas sehingga bentuk tree seperti Gambar 6 dapat dibentuk. Kemudian menentukan bagaimana algoritma BFS dapat menemukan node C.

