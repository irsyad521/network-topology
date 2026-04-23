# 🏢 Skenario Soal: Jaringan Gedung 2 Lantai

Sebuah perusahaan memiliki gedung dengan 2 lantai:

- **Lantai 1** → Divisi Admin & HR  
- **Lantai 2** → Divisi IT & Finance  

Jaringan menggunakan:
- 2 Router  
- 4 Switch  
- Beberapa PC di tiap divisi  

---

# 📊 Tabel Pembagian Jaringan

## 🔹 Lantai 1

| Divisi | VLAN | Network         | Gateway      | Switch | Jumlah PC |
|--------|------|----------------|--------------|--------|-----------|
| Admin  | 10   | 192.168.10.0/24 | 192.168.10.1 | S1     | 3         |
| HR     | 20   | 192.168.20.0/24 | 192.168.20.1 | S2     | 3         |

---

## 🔹 Lantai 2

| Divisi  | VLAN | Network         | Gateway      | Switch | Jumlah PC |
|---------|------|----------------|--------------|--------|-----------|
| IT      | 30   | 192.168.30.0/24 | 192.168.30.1 | S3     | 3         |
| Finance | 40   | 192.168.40.0/24 | 192.168.40.1 | S4     | 3         |

---

## 🔹 Antar Router

| Koneksi | Network       | IP R1      | IP R2      |
|--------|--------------|-----------|-----------|
| R1 ↔ R2 | 10.10.10.0/30 | 10.10.10.1 | 10.10.10.2 |

---

# 🧩 Struktur Perangkat

| Perangkat | Fungsi            |
|----------|-------------------|
| R1       | Router lantai 1   |
| R2       | Router lantai 2   |
| S1       | Switch Admin      |
| S2       | Switch HR         |
| S3       | Switch IT         |
| S4       | Switch Finance    |

---

# 📘 Soal (Tugas)

## 🎯 Konfigurasi Switching

1. Buat VLAN sesuai tabel  
2. Assign setiap port ke VLAN masing-masing  
3. Pastikan setiap PC berada di VLAN yang benar  

---

## 🎯 Konfigurasi Routing

1. Gunakan **router-on-a-stick** di masing-masing router  
2. Konfigurasi IP gateway tiap VLAN  
3. Hubungkan R1 dan R2  

---

## 🎯 Static Routing

1. Tambahkan static route antar router  
2. Pastikan semua network bisa saling akses  

---

## 🎯 Testing

1. PC Admin → PC IT (harus bisa ping)  
2. PC HR → PC Finance (harus bisa ping)  
3. PC dalam VLAN sama → harus bisa ping  

---

# ⚠️ Ketentuan Tambahan

- VLAN berbeda **tidak boleh komunikasi tanpa routing**  
- Semua komunikasi antar lantai harus melalui router  
- Gunakan subnet sesuai tabel  
- Gunakan kabel straight untuk PC → switch  

---

# 🧠 Tujuan Soal

Pejuang diharapkan memahami:

- VLAN segmentation  
- Inter-VLAN routing  
- Static routing antar router  
- Desain jaringan multi-lantai  

---

# 🎯 Tips

Agar hasil terlihat profesional:

- Tambahkan diagram topologi dari Packet Tracer  
- Sertakan screenshot hasil ping  
