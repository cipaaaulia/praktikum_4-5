# Praktikum_5_Heuristic search
Andi Siti Syifa Aulia


5311421109


Tujuan Praktikum


Mampu menyelesaikan permasalahan pada game 8-puzzle dengan menggunakan algoritma heuristic search serta mampu mengimplementasikan algoritma heuristic menggunakan java

1. Mempelajari  class EightPuzzleSearch, EightPuzzleSpace, dan Node.
     **Kelas `Node`**:
   - Kelas `Node` digunakan untuk merepresentasikan keadaan dalam ruang keadaan papan puzzle delapan ubin. Setiap objek `Node` menyimpan informasi tentang keadaan papan, biaya saat ini, simpul induk, dan daftar simpul keturunan.
   - Konstruktor `__init__` menginisialisasi atribut-atribut:
     - `state`: Array yang merepresentasikan keadaan papan. Di sini, angka 0 menandakan ubin kosong.
     - `cost`: Biaya saat ini (dapat berupa biaya g(n), h(n), atau f(n) dalam algoritma A*).
     - `parent`: Simpul induk yang mengarahkan ke simpul saat ini dalam pencarian.
     - `successors`: Daftar simpul keturunan yang dapat dicapai dari simpul saat ini.
   - Metode `__str__` digunakan untuk mengonversi keadaan (papan) menjadi string yang dapat dicetak.
   - Metode `__eq__` membandingkan dua objek `Node` dan mengembalikan True jika keadaan (papan) keduanya sama.
     **Kelas `EightPuzzleSearch`**:
   - Kelas `EightPuzzleSearch` mengelola proses pencarian solusi untuk papan puzzle delapan ubin menggunakan algoritma A*.
   - Metode `EightPuzzleSpace` adalah bagian dari kelas ini dan digunakan untuk mengatur ruang keadaan papan puzzle. Ini mencakup metode untuk mendapatkan keadaan awal, keadaan tujuan, dan daftar keturunan dari suatu simpul.
   - Metode `h1_cost` dan `h2_cost` menghitung biaya heuristik dengan metode Manhattan Distance (h1) atau jumlah perbedaan (h2) antara keadaan saat ini dan tujuan.
   - Metode `h_cost` memilih metode heuristik yang akan digunakan untuk menghitung biaya heuristik.
   - Metode `get_best_node` digunakan untuk mendapatkan simpul dengan biaya terkecil dari daftar simpul yang tersedia.
   - Metode `get_previous_cost` mengembalikan biaya dari simpul yang telah dihitung sebelumnya.
   - Metode `print_path` mencetak jalur solusi.
   - Metode `run` menginisialisasi pencarian, menemukan solusi, dan mencetak jalur solusi.

   **Kelas `EightPuzzleSpace`**:
   - Kelas `EightPuzzleSpace` mengatur ruang keadaan papan puzzle delapan ubin. Ini mencakup metode-metode berikut:
     - `get_root`: Mengembalikan keadaan awal papan puzzle.
     - `get_goal`: Mengembalikan keadaan tujuan papan puzzle.
     - `get_successors`: Mengembalikan daftar simpul keturunan yang dapat dicapai dari suatu simpul.
     - `transform_state`: Metode yang digunakan untuk mengubah keadaan papan saat memindahkan ubin.

Kelas `EightPuzzleSearch` menggunakan kelas `Node` dan `EightPuzzleSpace` untuk melakukan pencarian solusi dalam papan puzzle delapan ubin. Kode ini mengikuti algoritma A* dengan metode heuristik yang dapat dipilih (h1 atau h2) untuk menghitung biaya. Hasil pencarian solusi ditampilkan melalui metode `print_path`.
![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/52394041-8c78-42dc-a0b3-de3bbc6e6f16)
![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/68d25d0e-eb3d-4b43-b34b-d9c2e083df10)
Hasil program
![image](https://github.com/cipaaaulia/praktikum_4-5/assets/149106143/895cbb54-1ebc-4403-a326-845c6800c3d3)
Dimana:


Situasi Awal: Papan puzzle terdiri dari sembilan ubin yang disusun dalam matriks 3x3. Ubin dengan angka 0 berfungsi sebagai ubin kosong yang dapat dipindahkan ke atas, bawah, kiri, atau kanan untuk mencapai tujuan.

Langkah 1: Pada tahap pertama, ubin kosong dipindahkan dari posisi (3,3) ke posisi (2,3).

Langkah 2: Selanjutnya, ubin kosong dipindahkan dari posisi (2,3) ke posisi (2,2).

Langkah 3: Ubin kosong dipindahkan dari posisi (2,2) ke posisi (1,2).

Langkah 4 (Tujuan Terpenuhi): Pada langkah terakhir, ubin kosong dipindahkan dari posisi (1,2) ke posisi (1,1).

Dengan urutan langkah-langkah ini, ubin kosong berhasil diposisikan dengan benar untuk mencapai tujuan.


2. Mengubah initial dan goal state dari program di atas sehingga bentuk initial dan goal statenya Gambar 8. Kemudian tentukan langkah-langkah mana saja sehingga puzzlenya mencapai goal state. Analisa dan bedakan dengan solusi pada point 1.

