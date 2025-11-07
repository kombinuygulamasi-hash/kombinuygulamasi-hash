graph TD
    %% Tema Renkleri
    classDef anaTur fill:#ffebcc,stroke:#cc9900,stroke-width:2px,color:#000,font-weight:bold;
    classDef kadro fill:#cce5ff,stroke:#3366cc,stroke-width:1px,color:#000;
    classDef ortak fill:#ccffcc,stroke:#339966,stroke-width:1px,color:#000;
    classDef ortakGenel fill:#eeeeee,stroke:#666666,stroke-width:1px,color:#000,font-style:italic;

    %% Ana Başlık
    A([MUAFİYET TÜRLERİ])
    class A anaTur

    %% Ana Türler
    A --> B([Tüzel Ortaklı Şirket])
    A --> C([Standart Şirketler])
    A --> D([I. Tip Muafiyeti Olan Şirketler])
    A --> O([Ortak Kısıtlar (Tüm Türler İçin Geçerli)])
    class B,C,D anaTur
    class O ortakGenel

    %% Ortak Kısıtlar
    O --> O1[Değerleme Uzmanı Yardımcısı Minimumu: 1]
    O --> O2[Değerleme Uzmanı Yardımcısı Oranı: 0,10]
    O --> O3[Yuvarlama Türü: Klasik Yuvarlama]
    class O1,O2,O3 ortakGenel

    %% --- Tüzel Ortaklı Şirket ---
    B --> B1[Vaka 1]
    B --> B2[Vaka 2]

    %% Vaka 1
    B1 --> B1A[Kadro Kısıtları - Vaka 1]
    class B1A kadro
    B1A --> B1A1[Sorumlu Değerleme Uzmanı Min.: 2]
    B1A --> B1A2[Toplam Değerleme Uzmanı Min.: 5]

    B1 --> B1B[Ortaklık Kısıtları - Vaka 1]
    class B1B ortak
    B1B --> B1B1[Sermaye Min.: 0,00 TL]
    B1B --> B1B2[Ortak Sorumlu Uzman Min.: 2]
    B1B --> B1B3[SDU Ortaklık Payı Min.: 0,10]
    B1B --> B1B4[Toplam SDU Ortaklık Payı Min.: 0,51]
    B1B --> B1B5[Toplam TÜZEL Ortaklık Payı Min.: 0,01]
    B1B --> B1B6[Bütün SDU'lar Ortak/Değil: İşaretsiz]

    %% Vaka 2
    B2 --> B2A[Kadro Kısıtları - Vaka 2]
    class B2A kadro
    B2A --> B2A1[Sorumlu Değerleme Uzmanı Min.: 2]
    B2A --> B2A2[Toplam Değerleme Uzmanı Min.: 5]

    B2 --> B2B[Ortaklık Kısıtları - Vaka 2]
    class B2B ortak
    B2B --> B2B1[Sermaye Min.: 0,00 TL]
    B2B --> B2B2[Ortak Sorumlu Uzman Min.: 0]
    B2B --> B2B3[SDU Ortaklık Payı Min.: 0,00]
    B2B --> B2B4[Toplam SDU Ortaklık Payı Min.: 0,00]
    B2B --> B2B5[Toplam TÜZEL Ortaklık Payı Min.: 0,51]
    B2B --> B2B6[Bütün SDU'lar Ortak/Değil: İşaretsiz]

    %% --- Standart Şirketler ---
    C --> C1[Vaka 1]
    C --> C2[Vaka 2]

    %% Vaka 1
    C1 --> C1A[Kadro Kısıtları - Vaka 1]
    class C1A kadro
    C1A --> C1A1[Sorumlu Değerleme Uzmanı Min.: 1]
    C1A --> C1A2[Toplam Değerleme Uzmanı Min.: 10]

    C1 --> C1B[Ortaklık Kısıtları - Vaka 1]
    class C1B ortak
    C1B --> C1B1[Sermaye Min.: 1.000.000 TL]
    C1B --> C1B2[Ortak Sorumlu Uzman Min.: 1]
    C1B --> C1B3[SDU Ortaklık Payı Min.: 0,10]
    C1B --> C1B4[Toplam SDU Ortaklık Payı Min.: 0,51]
    C1B --> C1B5[Toplam TÜZEL Ortaklık Payı Min.: 0,00]
    C1B --> C1B6[Bütün SDU'lar Ortak/Değil: İşaretli (✓)]

    %% Vaka 2
    C2 --> C2A[Kadro Kısıtları - Vaka 2]
    class C2A kadro
    C2A --> C2A1[Sorumlu Değerleme Uzmanı Min.: 2]
    C2A --> C2A2[Toplam Değerleme Uzmanı Min.: 10]

    C2 --> C2B[Ortaklık Kısıtları - Vaka 2]
    class C2B ortak
    C2B --> C2B1[Sermaye Min.: 1.000.000 TL]
    C2B --> C2B2[Ortak Sorumlu Uzman Min.: 2]
    C2B --> C2B3[SDU Ortaklık Payı Min.: 0,10]
    C2B --> C2B4[Toplam SDU Ortaklık Payı Min.: 0,51]
    C2B --> C2B5[Toplam TÜZEL Ortaklık Payı Min.: 0,00]
    C2B --> C2B6[Bütün SDU'lar Ortak/Değil: İşaretli (✓)]

    %% --- I. Tip Muafiyeti Olan Şirketler ---
    D --> D1[Kadro Kısıtları]
    class D1 kadro
    D1 --> D1A[Sorumlu Değerleme Uzmanı Min.: 2]
    D1 --> D1B[Toplam Değerleme Uzmanı Min.: 5]

    D --> D2[Ortaklık Kısıtları]
    class D2 ortak
    D2 --> D2A[Sermaye Min.: 0,00 TL]
    D2 --> D2B[Ortak Sorumlu Uzman Min.: 2]
    D2 --> D2C[SDU Ortaklık Payı Min.: 0,10]
    D2 --> D2D[Toplam SDU Ortaklık Payı Min.: 0,51]
    D2 --> D2E[Toplam TÜZEL Ortaklık Payı Min.: 0,00]
    D2 --> D2F[Bütün SDU'lar Ortak/Değil: İşaretli (✓)]

