<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tienda de Repostería</title>
    <style>
        body {
            background-color: #FFE5B4;
            font-family: 'Arial', sans-serif;
            color: #333;
            margin: 0;
            padding: 0;
            text-align: center;
        }

        h1 {
            color: #A0522D;
            margin: 20px 0;
            font-size: 2.5em;
        }

        h2 {
            color: #A0522D;
        }

        #productos {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 15px;
            padding: 20px;
            margin-top: 20px;
        }

        .producto {
            background-color: #fff;
            border: 2px solid #F0A07E;
            border-radius: 8px;
            padding: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .producto img {
            width: 80px;
            height: 80px;
            margin-bottom: 10px;
            border-radius: 8px;
        }

        .producto label {
            display: block;
            font-size: 1.1em;
            font-weight: bold;
            color: #A0522D;
            margin-bottom: 5px;
        }

        button {
            background-color: #A0522D;
            color: #fff;
            padding: 12px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            font-weight: bold;
            cursor: pointer;
            margin-top: 20px;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #8B4513;
        }

        .factura {
            background-color: #FFE5B4;
            padding: 20px;
            display: none;
        }
    </style>
</head>
<body>
    <h1>Bienvenidos a la Tienda de Repostería</h1>
    <p>¡Descubre nuestros deliciosos productos y haz tu pedido!</p>

    <div id="productos">
        <!-- Lista de 15 productos con imágenes y campos de cantidad -->
        <div class="producto">
            <img src="https://pastelerialaceleste.cl/wp-content/uploads/2022/05/deco_chocolate-1x1-1.jpg" alt="Pastel de Chocolate">
            <label>Pastel de Chocolate (Q300)</label>
            <input type="number" id="pastelChocolate" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://pasteleriakolonia.com/wp-content/uploads/2020/07/WhatsApp-Image-2023-06-07-at-10.58.58-PM-1.jpeg" alt="Pastel de Vainilla">
            <label>Pastel de Vainilla (Q280)</label>
            <input type="number" id="pastelVainilla" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://www.allrecipes.com/thmb/bHxzoJU6qomQtu67YpQY-ZJiH9Q=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/2385598-vegan-cupcakes-jcalliagas-1x1-1-3167c2e67b834943acca9bfa9564b786.jpg" alt="Cupcakes">
            <label>Cupcakes (docena) (Q150)</label>
            <input type="number" id="cupcakes" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://fedecocina.net/static/d60a5168b8cfa74ef55b91094dcd6aa9/02dff/brownies-facil-y-rapido-1x1.jpg" alt="Brownies">
            <label>Brownies (Q120)</label>
            <input type="number" id="brownies" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://cdn.cookwithbelula.com/receta/galletas-chispas-chocolate/galletas-chispas-chocolate-1x1.webp" alt="Galletas con Chispas">
            <label>Galletas con Chispas (docena) (Q100)</label>
            <input type="number" id="galletasChispas" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://static2.diariovasco.com/www/multimedia/202104/29/media/cortadas/macarons-franceses-receta-k6FG-U140210492029SsH-624x385@Diario%20Vasco.jpg" alt="Macarons">
            <label>Macarons (Q200)</label>
            <input type="number" id="macarons" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://media-cldnry.s-nbcnews.com/image/upload/newscms/2023_34/2027266/cheesecake-bars-1x1-zz-230824.jpg" alt="Cheesecake">
            <label>Cheesecake (Q350)</label>
            <input type="number" id="cheesecake" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://cdn.cookwithbelula.com/receta/tarta-limon-merengue/tarta-limon-merengue-1x1.webp" alt="Panquecito de Limón">
            <label>Panquecito de Limón (Q90)</label>
            <input type="number" id="panquesitoLimon" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://ds1e83w8pn0gs.cloudfront.net/fotosmultisite/502613-1.jpg" alt="Tarta de Frutas">
            <label>Tarta de Frutas (Q250)</label>
            <input type="number" id="tartaFrutas" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://cdn.cookwithbelula.com/receta/alfajores-de-maicena/alfajores-de-maicena-rhng-1x1.webp" alt="Alfajores">
            <label>Alfajores (docena) (Q150)</label>
            <input type="number" id="alfajores" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://ds1e83w8pn0gs.cloudfront.net/fotosmultisite/502476-1.jpg" alt="Pastel de Zanahoria">
            <label>Pastel de Zanahoria (Q320)</label>
            <input type="number" id="pastelZanahoria" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://goldbelly.imgix.net/uploads/showcase_media_asset/image/158197/Martha-Stewart-x-Goldbelly-1.5.22-242-72ppi-1x1.jpg?ixlib=react-9.9.0&ar=1%3A1&fit=crop&w=3840&auto=format" alt="Croissants">
            <label>Croissants (media docena) (Q180)</label>
            <input type="number" id="croissants" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://i.pinimg.com/originals/41/f2/3f/41f23f3290646aedf5e01e25fcf9901e.jpg" alt="Donas">
            <label>Donas (docena) (Q120)</label>
            <input type="number" id="donas" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://www.lindalicious.at/wp-content/uploads/2020/12/Tiramisu-1x1-1-800x600.jpg" alt="Tiramisú">
            <label>Tiramisú (Q200)</label>
            <input type="number" id="tiramisu" value="0" min="0">
        </div>
        <div class="producto">
            <img src="https://as1.ftcdn.net/v2/jpg/03/05/92/58/1000_F_305925852_XHJXQXY7PvZJG1PDl8cfptaIyQvFu6EI.jpg" alt="Eclairs">
            <label>Eclairs (media docena) (Q160)</label>
            <input type="number" id="eclairs" value="0" min="0">
        </div>
    </div>

    <button onclick="finalizarCompra()">Finalizar Compra</button>

    <div id="factura" class="factura">
        <!-- Aquí se mostrará la factura -->
    </div>

    <script>
        function finalizarCompra() {
            const precios = {
                pastelChocolate: 300,
                pastelVainilla: 280,
                cupcakes: 150,
                brownies: 120,
                galletasChispas: 100,
                macarons: 200,
                cheesecake: 350,
                panquesitoLimon: 90,
                tartaFrutas: 250,
                alfajores: 150,
                pastelZanahoria: 320,
                croissants: 180,
                donas: 120,
                tiramisu: 200,
                eclairs: 160
            };

            let total = 0;
            let facturaHTML = '<h2>Factura de Compra</h2><ul>';

            for (let producto in precios) {
                let cantidad = parseInt(document.getElementById(producto).value) || 0;
                if (cantidad > 0) {
                    let costoProducto = cantidad * precios[producto];
                    total += costoProducto;
                    facturaHTML += `<li>${producto.replace(/([A-Z])/g, ' $1')}: Q${costoProducto} (${cantidad} x Q${precios[producto]})</li>`;
                }
            }

            facturaHTML += `</ul><h3>Total: Q${total}</h3>`;
            document.getElementById("productos").style.display = "none";
            document.querySelector("button").style.display = "none";
            document.getElementById("factura").style.display = "block";
            document.getElementById("factura").innerHTML = facturaHTML;
        }
    </script>
</body>
</html>
