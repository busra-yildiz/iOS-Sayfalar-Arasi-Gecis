# iOS-Sayfalar-Arasi-Gecis
iOS uygulamalarında sayfalar arası geçiş genellikle UINavigationController veya alternatif olarak kullanabileceğiniz birçok farklı yol ile yapılabilir. 
İşte bu geçişleri nasıl yapabileceğinizi anlatan detaylı bir açıklama:

UINavigationController Kullanarak Sayfa Geçişi:
UINavigationController, iOS uygulamalarında yaygın olarak kullanılan bir yoludur. Temel olarak, bir dizi görünüm denilen View Controller'ları bir yığın
halinde tutar ve bu yığın üzerinden sayfa geçişleri yapmanıza olanak tanır. İşte nasıl kullanılır:
Adım 1: UINavigationController ekleyin:
Ana storyboard'unuzda veya kod ile bir UINavigationController ekleyin. Genellikle bu, uygulamanızın ana ekranı veya bir alt menü gibi bir ana görsel 
öğenin içine eklenir.
Adım 2: Sayfaları Ekleyin:
UINavigationController, birçok View Controller'ı içinde barındırabilir. Bu yüzden geçiş yapmak istediğiniz her sayfa için bir View Controller oluşturun.
Örneğin, "Ana Sayfa" ve "Detay Sayfa" gibi.
Adım 3: Geçişleri Tanımlayın:
Geçiş yapmak istediğiniz bir butona veya olaya sahip olan bir ViewController'a geçin (örneğin, "Ana Sayfa" ViewController'ı).
Swift için örnek bir kod:
// Geçiş yapılacak sayfayı oluşturun
let detayViewController = storyboard?.instantiateViewController(withIdentifier: "DetayViewController") as! DetayViewController

// Geçiş işlemini başlatın
self.navigationController?.pushViewController(detayViewController, animated: true)
Burada "DetayViewController" yerine hedef View Controller'ın adını ve kimliğini kullanmalısınız.
Segue (Bağlantı) Kullanarak Sayfa Geçişi:
Segue, bir View Controller'dan diğerine geçişi tanımlamak ve görsel bir şekilde storyboard üzerinden sürükleyip bırakarak oluşturmak için kullanılır. 
İşte nasıl kullanılır:
Adım 1: Storyboard'da Segue Ekleyin:
Ana storyboard'unuzda, bir View Controller'dan diğerine geçmek istediğiniz bağlantıyı oluşturun. Bu, bir buton veya bir görünüm öğesi üzerine sürükleyip 
bırakarak yapılabilir.
Adım 2: Segue Tanımlayın:
Segue oluşturduktan sonra, belirlediğiniz Segue'nin özelliklerini (örneğin, geçiş türü) ayarlayabilirsiniz.
Adım 3: Geçişi Tetikleyin:
Segue'yi tetiklemek için bir buton, bir etkinlik veya programatik olarak bir işlem kullanabilirsiniz. Genellikle bu işlem, kullanıcının bir eylemi 
gerçekleştirmesi sonucunda gerçekleşir.
Swift için örnek bir kod (programatik tetikleme):
performSegue(withIdentifier: "DetaySegue", sender: self)
Burada "DetaySegue" yerine oluşturduğunuz Segue'nin adını kullanmalısınız.
Bu iki yöntem, iOS uygulamalarında sayfalar arası geçiş yapmanın iki yaygın yoludur. Hangi yöntemi kullanacağınız, uygulamanızın gereksinimlerine ve tasarımına bağlı olarak değişebilir.
