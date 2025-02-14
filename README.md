Nama : Devandra Reswara Arkananta

NPM : 2206083552

## Tutorial 2 - Introduction to Game Engine
### Latihan: Playtest
* Apa saja pesan log yang dicetak pada panel Output?

    Jawab : yang dicetak pada output adalah "Reached objective!"
    
* Coba gerakkan landasan ke batas area bawah, lalu gerakkan kembali ke atas hingga hampir menyentuh batas atas. Apa saja pesan log yang dicetak pada panel Output?

    Jawab : yang dicetak pada output adalah "Reached objective!"
    
* Buka scene MainLevel dengan tampilan workspace 2D. Apakah lokasi scene ObjectiveArea memiliki kaitan dengan pesan log yang dicetak pada panel Output pada percobaan sebelumnya?

    Jawab : ada kaitannya karena ada CollisionShape2D pada ObjectiveArea, jadi mungkin saat platform melewati collision shape ini maka pesan akan dicetak pada log

### Latihan: Memanipulasi Node dan Scene
* Scene BlueShip dan StonePlatform sama-sama memiliki sebuah child node bertipe Sprite. Apa fungsi dari node bertipe Sprite? 

    Jawab : fungsi dari Sprite node adalah untuk menampilkan tekstur 2D, Tekstur yang ditampilkan dapat berupa region dari tekstur atlas yang lebih besar, atau frame dari animasi sprite sheet.
    
* Root node dari scene BlueShip dan StonePlatform menggunakan tipe yang berbeda. BlueShip menggunakan tipe RigidBody2D, sedangkan StonePlatform menggunakan tipe StaticBody2D. Apa perbedaan dari masing-masing tipe node?

    Jawab : RigidBody2D mengimplementasikan 2D physics, jadi tidak bisa dikontrol secara langsung, namun harus mengaplikasikan gaya seperti gravitasi atau impuls lalu simulasi physics akan menghitung pergerakan, rotasi, reaksi dan efek ke benda lain. Sementara itu, StaticBody2D tidak dapat digerakkan atau diubah oleh kontak eksternal, namun bisa digerakkan manual melalui kode. saat StaticBody2D digerakkan, langsung diteleportasi ke posisi baru tanpa memengaruhi benda lain di sekitarnya.
    
* Ubah nilai atribut Mass pada tipe RigidBody2D secara bebas di scene BlueShip, lalu coba jalankan scene MainLevel. Apa yang terjadi?

    Jawab : Tidak ada hal berbeda yang terjadi, karena tidak ada atribut gesekan udara, jadi kecepatan jatuhya tetap sama maupun 1 kg atau 10000 kg, lalu karena platform adalah StaticBody2D, jadi saat mendorong BlueShip keatas, tidak ada perbedaan sama sekali karena physics tidak berlaku untuk platform.
    
* Ubah nilai atribut Disabled pada tipe CollisionShape2D di scene StonePlatform, lalu coba jalankan scene MainLevel. Apa yang terjadi?

    Jawab : Blueship langsung jatuh kebawah, karena collision shape disabled, jadi tidak bersentuhan dengan platform dibawahnya.
    
* Pada scene MainLevel, coba manipulasi atribut Position, Rotation, dan Scale milik node BlueShip secara bebas. Apa yang terjadi pada visualisasi BlueShip di Viewport?

    Jawab : Jika kita mengubah position, maka koordinat awal atau posisi BlueShip akan berubah, lalu jika Rotation diubah, maka BlueShip akan diputar sesuai sudutnya. Dan, Scale mengubah ukuran dari BlueShip.
    
* Pada scene MainLevel, perhatikan nilai atribut Position node PlatformBlue, StonePlatform, dan StonePlatform2. Mengapa nilai Position node StonePlatform dan StonePlatform2 tidak sesuai dengan posisinya di dalam scene (menurut Inspector) namun visualisasinya berada di posisi yang tepat?

    Jawab : Itu karena nilai posisi di dalam inspector adalah relatif terhadap node parentnya, jadi karena pas di dalam PlatformBlue, posisi StonePlatform adalah (0,0), lalu StonePlatform2 posisinya (70,0) karena posisinya berada tepat di sebelah StonePlatform.
