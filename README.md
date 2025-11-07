```mermaid
graph TD
    %% Tema Renkleri
    classDef anaTur fill:#ffebcc,stroke:#cc9900,stroke-width:2px,color:#000,font-weight:bold;
    classDef kadro fill:#cce5ff,stroke:#3366cc,stroke-width:1px,color:#000;
    classDef ortak fill:#ccffcc,stroke:#339966,stroke-width:1px,color:#000;
    classDef ortakGenel fill:#eeeeee,stroke:#666666,stroke-width:1px,color:#000,font-style:italic;

    %% Ana Baslik
    A([MUAFIYET TURERİ])
    class A anaTur

    %% Ana Turler
    A --> B([Tuzel Ortakli Sirket])
    A --> C([Standart Sirketler])
    A --> D([I. Tip Muafiyeti Olan Sirketler])
    A --> O([Ortak Kisitlar (Tum Turler Icin Gecerli)])
    class B,C,D anaTur
    class O ortakGenel

    %% Ortak Kisitlar
    O --> O1[Degerleme Uzmani Yardimcisi Minimumu: 1]
    O --> O2[Degerleme Uzmani Yardimcisi Orani: 0.10]
    O --> O3[Yuv. Turu: Klasik Yuv.]
    class O1,O2,O3 ortakGenel

    %% Tuzel Ortakli Sirket
    B --> B1([Ortak Sayisi: 2 veya daha fazla])
    B --> B2([Her Ortak: Gecici Muafiyet Alabilir])
    B --> B3([Yillik Rapor Sunumu Zorunlu])
    class B1,B2,B3 kadro

    %% Standart Sirketler
    C --> C1([Tek Ortakli])
    C --> C2([Tam Yetkili Uzman Kadrosu])
    C --> C3([Yillik Muafiyet Yenilemesi])
    class C1,C2,C3 kadro

    %% I. Tip Muafiyeti
    D --> D1([Kismi Faaliyet Izni])
    D --> D2([Sermaye Sarti: 1.000.000 TL])
    D --> D3([Ozel Raporlama Sarti])
    class D1,D2,D3 kadro
