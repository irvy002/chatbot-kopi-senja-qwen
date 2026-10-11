# Chatbot UMKM "Kopi Senja" (Qwen + QLoRA) - Versi 1

Prototype chatbot toko kopi fiktif. Alur: Teks → Qwen2.5-1.5B-Instruct (+ adapter LoRA) → Teks.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/irvy002/chatbot-kopi-senja-qwen   .../blob/main/Chatbot_Kopi_Senja_Qwen_QLoRA.ipynb)

## Metode
- Model dasar: Qwen2.5-1.5B-Instruct (4-bit), fine-tuning QLoRA (r=16, 5 epoch)
- Dataset buatan sendiri: 478 train, 53 validasi, 34 soal uji
- Antarmuka: Gradio (model dasar vs fine-tuned berdampingan)

## Hasil (34 soal uji)
| | Model dasar | Fine-tuned |
|---|---|---|
| Jawaban benar secara fakta | 0/34 | 31/34 |
| Rata-rata penilaian manual (1-5) | 2,18 | 4,81 |

## Keterbatasan
Model cenderung menghafal pola jawaban. Pada pertanyaan definisi ("apa itu happy hour?"), model menjawab jadwal promo, bukan definisi. Ini mendasari perbaikan di versi 2.

## Adapter LoRA
Unduh di: [https://drive.google.com/drive/folders/1wbihENRTYZ854c041moLZl8QvPWZWb08?usp=sharing]
