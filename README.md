# Walletconnect
Wallet connect
def sapa(nama):
  """Fungsi ini menyapa seseorang dengan pesan selamat datang."""
  print(f"Halo, {nama}! Selamat datang di Wallet Connect.")

def tampilkan_saldo(saldo):
  """Fungsi ini menampilkan saldo dompet."""
  print(f"Saldo Anda saat ini adalah: Rp {saldo:,.2f}")

def tambah_saldo(saldo_awal, jumlah):
  """Fungsi ini menambahkan sejumlah uang ke saldo."""
  saldo_baru = saldo_awal + jumlah
  print(f"Menambahkan Rp {jumlah:,.2f} ke saldo.")
  return saldo_baru

def kurangi_saldo(saldo_awal, jumlah):
  """Fungsi ini mengurangi sejumlah uang dari saldo."""
  if jumlah > saldo_awal:
    print("Maaf, saldo Anda tidak mencukupi.")
    return saldo_awal
  else:
    saldo_baru = saldo_awal - jumlah
    print(f"Mengurangi Rp {jumlah:,.2f} dari saldo.")
    return saldo_baru

if __name__ == "__main__":
  nama_pengguna = input("Masukkan nama Anda: ")
  sapa(nama_pengguna)

  saldo_dompet = 1000000.00
  tampilkan_saldo(saldo_dompet)

  print("\n--- Transaksi ---")
  saldo_dompet = tambah_saldo(saldo_dompet, 500000.00)
  tampilkan_saldo(saldo_dompet)

  saldo_dompet = kurangi_saldo(saldo_dompet, 250000.00)
  tampilkan_saldo(saldo_dompet)

  saldo_dompet = kurangi_saldo(saldo_dompet, 2000000.00)
  tampilkan_saldo(saldo_dompet)
