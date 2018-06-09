# project1
import time 

class depo(): #ana sınıf depo olarak oluşturuldu.
    
    
    def __init__(self,adet_sayisi="0",renk="yok",özellik="yok"):#init metodunda kendimiz özel değerlerimizi atıyoruz.
        self.adet_sayisi=adet_sayisi
        self.renk=renk
        self.özellik=özellik
        
class forklit(depo):# forklit sınıfı depo sınıfında kalıtılarak oluşturuldu.
    def __init__(self,adet_sayisi,renk,özellik,marka="yok",ülke="yok"):#burada iki özellik ekliyoruz , hangi ülkede üretildiği ve markası
    super().__init__(adet_sayisi,renk,özellik) #super metodu ile miras aldığımız sınıfın özelliklerini eklemiş oluyoruz
    self.marka =marka #marka ve ülke bilgileri bu sınıf a tanımlanıyor.
    self.ülke =ülke
    
    def forklit(self,adet_sayisi,renk,özellik,marka,ülke):#burada ki fonksiyon ile parametreye denk gelen özellikleri bilgi girşi için eşitliyoruz 
        self.adet_sayisi=adet_sayisi #input metodu ile bilgi girşi yapacağız
        self.renk=renk
        self.özellik=özellik
        self.marka=marka
        self.ülke=ülke
        
    def bilgilerigöster(self):#bilgileri göstermek için bir fonksiyon 
        print("forklit sınıfı bilgileri")
        print("adet_sayisi: {}\n renk: {}\n özellik: {}\n marka : {}\n ülke: {}".format(self.adet_sayisi,self.renk,self.özellik,self.marka,self.ülke))
        
        
class termimal (forklit,depo): #terminal sınıfı forklit ve depo sınıflarından türetilerek oluşturuluyor.
    def __init__(self,adet_sayisi,renk,özellik,marka,ülke,motor_hacmi="yok"):#burada ek olarak motor hacmi bilgisi eklendi
    super().__init__(adet_sayisi,renk,özellik,marka,ülke) #kalıtım sınıfında aldığımız verileri super metodu ile çağarıyoruz
    self.motor_hacmi=motor_hacmi
    
    def terminal_ekle(self,adet_sayisi,renk.özellik,marka,ülke,motor_hacmi):
        self.adet_sayisi=adet_sayisi
        self.renk=renk
        self.özellik=özellik
        self.marka=marka
        self.ülke=ülke
        self.motor_hacmi=motor_hacmi
        
    def terminal_bilgilerini_göster(self):
        print("terminal sınıfı bilgileri..")
        print("adet sayisi: {}\n renk: {}\n özellik: {}\n marka : {}\n ülke: {}\n motor hacmi : {}".format(self.adet_sayisi,self.renk,self.özellik,self.marka,self.ülke,self.motor_hacmi))
        
class kamyon (forklit,depo):
    def __init__(self,adet_sayisi,renk,özellik,marka,ülke,motor_hacmi,hız="0",boy="0"):
        super().__init__(self,adet_sayisi,renk,özellik)
        self.hız=hız
        self.boy=boy
        
    def kamyon_ekle(self,adet_sayisi,renk,özellik,marka,ülke,hız,boy):
        self.adet_sayisi=adet_sayisi
        self.renk=renk
        self.özellik=özellik
        self.marka=marka
        self.ülke=ülke
        self.hız=hız
        self.boy=boy
        
    def kamyon_bilgileri_göster
        print("kamyon sınıfı bilgileri gösteriliyor...")
        print("adet sayisi :{}\n renk:{}\n özellik: {}\n marka:{}\n ülke:{}\n hız:{}\n boy: {}".format(self.adet_sayisi,self.renk,self.özellik,self.marka,self.ülke,self.hız,self.boy))
        
        
        
        
forklit =forklit("5","mavi","yok","ge","ger") #sınıflardan yeni nesneler oluşturuyoruz ve parametre değerlerini veriyoruz
terminal =terminal("3","siyah","yok","ge","ger","yok")
kamyon=kamyon("4","beyaz","yok","ge","tr","yok","yok")



print ("""


0. çıkış için "q" ya basınız ...
1.forklit bilgisi girişi için 
2.forklit bilgilerini göstermek için
3.terminal bilgisi girişi için 
4.terminal bilgilerini göstermek için 
5.kamyon bilgisi girişi için 
6.kamyon bilgilerini göstermek için 
  basınız .......




""")
        
        
  

 while True:
        işlem =input("işlem seçiniz:")
        
        if (işlem =="q"):
            print("program sonlandırlıyor....")
            time.sleep(2)
            break
 #burada giriş verileri isteniyor ve ilgili nesnenin ilgili fonk. çalıştırılarak etkileşim sağlanıyor 


        elif  (işlem=="1"):
                adet_giris=input("adet sayısı:")
                renk_giris=input("rengi:")
                ozellik_giris=input("özelliği:")
                marka_giris=input("markası:")
                ulke_giris=input("ülkesi")
                
                
                forklit.forklit(adet_giris,renk_giris,ozellik_giris,marka_giris,ulke_giris)
        elif (işlem =="2"):
            
            forklit.bilgilerigoster()
            
            
        elif (işlem=="3"):
            adet_giris=input("adet sayısı:")
            renk_giris=input("rengi:")
            ozellik_girisi=input("ozellik:")
            marka_giris=input("markası:")
            ulke_giris=input("ülkesi:")
            motor_giris=input("motor hacmi:")
            
            
            terminal.terminal_ekle(adet_giris,renk_giris,ozellik_giris,marka_giris,ulke_giris,motor_giris)
            
            
        elif (işlem=="4"):
            terminal.bilgilerigoster()
            
        elif (işlem=="5"):
            adet_giris=input("adet sayısı:")
            renk_giris=input("rengi:")
            ozellik_giris=input("özellik:")
            marka_giris=input("markası:")
            ulke_giris=input("ülkesi:")
            hız_giris=input("hızı:")
            boy_giris=input("boyu:")
            
            
            kamyon.kamyon_ekle(adet_giris,renk_giris,ozellik_giris,marka_giris,ulke_giris,hız_giris,boy_giris)

            
        elif (işlem=="6") :
            kamyon.bilgilerigoster ()
            
            
            
            
            
            
            
            
            
            
            
               
                
        
        
        
        
        
        
        
