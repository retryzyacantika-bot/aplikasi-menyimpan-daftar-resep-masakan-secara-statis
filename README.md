# --- Struktur Data Statis untuk Menyimpan Resep ---
RESEP_MASAKAN = [
    {
        "judul": "Nasi Goreng Sederhana",
        "bahan": [
            "2 piring nasi putih dingin",
            "2 butir telur",
            "3 siung bawang merah",
            "2 siung bawang putih",
            "1/2 sendok teh terasi",
            "1 sendok makan kecap manis",
            "Garam dan merica secukupnya",
            "Minyak goreng secukupnya"
        ],
        "instruksi": [
            "Haluskan bawang merah, bawang putih, dan terasi.",
            "Panaskan minyak, orak-arik telur hingga matang, sisihkan.",
            "Tumis bumbu halus hingga harum.",
            "Masukkan nasi, aduk rata.",
            "Tambahkan kecap manis, garam, dan merica. Aduk hingga semua tercampur dan nasi panas.",
            "Sajikan nasi goreng dengan telur orak-arik."
        ]
    },
    {
        "judul": "Sayur Asem Jakarta",
        "bahan": [
            "1 ikat kacang panjang",
            "1 buah labu siam",
            "1 genggam daun melinjo dan buahnya",
            "1/2 gelas melinjo",
            "2 liter air",
            "Bumbu: 4 siung bawang merah, 2 siung bawang putih, 1/2 sendok teh terasi, 1 ruas jari lengkuas, 2 lembar daun salam, 3 sendok makan asam jawa, gula dan garam secukupnya"
        ],
        "instruksi": [
            "Potong semua sayuran sesuai selera.",
            "Rebus air hingga mendidih. Masukkan bumbu halus (bawang merah, bawang putih, terasi) dan bumbu utuh (lengkuas, daun salam).",
            "Masukkan melinjo dan tunggu hingga agak empuk.",
            "Masukkan semua sayuran lainnya. Tambahkan asam jawa, gula, dan garam.",
            "Masak hingga semua sayuran matang. Koreksi rasa.",
            "Sajikan hangat."
        ]
    }
]

# --- Fungsi untuk Menampilkan Semua Resep ---
def tampilkan_semua_resep():
    """Menampilkan daftar semua resep yang tersimpan secara statis."""
    print("✨ **DAFTAR RESEP MASAKAN STATIS** ✨")
    print("-" * 40)

    if not RESEP_MASAKAN:
        print("Belum ada resep yang tersimpan.")
        return

    for i, resep in enumerate(RESEP_MASAKAN):
        print(f"## 🍽️ {i+1}. {resep['judul'].upper()} ##")
        
        # Bahan
        print("\n**Bahan-bahan:**")
        for bahan in resep['bahan']:
            print(f"* {bahan}")
            
        # Instruksi
        print("\n**Langkah-langkah:**")
        for j, langkah in enumerate(resep['instruksi']):
            print(f"{j+1}. {langkah}")
            
        print("\n" + "=" * 40)

# --- Menjalankan Aplikasi ---
if __name__ == "__main__":
    tampilkan_semua_resep()
