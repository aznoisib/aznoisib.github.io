Belajar membuat repository/halaman github dengan metode fundamental  & di sertai cara menyelesaikan/solved masalah yang terjadi menggunakan referensi, seputar info untuk kenyataanya ini pun hanya rangkuman tidak mendalami penuh seputar git karna bisa memakan waktu cukup lama hanya untuk satu pelajaran git ini dalam banyak kasus masalah pun terus terjadi dan selalu ada masalah baru yang tidak kunjung habis, maka dari itu di sediakan referensi untuk detailnya situs sekaligus sebagai backlink/credit si penulis,

 praktek & pahami -> cari referensi sebanyak2nya dengan cara ini kesalahan pun bisa di minimalisir dengan bukti referensi. sebaiknya di arsipkan saja referensi tersebut untuk di pelajari/dipahami --> praktek, dengan cara itu lah program di bangun itu baru sepengetahuan saya saja selama membuat program dengan metode fundamental otodidak. silahkan di bookmark/fork karena disini saya akan update ilmu seputar git dan github menggunakan gambar

 kutipan terakhir repository itu nama lain/synonim dari berkas dan folder beserta isinya, jadi intinya kita harus manual nge push menjalankan command setiap perubahan yang di lakukan di berkas komputer 
apa manfaat program git ini kita bisa log atau backup/restore setiap perubahan yang kita lakukan di berkas seperti file yang di hapus bisa di kembalikan/restore dengan ketentuan harus melakukan command `git push` di setiap perubahan 

## Git commander On Windows

`git remote rm origin` untuk menghapus akses remote ke git url di gunakan hanya ketika terkoneksi ke remote saja, bagaimana mengecek apakah kita sedang terkonseksi ke remote git url ?

`git branch -ra` untuk mengecek branch remote dan local dengan cara ini kita bisa mengetahui sedang terkoneksi remote atau tidak

Example:
```bash
git remote rm origin https://github.com/username-anda/example.git
git branch -ra
```

![Image](https://raw.githubusercontent.com/aznoisib/aznoisib.github.io/master/docs/removeremote.PNG)

* warna hijau branch local warna merah remote branch

![Image](https://raw.githubusercontent.com/aznoisib/aznoisib.github.io/master/docs/existingremote.PNG)

* fatal: remote origin already exists. di karenakan anda sudah terkoneksi ke remote git url jadi hanya tinggal melakukan perubahan repo local lalu jalan command di bawah ini

`git add .` menambahkan semua isi di folder repository local yang berada di komputer anda ke program git   
`git push -u origin master` mentransfer repo local ke remote git url/repository online berbasis git

Example:
```bash
git add .
git push -u origin master
```




![Image](https://raw.githubusercontent.com/aznoisib/aznoisib.github.io/master/docs/nochange.PNG)

* Everything up-to-date
Branch 'master' set up to track remote branch 'master' from 'origin'.
di karenakan tidak adanya perubahan repo local yang terjadi misal anda tidak melakukan save file lalu anda menjalankan command `git add .` & `git push -u origin master`  dan ternyata pesan ini masih muncul juga meskipun sudah melakukan perubahan langsung saja jalankan command

```bash
git add .
git commit -am "my comment"
git push
```

hasilnya:

![Image](https://raw.githubusercontent.com/aznoisib/aznoisib.github.io/master/docs/images/adds.PNG)

coba lagi jalankan command 

```bash
git add .
git commit -am "my comment"
git push
```

di karenakan anda tidak melakukan perubahan apapun hasilnya:

![Image](https://raw.githubusercontent.com/aznoisib/aznoisib.github.io/master/docs/images/addr.PNG)

coba sekarang anda lakukan perubahan seperti merubah isi yang ada di folder/berkas/repository lokal anda
misalkan save file atau delete file atau menambahkan file lalu jalankan lagi command


```bash
git add .
git commit -am "my comment"
git push
```

hasilnya berhasil tidak ada pesan gagal!

![Image](https://raw.githubusercontent.com/aznoisib/aznoisib.github.io/master/docs/images/addsc.PNG)  
credits: https://stackoverflow.com/questions/2936652/git-push-wont-do-anything-everything-up-to-date


## Initial repo

untuk pertama kali membuat repository github menggunakan Os windows jalankan

Windows command Prompt

```bash
git init 
git add .
git commit -m "first commit" 
git remote add origin https://github.com/username-anda/example.git
git push -u origin master
```

## Existing repo

untuk repositry github yang sudah ada menggunakan Os windows jalankan

Windows command Prompt

```bash
git add .
git commit -m "my commit"
git remote set-url origin https://github.com/username-anda/example.git
git push -u origin master
```

## Reffrences
- menambahkan
  - https://git-scm.com/book/en/v2/Git-Tools-Submodules
  - And this

https://chrisjean.com/git-submodules-adding-using-removing-and-updating/  
https://eka.gdn/programming/cara-logout-dari-git-credential-manager/  
https://stackoverflow.com/questions/18842120/git-pushing-to-a-private-repo  
https://stackoverflow.com/questions/10116373/git-push-error-repository-not-found  
https://stackoverflow.com/questions/20413459/fatal-not-a-git-repository-or-any-of-the-parent-directories-git  
https://stackoverflow.com/questions/28238037/git-log-out-user-from-command-line  
https://guides.github.com/features/mastering-markdown/  
https://community.atlassian.com/t5/Git-questions/fatal-No-such-remote-origin-after-git-remote-set-url-origin/qaq-p/401456  
https://stackoverflow.com/questions/43863522/your-push-would-publish-a-private-email-address-error  
https://git-scm.com/book/en/v2/Git-Internals-Maintenance-and-Data-Recovery  
https://gist.github.com/jbgo/1944238  
https://medium.com/flawless-app-stories/useful-git-commands-for-everyday-use-e1a4de64037d  
https://stackoverflow.com/questions/26626256/how-to-insert-a-line-break-br-in-markdown