graph TD
    subgraph Aktor
        User((User))
        Driver((Driver))
    end

    subgraph Use_Case
        Registrasi_User[Registrasi User]
        Membuat_Pesanan[Membuat Pesanan]
        Melakukan_Pembayaran[Melakukan Pembayaran]
        Membatalkan_Pesanan[Membatalkan Pesanan]
        Memberi_Rating[Memberi Rating]
        Registrasi_Driver[Registrasi Driver]
        Menerima_Pesanan[Menerima Pesanan]
        Menyelesaikan_Perjalanan[Menyelesaikan Perjalanan]
    end

    User --> Membuat_Pesanan
    User --> Melakukan_Pembayaran
    User --> Memberi_Rating
    User --> Membatalkan_Pesanan
    User --> Registrasi_User

    Driver --> Menerima_Pesanan
    Driver --> Menyelesaikan_Perjalanan
    Driver --> Membatalkan_Pesanan
    Driver --> Registrasi_Driver

    Membuat_Pesanan --> Menerima_Pesanan
