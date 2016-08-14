Deneme dizini oluşturup. Projeyi(ojs'yi) Github'tan clone'landım.
**ojs-docker**'ı da clone'ladım.
<br><img class="" src="1.png" alt="" />

**ojs-docker**daki Readme.md dosyasındaki komutları gerçekleştirdim.
<br><img class="" src="readme.png" alt="" />
<pre><code>docker pull okulbilisim/ojs</code></pre>
<img class="" src="2.png" alt="" />

<pre><code>docker run --name ojsserver -d -p 80:80 -p 3306:3306 -p 27017:27017 -v ~/www/ojs/www:/var/www okulbilisim/ojs</code></pre>
<br><img class="" src="3.png" alt="" />
*__docker: Error response from daemon: Conflict. The name "/ojsserver" is already in use by container a660e5002b3ee744e73439880fe31c4d3ecf4f870a9db42b94d6cfa3d44c902f. You have to remove (or rename) that container to be able to reuse that name..
See 'docker run --help'__*
<br>Bu hata ile karşılaştım. Sanırsam daha önce aynı isimde container olduğunu belirtiyor.

<pre><code>docker build -t="okulbilisim/ojsdocker" ./</code></pre>
<br><img class="" src="4.png" alt="" />
<br><img class="" src="5.png" alt="" />
<font face="Arial" color="red">+ apt-get update</font>
<br><font face="Arial" color="red">+ apt-get install -y openjdk-8-jdk=8u45-b14-2~bpo8+2 ca-certificates-java=20140324</font>
<br><font face="Arial" color="red">E: Version '8u45-b14-2~bpo8+2' for 'openjdk-8-jdk' was not found</font>
<br> ile karşılaştım.

<br><img class="" src="12container.png" alt="" />
12.containerdan sonra bir sıkıntı yaşıyorum. Anlayamadım.
