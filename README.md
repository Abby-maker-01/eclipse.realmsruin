# ECLIPSE: REALMS OF RUIN — Prototype V2

Aplikasi RPG top-down bergaya pixel untuk prototipe Android (Capacitor) dan browser. Build ini menambahkan tata letak kontrol tempur yang lebih cocok untuk landscape, dua skill, HP monster, animasi hit sederhana, partikel serangan, dan efek suara sintetis tanpa berkas audio eksternal.

## Menjalankan
Buka `index.html` di browser modern atau unggah proyek ke GitHub dan jalankan workflow `.github/workflows/build-apk.yml` untuk membuat APK debug. Untuk rilis Google Play, perlu menyiapkan build release/AAB, signing, target API, serta memeriksa kebijakan terbaru.

## Sudah ada dalam prototipe
- Peta top-down bergaya pixel dan perpindahan dengan tombol sentuh/keyboard.
- Beberapa wilayah konsep, ras, class, level/EXP, rank, statistik, inventaris, equipment, crafting, pasar, loot, dan quest sederhana.
- Kontrol Serang, Skill I, Skill II; HP monster, damage, efek partikel, hit reaction sederhana, monster respawn prototipe.
- Efek audio sintetis lokal: ayunan, hit, skill, ultimate, monster kalah, karakter terluka, langkah, dan aksi ditolak.
- Layout yang lebih ringkas untuk layar landscape.
- Penyimpanan progres lokal di browser perangkat.

## Catatan audio
Audio dibuat secara sintetis menggunakan Web Audio API agar prototipe tidak memerlukan file musik pihak ketiga. Ini **belum** merupakan soundtrack final atau sistem musik dinamis per wilayah. Pemutaran suara memerlukan interaksi pertama pemain pada browser/perangkat. Musik latar belum otomatis menyala; audio harus diaktifkan secara eksplisit setelah gesture pengguna. File audio berlisensi/orisinal dapat ditambahkan pada tahap produksi.

## Rencana fitur yang sudah kita sepakati
Rencana produk (belum berarti sudah terimplementasi):
- Character creator: gender, skin, rambut, wajah, pakaian, kelas; nama akun dan nama karakter unik.
- Kelas Warrior, Assassin, Mage, Archer dengan skill khusus; class terkunci setelah pembuatan karakter kecuali sistem perubahan kelas yang dirancang secara resmi.
- Animasi lengkap monster Idle/Walk/Attack/Hurt/Die, AI pengejaran dan serangan, loot, beberapa titik spawn.
- Dunia: Verdant Reach, Frostveil Highlands, Ashen Wastes, Obsidian Dominion, Abyssal Frontier.
- NPC Eldric, Brom, Mira, Seren, Vaelis, Orin; tutorial “The First Awakening” (3 Slime, 2 bahan, hadiah EXP/Gold/potion).
- Quest, inventory, crafting, enhancement, durability bila diimplementasikan, trading dengan konfirmasi, party, guild, whisper, global/proximity/system chat.
- Achievement/title Common/Rare/Epic/Legendary/Mythic; secret quests dan leaderboard; validasi syarat oleh server.
- Founder title `THE LAST BOSS`, terkunci ke akun Founder yang diverifikasi server, efek gerhana; tidak bisa didapat lewat loot/quest/command biasa.
- Developer tools dan event commands yang hanya bisa dipakai akun berizin, dengan audit log.
- Eclipse Crystal, toko kosmetik, item bantuan yang tidak merusak keseimbangan, top-up setelah backend dan verifikasi pembayaran siap.
- Respawn normal 5–10 detik, elite 30–60 detik, regional boss 5–10 menit, world boss 30–60 menit; harus dikendalikan server untuk multiplayer.
- Server WebSocket, akun dan progres server-side, PostgreSQL, anti-cheat, kapasitas target awal 30–50 pemain, lalu uji beban.

## Batasan penting
Build ini **belum merupakan MMORPG online**. Tidak ada server multiplayer aktif, akun/login server, penyimpanan server, chat online, party/guild, perdagangan antarpemain, pembayaran/top-up, atau otorisasi Founder yang benar-benar aman. Data game masih lokal dan dapat diubah dari perangkat. AI monster dan efek visual masih prototipe sederhana; belum menggunakan sprite sheet final. Soundtrack final belum tersedia. Jangan gunakan ekonomi atau item lokal sebagai sistem produksi sebelum otoritas dipindahkan ke backend.

Gunakan aset buatan sendiri atau aset yang lisensinya mengizinkan distribusi komersial sebelum rilis publik.
