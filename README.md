# StrukturData-Q1-2501010021-I-Gusti-Ngurah-Ketut-Puja-Bagus-Permana-A

1.Array dapat melakukan akses elemen dalam waktu O(1) karena array disimpan di memori yang kontinu (contiguous memory). Setiap elemen memiliki ukuran tetap, sehingga alamat elemen ke-i bisa dihitung langsung.

Artinya, CPU tidak perlu menelusuri elemen satu per satu—langsung lompat ke alamat yang dituju.

Sebaliknya, Singly Linked List disimpan di memori yang tidak kontinu (non-contiguous). Setiap node berisi data + pointer ke node berikutnya. Untuk mengakses elemen ke-i, kita harus mulai dari head lalu mengikuti pointer satu per satu sampai posisi yang dituju, sehingga kompleksitasnya O(n).


2. Linked List lebih unggul dibanding Array untuk operasi insert dan delete ketika:

Operasi sering terjadi di awal (head) atau tengah list
Posisi node sudah diketahui (punya pointer/reference ke node tersebut)

Alasannya:

Linked List tidak memerlukan pergeseran elemen seperti array
Insert/delete cukup mengubah pointer (relasi antar node)


3. Struktur node Doubly Linked List:

Setiap node memiliki tiga bagian:

data
prev → pointer ke node sebelumnya
next → pointer ke node berikutnya

Kelebihan:
Bisa traversal dua arah (maju dan mundur)
Delete node lebih efisien (tidak selalu perlu mencari predecessor)
Lebih fleksibel untuk operasi navigasi

Kekurangan:
Membutuhkan memori lebih besar (karena ada tambahan pointer prev)
Insert/delete sedikit lebih kompleks karena harus update dua pointer


4. Perbedaan utama dengan Linked List biasa:

Linked List biasa: node terakhir menunjuk ke NULL
Circular Linked List: node terakhir menunjuk kembali ke head, membentuk siklus

Artinya, tidak ada ujung list secara logis.

Contoh use case:

Round-robin scheduling pada sistem operasi

Kenapa cocok?

Setelah mencapai akhir, proses langsung kembali ke awal tanpa reset pointer
Efisien untuk sistem yang membutuhkan giliran berulang secara terus-menerus


5. Awalnya list dialokasikan dengan kapasitas lebih besar dari ukuran saat ini (over-allocation)

Saat kapasitas penuh dan append dilakukan:
Python membuat array baru dengan ukuran lebih besar (biasanya bertambah secara geometris)
bukan sekadar +1, tapi sekitar kelipatan tertentu

Elemen lama disalin ke array baru

Memori lama dilepas

Elemen baru ditambahkan ke array baru



