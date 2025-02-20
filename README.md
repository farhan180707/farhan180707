<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restoran Sambal Bakar</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(45deg, #ff5733, #c70039);
        }
        table {
            width: 100%;
            border-collapse: collapse;
            table-layout: fixed; /* Ensures even column widths */
        }
        .header {
            background: linear-gradient(45deg, #900C3F, #C70039);
            color: white;
            text-align: center;
            padding: 30px;
        }
        .nav {
            background-color: rgba(0,0,0,0.8);
            text-align: center;
            padding: 15px;
            position: sticky;
            top: 0;
        }
        .nav a {
            text-decoration: none;
            color: white;
            margin: 0 15px; /* Reduced margin for better spacing */
            font-weight: bold;
            transition: 0.3s;
            padding: 10px 15px;
            border-radius: 5px;
        }
        .nav a:hover {
            background-color: #ff5733;
            transform: scale(1.1);
        }
        .content {
            padding: 40px 20px;
            text-align: center;
            min-height: 500px;
            background-color: rgba(255,255,255,0.9);
        }
        .footer {
            background-color: rgba(0,0,0,0.9);
            color: white;
            text-align: center;
            padding: 20px;
        }
        .menu-list {
            display: flex;
            flex-wrap: wrap; /* Allows items to wrap onto multiple lines */
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }
        .menu-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            width: 25%; /* Adjust width as needed */
            min-width: 200px; /* Minimum width to prevent collapse */
            text-align: center; /* Center text within card */
        }
        .menu-card img {
            max-width: 100%;
            height: auto; /* Maintain aspect ratio */
            margin-bottom: 10px;
        }

    </style>
</head>
<body>
<table>
    <tr>
        <td colspan="2" class="header">
            <h1>Restoran Sambal Bakar</h1>
            <h3>Lezatnya Pedas yang Menggoda!</h3>
        </td>
    </tr>
    <tr>
        <td colspan="2" class="nav">
            <a onclick="loadPage('home')">Home</a>
            <a onclick="loadPage('menu')">Menu</a>
            <a onclick="loadPage('order')">Order</a>
            <a onclick="loadPage('contact')">Contact</a>
        </td>
    </tr>
    <tr>
        <td class="content" id="content" colspan="2">
            <h2>Selamat Datang di Restoran Sambal Bakar!</h2>
            <p>Rasakan kenikmatan makanan pedas khas kami dengan cita rasa autentik!</p>
        </td>
    </tr>
    <tr>
        <td colspan="2" class="footer">
            <p>&copy; 2024 Restoran Sambal Bakar • Follow us: 
                <a href="#" style="color: #ff5733">Instagram</a> | 
                <a href="#" style="color: #ff5733">Twitter</a>
            </p>
        </td>
    </tr>
</table>

<script>
    function loadPage(page) {
        let content = document.getElementById('content');

        if (page === 'menu') {
            content.innerHTML = `
                <h2>Menu Kami</h2>
                <div class="menu-list">
                    <div class="menu-card">
                        <img src="https://assets.onecompiler.app/439mbarfp/439mr5uwp/076541100_1716699691-Sepiring_ayam_bakar_pedas_manis._Liputan6.comIGcheche_kitchen.jpg" alt="Ayam Sambal Bakar">
                        <h3>Ayam Sambal Bakar</h3>
                        <p>IDR 25.000</p>
                    </div>
                    <div class="menu-card">
                        <img src="https://assets.onecompiler.app/439mbarfp/439mr5uwp/5fdb3cd0c1525.jpg" alt="Ikan Sambal Bakar">
                        <h3>Ikan Sambal Bakar</h3>
                        <p>IDR 30.000</p>
                    </div>
                    <div class="menu-card">
                        <img src="https://assets.onecompiler.app/439mbarfp/439mr5uwp/photo.jpg" alt="Tahu Tempe Bakar">
                        <h3>Tahu Tempe Bakar</h3>
                        <p>IDR 15.000</p>
                    </div>
                </div>
            `;
        } else if (page === 'order') {
            content.innerHTML = `
                <h2>Pesan Sekarang</h2>
                <form>
                    <input type="text" placeholder="Nama" required>
                    <input type="email" placeholder="Email" required>
                    <select required>
                        <option value="">Pilih Menu</option>
                        <option>Ayam Sambal Bakar</option>
                        <option>Ikan Sambal Bakar</option>
                        <option>Tahu Tempe Bakar</option>
                    </select>
                    <button type="submit">Pesan Sekarang</button>
                </form>
            `;
        } else if (page === 'contact') {
            content.innerHTML = `
                <h2>Kontak Kami</h2>
                <p>📞 081289779275</p>
                <p>📧 sambalbakar18@gmail.com</p>
                <p>📍 Jl. Pedas No. 99, Jakarta</p>
            `;
        } else {
            content.innerHTML = `
                <h2>Selamat Datang di Restoran Sambal Bakar!</h2>
                <p>Rasakan kenikmatan makanan pedas khas kami dengan cita rasa autentik!</p>
            `;
        }
    }
</script>

</body>
</html>
