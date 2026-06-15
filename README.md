def dogrusal_fonksiyon(a, b, x):
    return a * x + b

def fonksiyon_tersi(a, b):
    if a == 0:
        return "Gecersiz fonksiyon (a sifir olamaz)"
    return "(x - " + str(b) + ") / " + str(a)

def bileske_fonksiyon(a1, b1, a2, b2, x):
    g_x = a2 * x + b2
    f_g_x = a1 * g_x + b1
    return f_g_x

print("--- 10. SINIF MATEMATIK PROJESI: FONKSIYON MATIK ---")
print("1- Fonksiyon Degeri Hesapla f(x) = ax + b")
print("2- Dogrusal Fonksiyonun Tersi Bul f^-1(x)")
print("3- Bileske Fonksiyon Hesapla (f o g)(x)")

secim = input("Yapmak istediginiz islemi secin (1/2/3): ")

if secim == "1":
    a = float(input("a degerini girin: "))
    b = float(input("b degerini girin: "))
    x = float(input("x degerini girin: "))
    sonuc = dogrusal_fonksiyon(a, b, x)
    print("Sonuc: " + str(sonuc))

elif secim == "2":
    a = float(input("a degerini girin: "))
    b = float(input("b degerini girin: "))
    tersi = fonksiyon_tersi(a, b)
    print("Fonksiyonun Tersi: " + str(tersi))

elif secim == "3":
    print("f(x) = a1*x + b1 ve g(x) = a2*x + b2 olsun.")
    a1 = float(input("a1 degerini girin: "))
    b1 = float(input("b1 degerini girin: "))
    a2 = float(input("a2 degerini girin: "))
    b2 = float(input("b2 degerini girin: "))
    x = float(input("x degerini girin: "))
    sonuc = bileske_fonksiyon(a1, b1, a2, b2, x)
    print("Sonuc: " + str(sonuc))

else:
    print("Gecersiz secim yaptiniz!")
