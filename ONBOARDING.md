# Introduction

Selamat datang di DEN Econ Lab. Di DEN Econ Lab, kita fokus untuk memperbanyak tulisan dan brownbag seminars. Gak hanya itu, kita berusaha agar semua tulisan dan kodingan kita terdokumentasi dengan baik, transparan dan dapat direplikasi oleh siapa saja. Untuk melakukan hal tersebut, DEN Econ Lab menggunakan beberapa software yang sudah cukup standar untuk dipakai di berbagai lab akademis. Jika ada yang ingin ditanyakan bisa samperin Imed (DE2)

# Piranti lunak

Berikut ini adalah beberapa hal yang harus anda install untuk mengintegrasikan berbagai software yang dipakai di DEN Econ Lab:

## Manajemen proyek
1. [Github desktop](https://desktop.github.com/download/) adalah software yang akan kita gunakan untuk version control + distribusi.

## Komputasi:
1. [Anaconda](https://www.anaconda.com/download) untuk Distribusi Python. Anaconda sekarang membutuhkan email untuk download. Bisa download di user aja, nanti dia akan muncul di `users/<username>/Anaconda3/`.
2. [R](https://cran.rstudio.com/). Download `base` dan `Rtools` saja. Install dengan settingan standar.
3. [Quarto](https://quarto.org/docs/get-started/) untuk menulis.
4. [TeX Live](https://www.tug.org/texlive/) untuk ngerender latex.

## IDE:
Kita akan berinteraksi dengan semua piranti lunak di atas melalui sebuah IDE(Integrated Development Environment). Kita cuma perlu install 1 aja sebenarnya, tapi kalo sambil mau eksplor boleh juga diinstall lebih dari satu untuk memilih nantinya lebih suka make yang mana.
1. [VS Code](https://code.visualstudio.com/download) adalah IDE paling standar. Saya paling rekomendasiin IDE yang satu ini. Ketika diinstall, jangan lupa centang 'add "open with code"` (lihat gambar).

![Source: [Stack Overflow](https://stackoverflow.com/questions/37306672/visual-studio-code-open-with-code-does-not-appear-after-right-clicking-a-folde)](vscode.jpg)

3. [RStudio](https://posit.co/download/rstudio-desktop/) adalah IDE yang biasanya digunakan oleh pengguna R. Dulu saya juga mulai dari sini dan masih paling intuitif kalau kita pake R. Tapi saya sendiri lebih sering pakai VSCode sekarang. Jika anda pengguna RStudio boleh juga mulai nyoba pindah ke VS Code.
4. [Positron](https://positron.posit.co/) adalah IDE baru bikinan Posit, perusahaan di balik RStudio. IDE ini masih baru dan arahnya membuat IDE serupa RStudio tapi mengandalkan ekosistem plugin VS Code yang lebih kaya.
5. [Google Antigravity](https://antigravity.google/download) adalah IDE baru dari Google yang tujuannya mengoptimalkan asisten koding berbasis agen. My experience so far with this IDE is pretty good.

## VS Code

Jika sudah install VS Code, ada beberapa setting extra yang akan membuat hidup anda lebih nyaman. Ini gak wajib tapi mempermudah aja sih. Pertama adalah menggunakan anaconda prompt sebagai terminal default di VS Code. Lakukan langkah-langkah ini:

1. Buka VS Code.
2. Tekan `Ctrl + Shift + P` lalu ketik "Open User Settings (JSON)".
3. Tambahin entri di bawah ini. Jangan lupa perhatikan indentasi yah.

```{=JSON}
  "terminal.integrated.profiles.windows": {
      "Conda": {
          "source": "PowerShell",
          "icon": "terminal-powershell",
          "args": [
              "-ExecutionPolicy", "ByPass",
              "-NoExit",
              "-Command", "& 'C:\\Users\\YOUR_USERNAME\\anaconda3\\shell\\condabin\\conda-hook.ps1'; conda activate 'base'"
          ]
      }
  },
  "terminal.integrated.defaultProfile.windows": "Conda"
```
jangan lupa `YOUR_USERNAME` diganti jadi username di komputer anda.

kedua, plugin. jangan lupa install-install plugin yang akan mempermudah hidup anda. Yg wajib ada adalah Jupyter, Quarto, dan R. Kalau anda pake AI seperti Claude, ChatGPT atau Gemini, mereka juga punya plugins di store-nya VS Code.

