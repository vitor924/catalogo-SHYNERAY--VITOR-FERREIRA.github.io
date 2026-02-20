           
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Motos Shineray - Catalogo Oficial</title>
    <meta name="description" content="Catalogo completo de motos Shineray. Financiamento facilitado. Fale conosco pelo WhatsApp!">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #8B0000 0%, #DC143C 100%);
            color: white;
            padding: 15px 20px;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
        }

        .logo span {
            color: #FF6B6B;
        }

        .header-cta {
            background: #25D366;
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .header-cta:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.4);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #8B0000 0%, #B22222 50%, #DC143C 100%);
            color: white;
            padding: 120px 20px 60px;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto 30px;
        }

        .hero-badge {
            display: inline-block;
            background: #FFD700;
            color: #8B0000;
            padding: 10px 25px;
            border-radius: 25px;
            font-weight: 700;
            font-size: 1.1rem;
            animation: pulse 2s infinite;
        }

        .hero-promo {
            display: inline-block;
            background: white;
            color: #DC143C;
            padding: 15px 30px;
            border-radius: 10px;
            font-weight: 700;
            font-size: 1.4rem;
            margin-top: 20px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
            animation: pulse 2s infinite;
            border: 3px solid #FFD700;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        /* Vendedor Info */
        .vendedor-section {
            background: white;
            padding: 30px 20px;
            text-align: center;
            border-bottom: 3px solid #DC143C;
        }

        .vendedor-card {
            max-width: 500px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .vendedor-avatar {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #DC143C, #FF6B6B);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
        }

        .vendedor-info h3 {
            color: #8B0000;
            font-size: 1.3rem;
        }

        .vendedor-info p {
            color: #666;
        }

        /* Catalog Section */
        .catalog {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .catalog-title {
            text-align: center;
            margin-bottom: 40px;
        }

        .catalog-title h2 {
            font-size: 2rem;
            color: #8B0000;
            margin-bottom: 10px;
        }

        .catalog-title p {
            color: #666;
        }

        .moto-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
        }

        .moto-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .moto-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .moto-image {
            width: 100%;
            height: 180px;
            object-fit: contain;
            background: #f9f9f9;
            padding: 10px;
        }

        .moto-info {
            padding: 20px;
        }

        .moto-name {
            font-size: 1.2rem;
            font-weight: 700;
            color: #333;
            margin-bottom: 5px;
        }

        .moto-price {
            font-size: 1.4rem;
            color: #DC143C;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .moto-price small {
            font-size: 0.8rem;
            color: #999;
            font-weight: 400;
        }

        .btn-whatsapp {
            display: block;
            background: #25D366;
            color: white;
            text-align: center;
            padding: 12px 20px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.2s, transform 0.2s;
        }

        .btn-whatsapp:hover {
            background: #1da851;
            transform: scale(1.02);
        }

        .btn-whatsapp svg {
            vertical-align: middle;
            margin-right: 8px;
        }

        /* Footer */
        .footer {
            background: #8B0000;
            color: white;
            padding: 40px 20px;
            text-align: center;
        }

        .footer h3 {
            margin-bottom: 20px;
        }

        .footer-whatsapp {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: #25D366;
            color: white;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 20px;
            transition: transform 0.2s;
        }

        .footer-whatsapp:hover {
            transform: scale(1.05);
        }

        .footer p {
            opacity: 0.8;
            font-size: 0.9rem;
        }

        /* WhatsApp Float Button */
        .whatsapp-float {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.4);
            z-index: 999;
            transition: transform 0.2s;
            text-decoration: none;
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
        }

        .whatsapp-float svg {
            width: 35px;
            height: 35px;
        }

        /* Form Section */
        .form-section {
            background: #FFEBEE;
            padding: 30px 20px;
            border-bottom: 3px solid #DC143C;
        }

        .form-container {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .form-container h3 {
            color: #8B0000;
            margin-bottom: 5px;
            font-size: 1.3rem;
        }

        .form-container > p {
            color: #666;
            margin-bottom: 20px;
            font-size: 0.9rem;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            text-align: left;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-weight: 600;
            color: #8B0000;
            margin-bottom: 5px;
            font-size: 0.9rem;
        }

        .form-group input {
            padding: 12px 15px;
            border: 2px solid #FFCDD2;
            border-radius: 8px;
            font-size: 1rem;
            font-family: 'Poppins', sans-serif;
            transition: border-color 0.2s, box-shadow 0.2s;
        }

        .form-group input:focus {
            outline: none;
            border-color: #DC143C;
            box-shadow: 0 0 0 3px rgba(220, 20, 60, 0.2);
        }

        .form-group-checkbox {
            display: flex;
            align-items: center;
            gap: 10px;
            padding-top: 25px;
        }

        .form-group-checkbox input[type="checkbox"] {
            width: 20px;
            height: 20px;
            accent-color: #DC143C;
            cursor: pointer;
        }

        .form-group-checkbox label {
            font-weight: 600;
            color: #8B0000;
            font-size: 0.9rem;
            cursor: pointer;
        }

        .form-group input::placeholder {
            color: #aaa;
        }

        /* Responsive */
        @media (max-width: 600px) {
            .header-content {
                flex-direction: column;
                gap: 10px;
            }

            .hero h1 {
                font-size: 1.8rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .moto-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-content">
            <div class="logo">SHINERAY <span>Motos</span></div>
            <a href="#" class="header-cta" id="headerWhatsapp">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
                </svg>
                Fale Conosco
            </a>
        </div>
    </header>

    <!-- Hero -->
    <section class="hero">
        <h1>Realize o Sonho da Sua Moto!</h1>
        <p>Catalogo completo de motos Shineray com financiamento facilitado. Escolha seu modelo e fale direto comigo!</p>
        <div class="hero-badge">Financiamento Pre-Aprovado</div>
        <br>
        <div class="hero-promo">* Somente R$ 10,00 de entrada! *</div>
    </section>

    <!-- Vendedor -->
    <section class="vendedor-section">
        <div class="vendedor-card">
            <div class="vendedor-avatar">
                <svg width="40" height="40" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
                </svg>
            </div>
            <div class="vendedor-info">
                <h3 id="vendedorNome">Consultor Shineray</h3>
                <p>Representante Comercial Autorizado</p>
            </div>
        </div>
    </section>

    <!-- Formulario de Contato -->
    <section class="form-section">
        <div class="form-container">
            <h3>Preencha seus dados para facilitar o atendimento</h3>
            <p>Ao clicar em uma moto, seus dados serao enviados junto com a mensagem</p>
            <div class="form-grid">
                <div class="form-group">
                    <label for="clienteNome">Seu Nome</label>
                    <input type="text" id="clienteNome" placeholder="Digite seu nome completo">
                </div>
                <div class="form-group">
                    <label for="clienteCpf">CPF</label>
                    <input type="text" id="clienteCpf" placeholder="000.000.000-00" maxlength="14">
                </div>
                <div class="form-group">
                    <label for="clienteTelefone">WhatsApp</label>
                    <input type="text" id="clienteTelefone" placeholder="(00) 00000-0000" maxlength="15">
                </div>
                <div class="form-group">
                    <label for="clienteNascimento">Data de Nascimento</label>
                    <input type="date" id="clienteNascimento">
                </div>
                <div class="form-group-checkbox">
                    <input type="checkbox" id="clienteCnh">
                    <label for="clienteCnh">Possui CNH?</label>
                </div>
            </div>
        </div>
    </section>

    <!-- Catalogo -->
    <section class="catalog">
        <div class="catalog-title">
            <h2>Nosso Catalogo</h2>
            <p>Clique em "Tenho Interesse" para falar comigo pelo WhatsApp</p>
        </div>
        <div class="moto-grid" id="motoGrid">
            <!-- Motos serao inseridas via JavaScript -->
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <h3>Ficou com alguma duvida?</h3>
        <a href="#" class="footer-whatsapp" id="footerWhatsapp">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
            </svg>
            Chamar no WhatsApp
        </a>
        <p style="margin-bottom: 15px;">Shineray - Qualidade e Economia</p>
        <div style="border-top: 1px solid rgba(255,255,255,0.2); padding-top: 20px; margin-top: 10px;">
            <p style="font-size: 0.8rem; opacity: 0.7; margin-bottom: 8px;">
                Este catalogo exibe produtos e ao clicar voce envia uma mensagem direta para o WhatsApp do vendedor.
            </p>
            <p style="font-size: 0.75rem; opacity: 0.5;">
                Desenvolvido por Vitor ferreira | <a href="mailto:vitorferre@gmail.com" style="color: #FF6B6B; text-decoration: none;">vitor </a>
                - Catalogos e sistemas sob medida
            </p>
        </div>
    </footer>

    <!-- WhatsApp Float -->
    <a href="#" class="whatsapp-float" id="whatsappFloat">
        <svg viewBox="0 0 24 24" fill="currentColor">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
        </svg>
    </a>

    <script>
        // ==========================================
        // CONFIGURACAO DO VENDEDOR - EDITE AQUI!
        // ==========================================
        const CONFIG = {
            nomeVendedor: "Vitor Ferreira",
            telefoneVendedor: "6199597429", // Apenas numeros, com DDD
            cidade: "Brasilia"
        };

        // Catalogo de motos Shineray
        const MOTOS = [
            {         {
                nome: "JET 50 SS",
                preco: "R$ 11.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2023/06/Jet-50s.webp"
            },
                nome: "JET 125SS",
                preco: "R$ 12.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2023/06/JET-125ss.webp"
            },
            {
                nome: "RIO 125 EFI",
                preco: "R$ 12.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2023/12/RIO-125-EFI.webp"
            },
            {
                nome: "JEF 150s",
                preco: "R$ 15.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2023/08/JEF-150s.webp"
            },
          
            {
                nome: "URBAN 150 EFI",
                preco: "R$ 21.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2025/01/URBAN-150-EFI.webp"
            },
            {
                nome: "SHI 175",
                preco: "R$ 16.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2023/06/SHI-175-1.webp"
            },
            {
                nome: "SHI 175s EFI",
                preco: "R$ 14.990,00",
                imagem: "https://www.autocerto.com/fotos/4448/3778505/15_022941.jpg"
            },
            {
                nome: "STORM 200 EFI",
                preco: "R$ 23.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2024/08/Storm.webp"
            },
            {
                nome: "250F",
                preco: "R$ 21.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2024/12/250F.webp"
            },
            {
                nome: "Denver",
                preco: "R$ 27.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2024/12/Denver.webp"
            }
       {
                nome: "Titanium 250",
                preco: "R$ 27.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2024/12/Titanium-1.webp"
            }
     {
                nome: "Iron 250",
                preco: "R$ 26.990,00",
                imagem: "https://www.shineray.com.br/wp-content/uploads/2025/01/Iron.webp"
            }
        ];  

        // Elementos do formulario
        const inputNome = document.getElementById('clienteNome');
        const inputCpf = document.getElementById('clienteCpf');
        const inputTelefone = document.getElementById('clienteTelefone');
        const inputNascimento = document.getElementById('clienteNascimento');
        const inputCnh = document.getElementById('clienteCnh');

        // Mascara CPF
        inputCpf.addEventListener('input', function(e) {
            let valor = e.target.value.replace(/\D/g, '').slice(0, 11);
            let formatado = '';
            for (let i = 0; i < valor.length; i++) {
                if (i === 3 || i === 6) formatado += '.';
                if (i === 9) formatado += '-';
                formatado += valor[i];
            }
            e.target.value = formatado;
        });

        // Mascara Telefone
        inputTelefone.addEventListener('input', function(e) {
            let valor = e.target.value.replace(/\D/g, '').slice(0, 11);
            let formatado = '';
            for (let i = 0; i < valor.length; i++) {
                if (i === 0) formatado += '(';
                if (i === 2) formatado += ') ';
                if (i === 7) formatado += '-';
                formatado += valor[i];
            }
            e.target.value = formatado;
        });

        // Funcao para formatar data
        function formatarData(dataStr) {
            if (!dataStr) return '';
            const partes = dataStr.split('-');
            if (partes.length === 3) {
                return `${partes[2]}/${partes[1]}/${partes[0]}`;
            }
            return dataStr;
        }

        // Funcao para obter dados do formulario
        function getDadosCliente() {
            return {
                nome: inputNome.value.trim(),
                cpf: inputCpf.value.trim(),
                telefone: inputTelefone.value.trim(),
                nascimento: formatarData(inputNascimento.value),
                possuiCnh: inputCnh.checked
            };
        }

        // Funcao para gerar link WhatsApp
        function gerarLinkWhatsApp(mensagem) {
            const msg = encodeURIComponent(mensagem);
            return `https://wa.me/55${CONFIG.telefoneVendedor}?text=${msg}`;
        }

        // Funcao para gerar mensagem com dados do cliente
        function gerarMensagemMoto(moto) {
            const dados = getDadosCliente();
            let mensagem = `Ola! Tenho interesse na moto *${moto.nome}* - ${moto.preco}.\n\n`;

            if (dados.nome || dados.cpf || dados.telefone || dados.nascimento || dados.possuiCnh !== undefined) {
                mensagem += `*Meus dados:*\n`;
                if (dados.nome) mensagem += `Nome: ${dados.nome}\n`;
                if (dados.cpf) mensagem += `CPF: ${dados.cpf}\n`;
                if (dados.telefone) mensagem += `WhatsApp: ${dados.telefone}\n`;
                if (dados.nascimento) mensagem += `Data de Nascimento: ${dados.nascimento}\n`;
                mensagem += `Possui CNH: ${dados.possuiCnh ? 'Sim' : 'Nao'}\n`;
                mensagem += `\n`;
            }

            mensagem += `Pode me dar mais informacoes sobre financiamento?`;
            return mensagem;
        }

        // Funcao para gerar mensagem geral
        function gerarMensagemGeral() {
            const dados = getDadosCliente();
            let mensagem = `Ola! Vi o catalogo de motos Shineray e gostaria de mais informacoes.\n\n`;

            if (dados.nome || dados.cpf || dados.telefone || dados.nascimento || dados.possuiCnh !== undefined) {
                mensagem += `*Meus dados:*\n`;
                if (dados.nome) mensagem += `Nome: ${dados.nome}\n`;
                if (dados.cpf) mensagem += `CPF: ${dados.cpf}\n`;
                if (dados.telefone) mensagem += `WhatsApp: ${dados.telefone}\n`;
                if (dados.nascimento) mensagem += `Data de Nascimento: ${dados.nascimento}\n`;
                mensagem += `Possui CNH: ${dados.possuiCnh ? 'Sim' : 'Nao'}\n`;
            }

            return mensagem;
        }

        // Atualiza nome do vendedor
        document.getElementById('vendedorNome').textContent = CONFIG.nomeVendedor;

        // Links WhatsApp gerais (atualizados dinamicamente)
        function atualizarLinksGerais() {
            const link = gerarLinkWhatsApp(gerarMensagemGeral());
            document.getElementById('headerWhatsapp').href = link;
            document.getElementById('footerWhatsapp').href = link;
            document.getElementById('whatsappFloat').href = link;
        }

        // Atualiza links quando formulario muda
        inputNome.addEventListener('input', atualizarLinksGerais);
        inputCpf.addEventListener('input', atualizarLinksGerais);
        inputTelefone.addEventListener('input', atualizarLinksGerais);
        inputNascimento.addEventListener('change', atualizarLinksGerais);
        inputCnh.addEventListener('change', atualizarLinksGerais);
        atualizarLinksGerais();

        // Renderiza catalogo
        const grid = document.getElementById('motoGrid');
        MOTOS.forEach(moto => {
            const card = document.createElement('div');
            card.className = 'moto-card';
            card.innerHTML = `
                <img src="${moto.imagem}" alt="${moto.nome}" class="moto-image" loading="lazy">
                <div class="moto-info">
                    <h3 class="moto-name">${moto.nome}</h3>
                    <div class="moto-price">${moto.preco} <small>a vista</small></div>
                    <a href="#" class="btn-whatsapp" data-moto='${JSON.stringify(moto)}'>
                        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
                        </svg>
                        Tenho Interesse!
                    </a>
                </div>
            `;
            grid.appendChild(card);

            // Event listener para o botao
            const btn = card.querySelector('.btn-whatsapp');
            btn.addEventListener('click', function(e) {
                e.preventDefault();
                const motoData = JSON.parse(this.getAttribute('data-moto'));
                const mensagem = gerarMensagemMoto(motoData);
                const link = gerarLinkWhatsApp(mensagem);
                window.open(link, '_blank');
            });
        });
        
    </script>
</body>
</html>
