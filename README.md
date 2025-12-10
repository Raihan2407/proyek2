# Hypervisor Mini Project — QEMU/KVM & Libvirt  
Mata Kuliah: **Sistem Operasi**  
Dosen Pengampu: **(TULISKAN NAMA DOSEN DI SINI)**  

---

## 📘 Deskripsi Proyek  
Proyek ini merupakan implementasi simulasi virtualisasi menggunakan **QEMU**, **KVM**, **libvirt**, dan **virt-manager**.  
Tujuan dari proyek ini adalah membangun **hypervisor mini** yang dapat menjalankan 1–2 virtual machine (VM), melakukan pengaturan CPU/memori, serta menjalankan benchmark untuk menganalisis performa antar VM.

Proyek ini berlangsung dalam 5 tahap (minggu ke-11 hingga minggu ke-15), meliputi penyusunan proposal, instalasi tools virtualisasi, pembuatan VM, benchmarking performa, hingga penyusunan laporan akhir.

---

## 🎯 Tujuan Proyek  

1. Mempelajari konsep virtualisasi pada tingkat sistem operasi.  
2. Menginstal dan mengonfigurasi QEMU, libvirt, dan virt-manager sebagai environment hypervisor mini.  
3. Membangun dan menjalankan 1–2 VM secara stabil.  
4. Mengelola alokasi CPU dan RAM pada VM.  
5. Melakukan benchmarking CPU dan memori.  
6. Membuat analisis performa berdasarkan hasil pengujian.

---

## 🧩 Ruang Lingkup Proyek  

Proyek ini mencakup:  
- Instalasi QEMU, libvirt, dan virt-manager  
- Pembuatan dan konfigurasi virtual machine  
- Uji performa CPU dan memori menggunakan Sysbench  
- Dokumentasi progres mingguan  
- Penyusunan laporan akhir

**Catatan Penting:**  
Lingkungan pengembangan dijalankan pada **VirtualBox**, sehingga modul akselerasi hardware **KVM** tidak tersedia (`/dev/kvm` tidak dapat digunakan).  
Meskipun demikian, seluruh fungsi virtualisasi tetap berjalan menggunakan **QEMU software virtualization**, dan proyek tetap valid sesuai kebutuhan mata kuliah.

---

## 📂 Struktur Folder Repository  


---

## 🧪 Teknologi yang Digunakan  

- **QEMU**  
- **KVM** (opsional, tidak aktif pada VirtualBox)  
- **Libvirt**  
- **Virt-Manager**  
- **Sysbench** (benchmark CPU & memori)  
- **Linux Ubuntu**

---

## 📊 Hasil & Output Proyek  

- Dua VM berhasil dibuat dan berjalan stabil.  
- Pengaturan CPU/RAM dilakukan sesuai kebutuhan percobaan.  
- Benchmark CPU & memori telah dijalankan menggunakan Sysbench.  
- Laporan progres tersedia pada setiap minggu.  
- Laporan akhir mencakup analisis performa VM dan kesimpulan proyek.

---

## 👥 **Anggota Kelompok**

1. **Raihan Darma Putra** — 2401020138  
2. **Muhammad Alfikar** — 2401020145  
3. **Muhammad Bagas Risllah** — 2401020146  
4. **Muhammad Harist** — 2401020149  
5. **Muhammad Dimaz Al Bintani** — 2401020159  

---

## ⚠ Catatan Kompatibilitas  
Proyek dijalankan dalam **VirtualBox**, sehingga:  
- Fitur *hardware virtualization* (KVM) tidak tersedia  
- QEMU berjalan sepenuhnya dalam mode software virtualization  
- Hal ini **tidak mengganggu fungsi proyek** sesuai kebutuhan mata kuliah

---

## 📄 Lisensi  
Repositori ini bersifat publik dan digunakan untuk memenuhi tugas mata kuliah **Sistem Operasi**.

