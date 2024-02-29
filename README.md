# Fluence Airdropumu Nasıl Claim Edeceğim?

Selamlar, [Fluence Network](https://fluence.network/) 110 bini aşkın aktif web3 geliştiricisine $FLT token airdropu yaptı. Ben de Rues hocam sayesinde bunun farkına varıp claim ettim. RC <3

Claim için ne yapmamız gerekiyor onu anlatacağım.

Öncelikle [claim sayfasına](https://claim.fluence.network/) gidiyoruz ve github kullanıcı adımızı aratıyoruz. Eligible isek şu şekilde bir sayfa bizi karşılayacak:

![image](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/d8eb0538-cc0a-488d-a452-636cae02fd65)

EVM cüzdanımızı bağlayıp Ethereum Mainnet ağına geçiş yapıyoruz. **Submit Proofs** diyerek sonraki aşamaya geçebiliriz.

![image](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/81440af4-35b0-4c42-9296-9ff6fc5c3989)

**Clone this repo**'ya tıklayıp çıkan repoyu forkluyoruz. Bu repoyu localinizde de açabilirsiniz ama ben [GitHub Codespace](https://github.com/codespaces) kullanmayı tercih ediyorum. Gerekli kütüphaneler hazır olarak geldiği için siz de Codespace kullanabilirsiniz.

![image](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/84e2e8f2-5122-477e-a9ef-d7ba2eef2b2f)

Yukarıdaki şekilde repoyu codespace üzerinden açabilirsiniz.

Repo açıldıktan sonra `.ssh` diye bir klasör oluşturuyoruz. Bu klasöre, daha önce GitHub'a bağlanmak için kullandığımız SSH keyimizi kaydedeceğiz.
Önceden kullandığınız SSH keylerinizi görmek için [GitHub SSH key ayarlarına](https://github.com/settings/keys) gidelim.

![image](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/991ceec0-1560-4582-85c6-ab214bf8c3b2)

Yukarıda gördüğünüz gibi 2 tane SSH keyim var. Birini çok önceden kendi bilgisayarım üzerinden GitHub repolarıma bağlanmak için kullanıyordum. Yüksek ihtimalle siz de eski SSH keyiniz ile claim edebileceksiniz ama şöyle bir sıkıntı var: Eğer SSH keyinizi kaybettiyseniz nasıl claim edebileceğiniz konusunda hiçbir fikrim yok. Ben şansa bala silmemişim ve eski SSH keyimi bilgisayarımın `C:\Users\<KULLANICI ADIM>\.ssh` klasöründe buldum. Codespace üzerinden yeni bir dosya oluşturup ismini `.ssh` yapıyoruz. Bilgisayarımızdaki `id_rsa` ve `id_rsa.pub` dosyalarını codespace'imizin `.ssh` klasörüne sürükleyerek kaydediyoruz. Şimdi proof üretmeye geçebiliriz.

![image](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/6323d864-ad83-48da-8226-cab940821376)

Codespace'imizin klasör yapısı yukarıdaki gibi olacak.

İlk başta şu kodu terminalde kullanıyoruz: `docker build -t dev-reward-script .`

İşlemler bittikten sonra ikinci komutumuzu kullanıyoruz: `docker run -it --network none -v ~/.ssh:/root/.ssh:ro dev-reward-script`

Bizden github kullanıcı adımızı, EVM cüzdan adresimizi ve SSH keyimizin olduğu klasör yolunu isteyecek. SSH keyimizi yolunu şu şekilde veriyoruz ve enterlayıp proof üretmesini bekliyoruz: `.ssh/id_rsa`

![image](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/2822e7fc-b283-421c-b172-939570d4e285)

Bize proofumuzu verdi, şimdi claim sitesine dönüp **Enter your Proof** kısmındaki kutucuğa bu proofu yapıştırıyoruz ve **Submit Proof** diyoruz.

![WhatsApp Görsel 2024-02-29 saat 15 06 53_3e8d895b](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/89635a0a-3e9d-4c3e-8813-6d11f5dbf192)

Yukarıda gördüğünüz gibi bir ekran bizi karşılayacak. Claim 5000 FLT butonuna tıklıyoruz ve cüzdanımıza gelen işleme onay veriyoruz. İşte bu kadar.

![image](https://github.com/eminmtas/fluence-dev-rewards-claim/assets/44838743/6d83e12a-c1e8-483f-af7b-d62465501e62)

Başarılı bir şekilde ödülümüzü claim ettik. Afiedd <3

[Rues](https://x.com/ruesandora0)

[emin.pdf](https://x.com/0x_Emin)
