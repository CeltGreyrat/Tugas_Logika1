# Tugas Logika Informatika
Program sederhana menghitung biaya pengiriman barang dengan perintah 
- Menghitung tambahan biaya pengiriman barang jika barang melebihi berat maksimal 5 Kg.
- Menghitung tambahan biaya pengiriman barang jika jarak pengiriman barang melebihi 10 Km.
- Menghitung total biaya jika pemesan memilih menggunakan jenis pengiriman express yang dikenakan biaya Rp. 20.000.
- Mengitung total biaya jika pemesan memiliki diskon member.

## Code Program
````python
print("Naufal Rafi Haryanto")
print ("312410118")
print ("TI.24.A1")

def hitung_biaya_pengiriman(berat, jarak, jenis_pengiriman, is_member):
    # Biaya dasar
    biaya = 10000

    #tambahan_biaya_berat 
    if berat > 5:
        biaya += 5000

    #Tambahan_jarak
    if jarak > 10:
        biaya += 8000
    
    #Tambahan_express
    if jenis_pengiriman.lower() == 'express':
        biaya += 20000

    #Diskon_member
    if is_member: 
        diskon = 0.1 * biaya
        biaya -= diskon
    else:
        biaya = biaya
        
    return biaya

def main():
    while True:
        print("\n=== Program Hitung Biaya Pengiriman ===")
        print("1. Hitung Biaya Pengiriman")
        print("2. Keluar")
        
        pilihan = input("Pilih menu (1/2): ")
        
        if pilihan == '1':
            # Input berat paket
            berat_paket = float(input("Masukkan berat paket (kg): "))
            
            # Input jarak pengiriman
            jarak_pengiriman = float(input("Masukkan jarak pengiriman (km): "))
            
            # Input jenis pengiriman
            jenis_pengiriman = input("Masukkan jenis pengiriman (biasa/express): ").strip().lower()
            
            # Input status keanggotaan
            is_member_input = input("Apakah Anda member? (ya/tidak): ").strip().lower()
            is_member = True if is_member_input == 'ya' else False
            
            # Hitung total biaya
            total_biaya = hitung_biaya_pengiriman(berat_paket, jarak_pengiriman, jenis_pengiriman, is_member)
            
            # Tampilkan hasil
            print(f'Total biaya pengiriman: Rp {total_biaya}')
        
        elif pilihan == '2':
            print("Terima kasih! Sampai jumpa.")
            break
        
        else:
            print("Pilihan tidak valid. Silakan pilih 1 atau 2.")

if __name__ == "__main__":
    main()
````

## Contoh Output
````
=== Program Hitung Biaya Pengiriman ===
1. Hitung Biaya Pengiriman
2. Keluar
Pilih menu (1/2): 1
Masukkan berat paket (kg): 10
Masukkan jarak pengiriman (km): 75
Masukkan jenis pengiriman (biasa/express): express
Apakah Anda member? (ya/tidak): ya
Total biaya pengiriman: Rp 38700.0

=== Program Hitung Biaya Pengiriman ===
1. Hitung Biaya Pengiriman
2. Keluar
Pilih menu (1/2): 1
Masukkan berat paket (kg): 4 
Masukkan berat paket (kg): 4
Masukkan jarak pengiriman (km): 8
Masukkan jarak pengiriman (km): 8
Masukkan jenis pengiriman (biasa/express): biasa
Masukkan jenis pengiriman (biasa/express): biasa
Apakah Anda member? (ya/tidak): ya
Total biaya pengiriman: Rp 9000.0
````
