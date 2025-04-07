# 🌩️ cloud-uth – Υποδομή για το Μάθημα Νεφοϋπολογιστικής

Καλωσορίσατε στο αποθετήριο του μαθήματος **Νεφοϋπολογιστική** για το Εαρινό Εξάμηνο 2024–2025. Το αποθετήριο αυτό περιέχει:

✅ Παραδείγματα με χρήση Docker & Docker Compose  
✅ Υλοποιήσεις σε Kubernetes: Pods, Deployments, StatefulSets, Volumes, ConfigMaps, Secrets  
✅ Πλήρη οδηγό για σύνδεση με την υποδομή Kubernetes του εργαστηρίου μέσω OpenVPN  
✅ Τεκμηρίωση σε μορφή Markdown και Makefile για αυτοματισμούς

## 📁 Δομή Οδηγιών

| Ενότητα | Περιγραφή |
|--------|-----------|
| [00_Preparatory-lab](docs/00_Preparatory-lab/) | Ρύθμιση Docker Desktop με WSL2 |
| [01_lab1-docker](docs/01_lab1-docker/) | Εισαγωγή στο Docker με πρακτικά παραδείγματα |
| [01_lab1-k8s](docs/01_lab1-k8s/) | Kubernetes, kubectl, k9s, Deployments, PVCs, StatefulSets |

## 🚀 Εκκίνηση

```bash
git clone https://github.com/ikons/cloud-uth.git
cd cloud-uth
```

> 💡 Βεβαιωθείτε ότι έχετε εγκαταστήσει:
> - Docker Desktop (με WSL2 backend)
> - OpenVPN Client
> - `kubectl` και `k9s`
