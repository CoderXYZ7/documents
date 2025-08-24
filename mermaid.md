# hi
``` mermaid
flowchart TD
    subgraph Server["Server Remoto"]
        P[Gestione Pagamenti]
        U[Gestione Utenti]
        L[Generazione Licenze (JWT)]
        P --> L
        U --> L
    end

    subgraph Client["App Mobile / PC Cliente"]
        T[Token JWT ricevuto]
    end

    subgraph Device["Raspberry Player"]
        V[Chiave pubblica integrata]
        C[Verifica Token]
        A[Audio Cifrato]
        Pm[Player Standard]
        Pro[Player Pro]
    end

    L -->|Invio Token| T
    T -->|Bluetooth / USB Gadget| C
    V --> C
    C -->|Token valido| Pro
    C -->|Token non valido| Pm
    A --> Pm
    A --> Pro
```
