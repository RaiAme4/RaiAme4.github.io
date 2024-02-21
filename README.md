<!DOCTYPE html>
<html>
<head>
    <title>Website Pertanyaan</title>
    <style>
        /* Gaya CSS untuk tata letak halaman */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #F0DDD7; 
        }
        img {
            width: 50%;
            margin-bottom: 20px;
        }
        .question {
            font-size: 50px;
            margin-bottom: 20px;
        }
        .options {
            display: flex;
            justify-content: center;
        }
        .options button {
            margin: 0 10px;
            padding: 10px 20px;
            font-size: 40px;
            cursor: pointer;
            border-radius: 10px; /* Membuat sudut tombol menjadi melengkung */
            border: none; /* Menghapus b#42445Aorder */
        }
        /* Gaya tambahan untuk warna tombol */
        .options button.yes {
            background-color: #72E985;
            color: white;
        }
        .options button.no {
            background-color: #FF598D;
            color: white;
        }
    </style>
</head>
<body>
    <img id="gambar" src="A.png" alt="Met Ultah!!">
    <div class="question">Selamat ulang tahun!! diterima gak ni ucapannya?</div>
    <div class="options">
        <button class="yes" onclick="jawab('yes')">Yes</button>
        <button class="no" onclick="jawab('no')">No</button>
    </div>
    <script>
        var pertanyaan = [
            {text: "Selamat ulang tahun!! diterima gak ni ucapannya?", image: "A.png"},
            {text: "Eh? Kenapa? kok gak di terima?", image: "B.png"},
            {text: "weh! jawab yes weh", image: "C.png"},
            {text: "jangan tekan no!! tekan yes", image: "D.png"},
            {text: "weh, jangan!!ntar ngebug ke bochi!!", image: "E.png"},
            {text: "jangan tekan no terus!!!!", image: "F.png"},
            {text: "Fadil !!!", image: "G.png"},
            {text: "yo----", image: "H.png"},
            {text: "Woe!! Tekan yes", image: "I.png"},
            {text: "Apa coba..", image: "J.png"},
            {text: "Jangan tekan no", image: "K.png"},
            {text: "Isshhh jangan", image: "L.png"},
            {text: "Woe!!", image: "M.png"},
            {text: "Serius..?", image: "N.png"},
            {text: "Pertanyaan terakhir.. Diterima gak?...", image: "O.png"},
            {text: "oh, padahal udah ku siapin berbulan-bulan.", image: "P.png"}
        ];
        var indexPertanyaan = 0;

        function jawab(jawaban) {
            if (jawaban === 'yes') {
                document.getElementById('gambar').src = 'X.png';
                document.querySelector('.question').style.display = 'none';
                document.querySelector('.options').style.display = 'none';
                return; // Menghentikan eksekusi fungsi setelah ini
            } else {
                if (indexPertanyaan === 15) {
                    window.location.href = 'Bocchi.mp4';
                } else {
                    indexPertanyaan++;
                }
            }
            document.getElementById('gambar').src = pertanyaan[indexPertanyaan].image;
            document.querySelector('.question').textContent = pertanyaan[indexPertanyaan].text;
        }
    </script>
</body>
</html>
