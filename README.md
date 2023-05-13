# VIS integracijos
## Kam to reikia?
Ši repozitorija skirta panaudojant Mermaid įrankį surinkti į vieną vietą Lietuvoje turimų informacinių sistemų tarpusavio sąryšius, tam, kad galima būtų susidaryti bendrą vaizdą ir palengvinti Perkančiosioms organizajioms ir IT sprendimų tiekėjams vertinti esamą situaciją ir palengvinti IS kūrimą valstybės mąstu.

## Aplinkos ministerijos valdomų ir jai pavaldžių įstaigų VIS integracijos
### Trumpiniai
VIS - valstybinės informacinės sistemos

```mermaid
%%{init: { "flowchart": { "htmlLabels": true, "curve": "basis", "useMaxWidth":true } } }%%

flowchart TD

subgraph VKI IS
    direction RL
    PENSEIS
    SSĮP
    IKS
    GPAIS
    AAKIS
    Infostatyba
    ALIS
    APVIS
end

%% === PENSEIS ===
PENSEIS
SPSC -->|Tvarkytojas|PENSEIS
subgraph RC
    NTR
    GR
end
NTR --> PENSEIS
GR --> PENSEIS

%% === SPĮP ===
SSĮP
APVA -->|Tvarkytojas|SSĮP
APVA -->|Valdytojas|SSĮP

%% === IKS ===
IKS
AM -->|Valdytojas|IKS
AAD -->|Tvarkytojas|IKS
AAA -->|Tvarkytojas|IKS
subgraph VMI
    IMIS
    MAIS
end
IMIS --> IKS
MAIS --> IKS

%% === GPAIS ===
GPAIS
AM -->|Valdytojas|GPAIS
AAA -->|Tvarkytojas|GPAIS
subgraph RC
    AR
    JAR
end
subgraph IVPK
    VIISP
end
ALIS --> GPAIS
ATVR --> GPAIS
JAR --> GPAIS
AR --> GPAIS
GR --> GPAIS
IKS --> GPAIS
VIISP --> GPAIS

%% === AAKIS ===
AAKIS
AM -->|Valdytojas|AAKIS
AAD -->|Tvarkytojas|AAKIS
VMT -->|Tvarkytojas|AAKIS
GMU -->|Tvarkytojas|AAKIS
LGT -->|Tvarkytojas|AAKIS
VSTT -->|Tvarkytojas|AAKIS
subgraph IVPK
    VAIISIS
end
ALIS -->AAKIS
UETK -->AAKIS
STK -->AAKIS
JAR -->AAKIS
GR -->AAKIS
GRPK -->AAKIS
VAIISIS -->AAKIS
ATPR -->AAKIS

%% === Infostatyba ===
Infostatyba
subgraph RC
    NTK
end
AM -->|Valdytojas|Infostatyba
KPD -->|Tvarkytojas|Infostatyba
NŽT -->|Tvarkytojas|Infostatyba
SPSC -->|Tvarkytojas|Infostatyba
JAR -->|XML|Infostatyba
NTR -->|XML|Infostatyba
AR-->|XML|Infostatyba
GR -->|TXT|Infostatyba
VIISP -->|XML|Infostatyba
GPRK -->|XML|Infostatyba
NTK -->|XML|Infostatyba
TIIIS -->|Str.d.|Infostatyba
Vartai -->|XML|Infostatyba
TPDR -->|XML, GIF, JPEG, OGC, GML, TIFF|Infostatyba
MAIS -->|XML|Infostatyba
LEII -->|XML|Infostatyba

%% === ALIS ===
ALIS
AM -->|Valdytojas|ALIS
AM -->|Tvarkytojas|ALIS
AAA -->|Tvarkytojas|ALIS
AAD -->|Tvarkytojas|ALIS
VMT -->|Tvarkytojas|ALIS
LGT -->|Tvarkytojas|ALIS
VSTT -->|Tvarkytojas|ALIS
JAR -->|XML|ALIS
AR -->|XML|ALIS
NTR -->|XML|ALIS
NTK -->|XML|ALIS
GR -->|XML|ALIS
UETK -->ALIS
AIVIKS -->ALIS
MVK -->ALIS
STK -->ALIS
GRPK -->ALIS
VAIISIS -->ALIS
KVR -->ALIS

%% === APVIS ===
APVIS
APVA -->|Valdytojas|APVIS
APVA -->|Tvarkytojas|APVIS
VIISP -->APVIS
KTPR -->APVIS
JAR -->APVIS
```
