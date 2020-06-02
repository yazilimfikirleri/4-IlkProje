# 4-IlkProje
C# Console ilk proje

# Kod Derleme Süreçleri (CLR, CLS, MSIL) 
Bir proglamlama dili öğrenirken, kullandığımız dili tanımak ve onu en etkin şekilde kullanmak esastır. Kullanacağımız .net Framework platformunu ve C# programlama dilini daha yakından tanımak için kod derleme süreçlerini çok iyi bilmeliyiz. Öncelikle işlemleri basitçe tanıyalım ve daha sonra terimlerimizi detaylı olarak inceleyelim. Örneğin C# programlama dilinde bir program yazdık. Bu programı çalıştırdığımızda neler oluyor? Hangi işlemler gerçekleşiyor? Bu işlemler gerçekleşirken .net Framework bu işin neresinde yer alıyor? Öncelikle .Net Framework’ü daha yakından tanıyalım. 

.Net Framework çatısı farklı dillerin aynı ortamda çalışmasını sağlar. Net Framework barındırdığı ortak dil çalışma zamanı (Common Language Runtime) sayesinde, .Net’in desteklediği diğer diller ile yazılmış kodları makine diline çevirerek yazılımlarda çoklu dil kullanmaya olanak sağlar. Çoklu dil kullanırken; 

- Her kod önce kendi diline ait derleyici ile derlenir ve MSIL koduna dönüştürülür. 
- Derlenen kod MSIL’e göre yeniden derlenir. Elde edilen MSIL kodu kendi başına çalışabilen bir kod değildir. MSIL bir takım taşınabilir assembly koddan oluşur. 
- Daha sonra CLR, MSIL olarak derlenmiş kodu çalıştırılabilir kod haline getirir. 

Bu işlem tüm .Net Framework çatısı altında toplanan diller için aynı şekilde uygulandığı için .Net çatısı altında toplanan diller arasında performans farkı yok denilecek kadar azdır. Oluşan performans farkı sadece dile ait derleyiciden kaynaklanmaktadır. Net Framework çatısı altında aşağıdaki programlama dilleri bulunmaktadır. 

- C#
- Visual Basic.Net
- Visual J#.Net 
- Visual C++ 
- Jscript.Net 
- Cobol 
- Perl
- Eiffel
- Python 
- Pascal
- Mercury
- Mondrian
- Oberon 
- Salford FTN95 (Fortran) 
- Small Talk
- Standart ML 
- Dyalog APL 

## Microsoft Intermediate Language  - MSIL (IL)
Bir C# kodu yazıp derlediğimizde bu kod Microsoft Intermediate Language ( MSIL ) 'a dönüştürülür. Bu kod " sözde kod " ( pseudo code ) içeren bir dosyadır. Bu kod çalıştırılabilir bir kod değildir. Bu kod anca bulunduğu sistemde bir ara program ile çalıştırılır.

## CLR ( Common Language Runtime ) 
CLR kısaca yazılan programın tüm işletim sistemlerinde çalışmasını sağlamakla görevlidir. Örneğin biz java ile yazılmış bir oyunu Windows işletim sistemine sahip bir bilgisayarda oynamak istediğimizde, Java Runtime Environment’ı bilgisayarımıza kurmalıyız. CLR .NET ile programların çalışmasını kontrol eden birimdir. Eskiden programlar derlenirken makine diline çevrilirdi ve işletim sistemiyle bağlantılı olarak çalışırlardı. Ama günümüzde kodları yorumlayacak kütüphane ve derleyici programlar ile platform bağımsız kod yazabilmekteyiz. 

## CLS ( Common Language Specification - Ortak Dil Spesifikasyonu )
Common Language Specification(CLS) bünyesinde barındırdığı birtakım yapıları ve kısıtları ile kütüphane(library) ve derleyici(compiler) yazabilmek için rehberlik yapmaktadır. CLS yazılan bir kütüphanenin CLS'yi destekleyen diğer programlama dilleri ile entegre şekilde çalışabilmesini ve bu diller tarafından da kullanılabilmesini sağlamaktadır. CLS, CTS'nin bir altkümesidir. CLS uygulama geliştiriciler için büyük önem arzetmektedir. Öyle ki bir uygulama geliştirici yazdığı kodun diğer kod geliştiriciler tarafından da kullanılabilir olmasını gözönünde bulundurmalıdır. CLS'nin kriterleri ve kuralları gözönünde bulundurularak yazılan bir API(Application Program Interface) diğer programlama dilleri içerisinden kullanılabilmekte Common Language Runtime tarafından da işletilebilmektedir. 
