# Hypervisor Mini menggunakan QEMU/KVM dan Libvirt

![Status](https://img.shields.io/badge/status-completed-success)
![Platform](https://img.shields.io/badge/platform-Linux-blue)
![License](https://img.shields.io/badge/license-MIT-green)

> **Proyek Tugas Akhir Mata Kuliah Sistem Operasi**  
> Program Studi Teknik Informatika  
> Universitas Maritim Raja Ali Haji  
> Semester Ganjil 2024/2025

---

## 📋 Deskripsi Proyek

Proyek ini merupakan implementasi **hypervisor mini** menggunakan teknologi **QEMU/KVM** dan **libvirt** untuk memahami konsep virtualisasi di level sistem operasi. Proyek mencakup pembangunan, konfigurasi, dan evaluasi performa virtual machine melalui metodologi benchmarking yang sistematis.

**Tujuan Utama:**
- 🎯 Memahami arsitektur virtualisasi dan hypervisor
- 🎯 Membangun VM yang stabil menggunakan QEMU/libvirt
- 🎯 Melakukan resource management (CPU, Memory)
- 🎯 Menganalisis performa melalui benchmarking

---

## 👥 Tim Pengembang

| Nama | NPM |
|------|-----|
| Raihan Darma Putra | 2401020138 |
| Muhammad Alfikar | 2401020145 |
| Muhammad Bagas Risllah | 2401020146 |
| Muhammad Harist Syafi'in | 2401020149 |
| Muhammad Dimaz Al Bintani | 2401020159 |

**Dosen Pengampu:** Ferdi Chahyadi, S.Kom., M.Cs

---

## 🛠️ Teknologi yang Digunakan

### **Virtualization Stack**
- **QEMU** - Emulator dan virtualizer
- **Libvirt** - API manajemen virtualisasi
- **Virt-Manager** - GUI management tool
- **Bridge-utils** - Network configuration

### **Operating Systems**
- **Host:** Ubuntu Linux (running on VirtualBox)
- **Guest:** Ubuntu Server 20.04 LTS

### **Benchmarking Tools**
- **Sysbench** - CPU dan Memory benchmark

### **Environment**
- Nested Virtualization: Windows → VirtualBox → Ubuntu → QEMU
- Software Virtualization (TCG backend)

---

## 🏗️ Spesifikasi Virtual Machine

| Komponen | Spesifikasi |
|----------|-------------|
| **vCPU** | 2 cores |
| **Memory** | 2900 MB (~3 GB) |
| **Storage** | 10 GB (qcow2) |
| **Network** | NAT (192.168.122.0/24) |
| **Hypervisor** | QEMU (TCG) |
| **OS Guest** | Ubuntu Server 20.04 LTS |

---

## 📊 Hasil Benchmark

### **CPU Performance**
```
Events per second:    52.39
Total time:           10.0159s
Average latency:      18.97 ms
Performance:          ~3-4% of native
Overhead:             ~96-97%
```

### **Memory Performance**
```
Transfer rate:        179.32 MiB/sec
Operations/sec:       183,622.55
Average latency:      <0.005 ms
Performance:          ~1-2% of native
Overhead:             ~98-99%
```

### **Key Findings**
- ⚠️ Software virtualization memiliki overhead sangat tinggi (96-99%)
- ⚠️ Nested virtualization menambah complexity dan overhead signifikan
- ✅ Memberikan pemahaman mendalam tentang cost of virtualization
- ✅ Mendemonstrasikan pentingnya hardware acceleration (KVM)

---

## 🚀 Quick Start

### **Prerequisites**
```bash
# Ubuntu Linux dengan minimal requirements:
- CPU: 2+ cores
- RAM: 4+ GB
- Storage: 20+ GB free space
- Internet connection
```

### **Instalasi Environment**
```bash
# Update sistem
sudo apt update && sudo apt upgrade -y

# Install virtualization packages
sudo apt install -y qemu-kvm libvirt-daemon-system libvirt-clients \
                    virt-manager bridge-utils

# Verifikasi instalasi
systemd-detect-virt
virsh --version
virt-manager --version
```

### **Membuat Virtual Machine**
```bash
# Menggunakan virt-manager (GUI)
virt-manager

# Konfigurasi VM:
# - Memory: 2900 MB
# - CPU: 2 cores
# - Storage: 10 GB
# - OS: Ubuntu Server 20.04 LTS
```

### **Benchmarking**
```bash
# Di dalam VM, install sysbench
sudo apt update
sudo apt install -y sysbench

# CPU Benchmark
sysbench cpu run

# Memory Benchmark
sysbench memory run
```

---

## 📁 Struktur Repository

```
hypervisor-mini-qemu-kvm/
├── 01-proposal/
│   └── Proposal_Sistem_Operasi_Proyek_2.pdf
│
├── 02-minggu-12-instalasi/
│   ├── laporan_progres_minggu_12.pdf
│   └── bukti_kerja_minggu_12.pdf
│
├── 03-minggu-13-pembuatan-vm/
│   ├── Laporan_Minggu_13.pdf
│   └── Bukti_Kerja_Minggu_13.pdf
│
├── 04-minggu-14-benchmarking/
│   ├── Laporan_Minggu_14.pdf
│   └── Bukti_Kerja_Minggu_14.pdf
│
├── 05-laporan-akhir/
│   └── Laporan_Akhir_Hypervisor_Mini.pdf
│
└── 06-presentasi/
    ├── Slide_Presentasi_15_Slide.pdf
    └── Script_Presentasi.md
```

---

## 📖 Dokumentasi

### **Minggu 11 - Proposal**
- 📄 [Proposal Proyek](01-proposal/Proposal_Sistem_Operasi_Proyek_2.pdf)

### **Minggu 12 - Instalasi Environment**
- 📄 [Laporan Progres](02-minggu-12-instalasi/laporan_progres_minggu_12.pdf)
- 📄 [Bukti Kerja](02-minggu-12-instalasi/bukti_kerja_minggu_12.pdf)

### **Minggu 13 - Pembuatan VM**
- 📄 [Laporan Progres](03-minggu-13-pembuatan-vm/Laporan_Minggu_13.pdf)
- 📄 [Bukti Kerja](03-minggu-13-pembuatan-vm/Bukti_Kerja_Minggu_13.pdf)

### **Minggu 14 - Benchmarking**
- 📄 [Laporan Progres](04-minggu-14-benchmarking/Laporan_Minggu_14.pdf)
- 📄 [Bukti Kerja](04-minggu-14-benchmarking/Bukti_Kerja_Minggu_14.pdf)

### **Minggu 15 - Laporan Akhir & Presentasi**
- 📄 [Laporan Akhir Lengkap](05-laporan-akhir/Laporan_Akhir_Hypervisor_Mini.pdf)
- 🎤 [Slide Presentasi (15 slides)](06-presentasi/Slide_Presentasi_15_Slide.pdf)
- 📝 [Script Presentasi](06-presentasi/Script_Presentasi.md)

---

## 🔬 Metodologi

### **Timeline Pelaksanaan**

```
Minggu 11: PLANNING
    └─→ Penyusunan proposal

Minggu 12: SETUP
    └─→ Instalasi QEMU, libvirt, virt-manager

Minggu 13: IMPLEMENTATION
    └─→ Pembuatan & konfigurasi VM

Minggu 14: TESTING
    └─→ Benchmark CPU & Memory

Minggu 15: DOCUMENTATION
    └─→ Analisis & laporan akhir
```

### **Tools & Metodologi**
- **Benchmarking:** Sysbench (CPU & Memory tests)
- **Environment:** Nested virtualization (3 layers)
- **Analysis:** Performance comparison dengan native

---

## 📈 Analisis & Kesimpulan

### **Overhead Virtualisasi**

| Aspek | Overhead | Penyebab Utama |
|-------|----------|----------------|
| **CPU** | 96-97% | TCG binary translation (80-85%) + Nested virt (10-12%) |
| **Memory** | 98-99% | Memory management (85-90%) + Nested virt (8-10%) |

### **Lesson Learned**
✅ Software virtualization sangat berguna untuk learning tapi tidak untuk production  
✅ Hardware acceleration (KVM dengan VT-x/AMD-V) mutlak diperlukan untuk performa  
✅ Nested virtualization menambah overhead yang sangat signifikan  
✅ Hasil benchmark memberikan pemahaman mendalam tentang cost of virtualization  

### **Recommendations**
- 🔧 Gunakan bare-metal dengan hardware acceleration untuk production
- 🔧 Implement CPU pinning dan NUMA optimization
- 🔧 Extended benchmarking: disk I/O, network performance
- 🔧 Multiple VMs untuk test resource contention

---

## 🎓 Referensi

1. Barham, P., et al. (2023). *Xen and the art of virtualization*. ACM SIGOPS
2. Bellard, F. (2021). *QEMU, a fast and portable dynamic translator*. USENIX
3. Habib, I. (2022). *Virtualization with KVM*. Linux Journal
4. Kumar, R., & Singh, S. P. (2023). *Performance analysis of virtualization technologies*
5. Smith, J. E., & Nair, R. (2021). *Virtual machines: Versatile platforms*

**[Daftar Referensi Lengkap](05-laporan-akhir/Laporan_Akhir_Hypervisor_Mini.pdf)**

---

## 🤝 Kontribusi

Proyek ini dikembangkan sebagai tugas akhir mata kuliah. Jika ada pertanyaan atau saran:

- 💬 Issues: [GitHub Issues](https://github.com/username/hypervisor-mini-qemu-kvm/issues)
- 📧 Email: Lihat informasi kontak tim di laporan

---

## 📜 License

Proyek ini dilisensikan di bawah [MIT License](LICENSE).

---

## 🙏 Acknowledgments

- **Bapak Ferdi Chahyadi, S.Kom., M.Cs** - Dosen Pengampu Sistem Operasi
- **Program Studi Teknik Informatika UMRAH** - Fasilitas dan support
- **QEMU/KVM Community** - Dokumentasi dan resources
- **Sysbench Project** - Benchmarking tools

---

## 📞 Contact

**Universitas Maritim Raja Ali Haji**  
Program Studi Teknik Informatika  
Batam, Kepulauan Riau, Indonesia

🌐 Website: [https://umrah.ac.id](https://umrah.ac.id)

---

<div align="center">

**⭐ Star this repository jika bermanfaat!**

Made with ❤️ by Tim Proyek 2 Sistem Operasi 2024/2025

</div>

---

**Last Updated:** Desember 2025  
**Version:** 1.0.0  
**Status:** ✅ Completed
