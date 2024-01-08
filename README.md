# UAS MEMBUAT PROGRAM KASIR
# Zaky Putra Pratama
# 312310613
# penjelasan video
[klik link youtube disini](https://youtu.be/m2jADOWv7GI)
# program
![gambar](dokumentasi/zeeky.png)
## output
![gambar](dokumentasi/ss.png)

```python
# menu dictionary
menu = {
   'mie goreng': 7_000,
   'mie rebus': 7_000,
   'nasi goreng': 13_000,
   'ayam geprek': 15_000,
   'es teh': 5_000,
   'es jeruk': 5_000,
   'air mineral': 3_000,
}
# looping untuk pemesanan baru
while True:
    pilihan = []
    total = 0
    # untuk menampilkan daftar menu makanan dan minuman
    print("\n[SELAMAT DATANG DI WARUNG ZEEKY]")
    print("\nMenu Makanan dan Minuman:")
    print("=" *26)
    for item, harga in menu.items():
        print(f"{item:<13} : Rp {harga:>7,}")
        
    # perintah untuk berhenti
    print("\n[ketik (ok) untuk selesai yah]")
    
    # looping pesanan memilih menu
    while True:
        pesanan = input("Masukan Pesanan: ")
        if pesanan.lower() == 'ok':
            break
        elif pesanan in menu:
            pilihan.append(pesanan)
            total += menu[pesanan]
        else:
            print("[Maaf, menu tidak ada]")
            
    # untuk memasukan nominal pembayaran
    uang = int(input("\nUang Pembayaran: Rp "))
    kembalian = uang - total
    
    # struk pembayaran    
    print("\n===== STRUK PEMBELIAN =====")
    for item in pilihan:
        print(f"{item:<13} = Rp {menu[item]:>7,}")
    print("-" *27)
    print(f"Total Harga   = Rp {total:>7,}")
    print("-" *27)
    print(f"Uang Bayar    = Rp {uang:>7,}")
    print(f"Kembalian     = Rp {kembalian:>7,}")
    print("-" * 27)
    print("Terima Kasih Guys :)")
    print("=" * 27)
    
    ulangi = input("\nPesanan Baru? (yes/no): ")
    if ulangi.lower() != 'yes':
            break
```
### link youtube cadangan
https://youtu.be/m2jADOWv7GI
