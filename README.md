Proje taslak projesi olup bir sürü gereksiz kod mevcuttur ama derlenebilir haldedir.
Proje tamamen zevk için yazıldığından dolayı birçok yazım hatası ve çok kötü bir yazım şekline sahip biraz eğlenmek istedik açıkçası.
Projede olan neredeyse tüm sistemler sorunsuz olarak çalışmakta en önemliside farmbot pointer güncelleyip kullanılabilecek haldedir.
M_FLDB olarak tanımladığım pointer aslında mobptr yani entitiylist dir. Etraftaki mobları,playerleri,metinleri,npcleri okumak için kullanıyoruz.
M_Mobptr olarak tanımladığım pointer ise CpythonPlayerdir yani GetTargetVid yi bulurken kullandığımız pointer yada PickCloseItem fonksiyonunun mov ecx i her ikiside aynı.
M_Playerptr ise adından da anlaşılacağı üzere player bilgilerini tutan pointer oluyor ve CINstanceBase dir yani wh yaparken kullandığımız pointer.
M_Target olarak tanımladığım offset ise GetTargetVid offsetidir.
M_TargetMob ise koşulacak mobun idsinin yazılacağı adresin offseti.
M_MobRun ise durum offseti. 0 dururken aldığı değerdir 3 ise moba koşarar ve vurur. eğer bu offseti 3 e sabitlerseniz mob ölene kadar vurmaya devam eder.Hangi moba 
vuracağını ise M_TargetMob da hangi vid yazıyorsa ona vurur farmbot mantığı şöyle çalışıyor M_TargetMob adresine saldırılacak mobun vid sini yazıyoruz ve M_Mobrun adresini 
3 değerine sabitliyoruz mob ölene kadar verdiğimiz vid ye saldıracaktır.
Proje c++ Builder 10.4 ile yazılmıştır.

