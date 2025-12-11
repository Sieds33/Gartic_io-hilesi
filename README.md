# Gartic_io-hilesi




import tkinter as tk
from tkinter import messagebox



# KELİME LİSTESİ
gartic_liste = ["açlik", "ağustos böceği", "aile", "akşam yemeği", "aksiyon", "alpaka", "avci" , "baba", "babun", "badem", "bahçe", "bakir", "bale", "bambu", "bankaci", "bebek bezi", "bere", "berber", "bilgisayar korsani", "böcek", "boya kalemi", "bronz", "buzdolabi", "buz sarkiti" , "ceset", "cin", "cinsiyet", "cyborg"  ,  "çakal", "çakil", "çamaşir suyu", "çapa", "çekiç", "çekmece", "çimento", "çift", "çiftçi", "çiçek", "çöl"  , "daire", "dal", "darbe", "diş telleri", "doktor", "dolar", "dolaşmak", "dosya", "Duvar-e", "düğme" , "ejderha", "engel", "Eskimo", "eşek" , "feryat", "filtre", "firin", "fosil" , "garaj", "gayzer", "gitar", "gökada", "guguk kuşu" , "hali", "halletmek", "hançer", "havuç", "hava yastiği", "havyar", "hippi", "hobbit", "hokey", "huysuz" , "ihanet etmek", "içeri", "iPhone" , "kabarcik", "kaktüs", "Kahve", "kamera", "kanarya", "kanyon", "kask", "keçi sakali", "kilise", "kiraz", "koza", "koltuk alti", "komedi", "kova", "kovboy", "köprü", "köşe", "kredi", "kulak kiri", "kumaş", "kumarhane", "kunduz", "kurabiye", "kuzen", "közler" , "liman" , "mermi", "morarma", "motor", "mum", "musluk", "muz", "münzevi" , "nazik", "nefes" , "okçu", "orman" , "pamuk", "parmak", "peynir", "porsuk" , "sağlik", "sarimsak", "Satürn", "savaş", "Segway", "sepet", "siçrama", "silgi", "sinema", "sinir", "sirk", "Slinky", "Sudoku", "sürücü", "sümük" , "şişe" , "tabut", "tampon", "Tarzan", "tehlike", "tereyaği", "Tetris", "top", "Tweety" , "Uranüs", "uşak", "utandirici" , "üzümler" , "varil", "yaka", "yanaklar", "yonca" , "zil"]

# --- Düzeltme 1: while True DÖNGÜSÜ KALDIRILDI ---
# Arayüz (GUI) uygulamaları, komut satırı döngüsü (while True) yerine 
# fonksiyonlar aracılığıyla olay (event) döngüsünde çalışır.

## --- Düzeltme 2: Arama Mantığı Fonksiyona Taşındı ---
def kelime_ara_ve_goster(event=None):
    # Harf girişini arayüzden al
    gartic_harf = giriş_alani.get().lower().strip()
    
    # Kelimeleri listelemek için boş bir dize (string) hazırla
    sonuc_yazisi = ""

    # Sizin if/elif yapınızın arayüzden alınan harfe göre çalıştırılması
    if (gartic_harf == "a" ):
        sonuc_yazisi = ", ".join(gartic_liste[:6])
    elif (gartic_harf == "b"):
        sonuc_yazisi = ", ".join(gartic_liste[7:24])
    elif (gartic_harf == "c"):
        sonuc_yazisi = ", ".join(gartic_liste[24:28])
    elif (gartic_harf == "ç"):
        sonuc_yazisi = ", ".join(gartic_liste[28:38])
    elif (gartic_harf == "d"):
        sonuc_yazisi = ", ".join(gartic_liste[39:49])
    elif (gartic_harf == "e"):
        sonuc_yazisi = ", ".join(gartic_liste[49:53])
    elif (gartic_harf == "f"):
        sonuc_yazisi = ", ".join(gartic_liste[53:57])
    elif (gartic_harf == "g"):
        sonuc_yazisi = ", ".join(gartic_liste[57:62])
    elif (gartic_harf == "h"):
        sonuc_yazisi = ", ".join(gartic_liste[62:72])
    elif (gartic_harf == "i"):
        sonuc_yazisi = ", ".join(gartic_liste[72:75])
    elif (gartic_harf == "k"):
        sonuc_yazisi = ", ".join(gartic_liste[75:100])
    elif (gartic_harf == "l"):
        sonuc_yazisi = ", ".join(gartic_liste[100:101])
    elif (gartic_harf == "m"):
        sonuc_yazisi = ", ".join(gartic_liste[101:108])
    elif (gartic_harf == "n"):
        sonuc_yazisi = ", ".join(gartic_liste[108:110])
    elif (gartic_harf == "o"):
        sonuc_yazisi = ", ".join(gartic_liste[110:112])
    elif (gartic_harf == "p"):
        sonuc_yazisi = ", ".join(gartic_liste[112:116])
    elif (gartic_harf == "s"):
        sonuc_yazisi = ", ".join(gartic_liste[116:131])
    elif (gartic_harf == "ş"):
        sonuc_yazisi = ", ".join(gartic_liste[131:132])
    elif (gartic_harf == "t"):
        sonuc_yazisi = ", ".join(gartic_liste[132:140])
    elif (gartic_harf == "u"):
        sonuc_yazisi = ", ".join(gartic_liste[140:143])
    elif (gartic_harf == "ü"):
        sonuc_yazisi = ", ".join(gartic_liste[143:144])
    elif (gartic_harf == "v"):
        sonuc_yazisi = ", ".join(gartic_liste[144:145])
    elif (gartic_harf == "y"):
        sonuc_yazisi = ", ".join(gartic_liste[145:148])
    elif (gartic_harf == "z"):
        sonuc_yazisi = ", ".join(gartic_liste[148:149])
    else:
        # Hata durumunu arayüzde göster
        sonuc_etiketi.config(text="Geçersiz harf girişi.")
        giriş_alani.delete(0, tk.END)
        return

    # Eğer sonuç bulunduysa, etiketi güncelle
    sonuc_etiketi.config(text=f"'{gartic_harf.upper()}' Harfiyle Başlayan Kelimeler:\n\n{sonuc_yazisi}")
    # Giriş alanını temizle
    giriş_alani.delete(0, tk.END)

# --- TKINTER ARAYÜZ KISMI ---
ana_pencere = tk.Tk()
ana_pencere.title ("Kelime bulma hilesi.")
ana_pencere.geometry ("500x400")

baslik_etiketi = tk.Label(
    ana_pencere,
    text = "Gartic ipuçları",
    font = ("Helvetica",16,"bold"),
    fg = "navy"
)
baslik_etiketi.pack (pady = 10)

giriş_alani = tk.Entry (
    ana_pencere,
    width = 10,
    font = ("Helvetica",12),
    justify = "center"
)
giriş_alani.pack (pady = 5)

# --- Düzeltme 3: command ve bind Fonksiyon Bağlantıları ---
# gartic_liste yerine yeni oluşturduğumuz fonksiyonu bağla
giriş_alani.bind ("<Return>", kelime_ara_ve_goster) # Enter tuşu için

arama_dugmesi = tk.Button (
    ana_pencere,
    text = "Kelime bul",
    command = kelime_ara_ve_goster, # Buton tıklaması için
    bg = "green",
    fg = "white",
    font = ("Helvetica",10,"bold")
)
arama_dugmesi.pack (pady = 10)

sonuc_etiketi = tk.Label (
    ana_pencere,
    text = "Lütfen yukarıya bir harf girip 'Kelimeyi Bul' butonuna tıklayın.",
    font = ("Helvetica", 11),
    justify = tk.LEFT,
    wraplength = 450,
    bg = "lightgray",
    padx = 10,
    pady = 10,
    anchor="nw" # Metni sol üste hizala
)
sonuc_etiketi.pack (pady = 20, padx = 20, fill = 'x')

ana_pencere.mainloop()
