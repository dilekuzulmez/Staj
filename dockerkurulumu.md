## UBUNTU TRUSTY 14.04 [LTS] İÇİN DOCKER KURULUMU
Öncelikle Docker için Ubuntu sürümü ne olursa olsun 64-bit kurulum gerektirir. Ayrıca kernel sürümü en az 3.10 olması gerekir. En son kernel sürümü 3.10 alt veya daha yeni bir sürümü de kabul edilebilir.

Bilgisayarınızdaki kernel sürümünü kontrol etmek için terminal açın(CTRL+ALT+T) ve kernel sürümünü öğrenmek için:
<br>uname -r

Eğer kernel sürümünüz Docker için uygunsa kuruluma başlayabiliriz.
Yeniden bir terminal açıp root olalım yada sudo ayrıcalıklarına sahip bir kullanıcı ile terminali açalım.

1.Önce bir güncelleme yapalım :
<pre><code>$ sudo apt-get update</code></pre>

2.Ardından CA sertifikasını indiriyoruz:
<pre><code>$ sudo apt-get install apt-transport-https ca-certificates</code></pre>

3.GPG anahtarını ekliyoruz:
<pre><code>$ sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D</code></pre>

4./etc/apt/sources.list.d/docker.list dosyasını istediğiniz herhangi bir editör ile açalım, ben vim kullanıyorum :
<pre><code>$ vim /etc/apt/sources.list.d/docker.list</code></pre>

<br>Dosya mevcut değilse, oluşturalım.
<br>İçinde herhangi bir şey yazıyorsa, silelim.

<br>Ubuntu Trusty 14.04 (LTS) için dosyanın içerisine bu satırı ekleyelim:
<pre><code> deb https://apt.dockerproject.org/repo ubuntu-trusty main</code></pre>
<br>ve kaydedip(:wq) dosyayı kapatalım.

5.Tekrar güncelleme yapalım:
<pre><code># apt-get update</code></pre>

6.Varsa eski repoları temizleyelim:
<pre><code>$ sudo apt-get purge lxc-docker</code></pre>

7.APT olduğunu doğrulayalım:
<pre><code># apt-cache policy docker-engine</code></pre>

###### Linux-image-extra paketini kernel sürümü için yükleyelim.

<br>1.Önce yine güncelleme yapalım:
<pre><code>$ sudo apt-get update</code></pre>

2.Önerilen paketi yükleyelim:
<pre><code>$ sudo apt-get install linux-image-extra-$(uname -r)</code></pre>

<br>Devam edelim ve Docker'ı yükleyelim.
<br>NOT: Ubuntu 14.04 ya da 12.04 için ***apparmor*** gereklidir. Apparmor kurulumu için: <pre><code># apt-get install apparmor</code></pre>

#### KURULUM

1.Docker kurulumu için ön koşulları hallettikten sonra root olalım yada sudo yetkisine sahip kullanıcı ile Ubuntuyu başlatalım.

2.APT paketlerini güncelleyerek başlayalım:
<pre><code>$ sudo apt-get update</code></pre>

<br>3.Docker yüklemek için:
<pre><code>$ sudo apt-get install docker-engine</code></pre>

4.Docker daemon başlatmak için:
<pre><code>$ sudo service docker start</code></pre>

5.Doğrulama kontrolü için:
<pre><code>$ sudo docker run hello-world</code></pre>

Bu komut bir test görüntüsü indirir ve konteyner çalıştırır. Konteyner çalıştığında bilgilendirici mesaj görünür ve sonra çıkar.
<br>:tada:
