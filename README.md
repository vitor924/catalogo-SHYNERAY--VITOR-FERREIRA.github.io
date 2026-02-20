<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Catálogo Oficial Shineray</title>
<meta name="description" content="Catálogo completo de motos Shineray com financiamento facilitado. Fale direto no WhatsApp!">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

<style>
:root{
    --primary:#8B0000;
    --secondary:#DC143C;
    --accent:#25D366;
    --light:#f5f5f5;
}

*{margin:0;padding:0;box-sizing:border-box}
body{
    font-family:'Poppins',sans-serif;
    background:var(--light);
    color:#333;
    line-height:1.6;
}

/* HEADER */
header{
    background:linear-gradient(135deg,var(--primary),var(--secondary));
    color:#fff;
    padding:15px 20px;
    position:fixed;
    width:100%;
    z-index:1000;
}
.header-content{
    max-width:1200px;
    margin:auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
}
.logo{font-weight:700;font-size:1.5rem}

.cta{
    background:var(--accent);
    color:#fff;
    padding:10px 20px;
    border-radius:25px;
    text-decoration:none;
    font-weight:600;
}

/* HERO */
.hero{
    padding:120px 20px 60px;
    text-align:center;
    background:linear-gradient(135deg,var(--primary),var(--secondary));
    color:#fff;
}
.hero h1{font-size:2.2rem;margin-bottom:15px}
.badge{
    background:#FFD700;
    color:var(--primary);
    padding:10px 25px;
    border-radius:25px;
    font-weight:700;
    display:inline-block;
    margin-top:15px;
}

/* FORM */
.form-section{
    background:#fff;
    padding:30px 20px;
}
.form-container{
    max-width:800px;
    margin:auto;
}
.form-grid{
    display:grid;
    gap:15px;
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
}
input{
    padding:12px;
    border:2px solid #ddd;
    border-radius:8px;
}
input:focus{
    outline:none;
    border-color:var(--secondary);
}

/* CATALOGO */
.catalog{
    max-width:1200px;
    margin:auto;
    padding:40px 20px;
}
.grid{
    display:grid;
    gap:25px;
    grid-template-columns:repeat(auto-fill,minmax(280px,1fr));
}
.card{
    background:#fff;
    border-radius:15px;
    overflow:hidden;
    box-shadow:0 5px 20px rgba(0,0,0,0.1);
}
.card img{
    width:100%;
    height:180px;
    object-fit:contain;
    background:#fafafa;
}
.card-content{padding:20px}
.price{
    color:var(--secondary);
    font-size:1.3rem;
    font-weight:700;
    margin:10px 0;
}
.btn{
    display:block;
    text-align:center;
    padding:12px;
    background:var(--accent);
    color:#fff;
    border-radius:8px;
    text-decoration:none;
    font-weight:600;
}

/* FOOTER */
footer{
    background:var(--primary);
    color:#fff;
    text-align:center;
    padding:40px 20px;
    margin-top:40px;
}

@media(max-width:600px){
    .hero h1{font-size:1.6rem}
}
</style>
</head>
<body>

<header>
<div class="header-content">
<div class="logo">SHINERAY Motos</div>
<a href="#" id="whatsHeader" class="cta">Fale no WhatsApp</a>
</div>
</header>

<section class="hero">
<h1>Realize o Sonho da Sua Moto</h1>
<p>Financiamento facilitado com entrada promocional.</p>
<div class="badge">Entrada a partir de R$ 10,00*</div>
<p style="margin-top:8px;font-size:0.8rem;opacity:0.8">
*Sujeito à análise de crédito
</p>
</section>

<section class="form-section">
<div class="form-container">
<h3>Preencha seus dados</h3>
<div class="form-grid">
<input type="text" id="nome" placeholder="Nome completo">
<input type="text" id="cpf" placeholder="CPF">
<input type="text" id="telefone" placeholder="WhatsApp">
<input type="date" id="nascimento">
<label><input type="checkbox" id="cnh"> Possui CNH</label>
</div>
<p style="font-size:0.75rem;margin-top:10px;color:#666">
Seus dados são enviados diretamente ao consultor via WhatsApp.
</p>
</div>
</section>

<section class="catalog">
<h2 style="text-align:center;margin-bottom:30px">Nosso Catálogo</h2>
<div class="grid" id="grid"></div>
</section>

<footer>
<p>Shineray - Qualidade e Economia</p>
</footer>

<script>
// ================= CONFIG =================
const CONFIG = {
    vendedor:"Vitor Ferreira",
    telefone:"556199597429"
};

// ================= MOTOS =================
const MOTOS = [
{nome:"JET 50 SS",preco:11990,imagem:"https://www.shineray.com.br/wp-content/uploads/2023/06/Jet-50s.webp"},
{nome:"JET 125SS",preco:12990,imagem:"https://www.shineray.com.br/wp-content/uploads/2023/06/JET-125ss.webp"},
{nome:"RIO 125 EFI",preco:12990,imagem:"https://www.shineray.com.br/wp-content/uploads/2023/12/RIO-125-EFI.webp"},
{nome:"JEF 150s",preco:15990,imagem:"https://www.shineray.com.br/wp-content/uploads/2023/08/JEF-150s.webp"},
{nome:"URBAN 150 EFI",preco:21990,imagem:"https://www.shineray.com.br/wp-content/uploads/2025/01/URBAN-150-EFI.webp"},
{nome:"SHI 175",preco:16990,imagem:"https://www.shineray.com.br/wp-content/uploads/2023/06/SHI-175-1.webp"},
{nome:"STORM 200 EFI",preco:23990,imagem:"https://www.shineray.com.br/wp-content/uploads/2024/08/Storm.webp"},
{nome:"250F",preco:21990,imagem:"https://www.shineray.com.br/wp-content/uploads/2024/12/250F.webp"},
{nome:"Denver",preco:27990,imagem:"https://www.shineray.com.br/wp-content/uploads/2024/12/Denver.webp"},
{nome:"Titanium 250",preco:27990,imagem:"https://www.shineray.com.br/wp-content/uploads/2024/12/Titanium-1.webp"},
{nome:"Iron 250",preco:26990,imagem:"https://www.shineray.com.br/wp-content/uploads/2025/01/Iron.webp"}
];

// ================= FUNÇÕES =================
function moeda(valor){
    return valor.toLocaleString("pt-BR",{style:"currency",currency:"BRL"});
}

function getDados(){
    return {
        nome:document.getElementById("nome").value.trim(),
        cpf:document.getElementById("cpf").value.trim(),
        telefone:document.getElementById("telefone").value.trim(),
        nascimento:document.getElementById("nascimento").value,
        cnh:document.getElementById("cnh").checked
    };
}

function gerarMensagem(moto){
    const d = getDados();
    let msg = `Olá! Tenho interesse na ${moto.nome} - ${moeda(moto.preco)}.\n\n`;
    if(d.nome||d.cpf||d.telefone||d.nascimento){
        msg += "Meus dados:\n";
        if(d.nome) msg += `Nome: ${d.nome}\n`;
        if(d.cpf) msg += `CPF: ${d.cpf}\n`;
        if(d.telefone) msg += `WhatsApp: ${d.telefone}\n`;
        if(d.nascimento) msg += `Nascimento: ${d.nascimento}\n`;
        if(d.cnh) msg += "Possui CNH: Sim\n";
        msg += "\n";
    }
    msg += "Quero saber como funciona a entrada de R$ 10,00 e as parcelas.";
    return encodeURIComponent(msg);
}

function linkWhats(msg){
    return `https://wa.me/${CONFIG.telefone}?text=${msg}`;
}

// ================= RENDER =================
const grid = document.getElementById("grid");

MOTOS.forEach(m=>{
    const card = document.createElement("div");
    card.className="card";
    card.innerHTML=`
        <img src="${m.imagem}" alt="${m.nome}">
        <div class="card-content">
            <h3>${m.nome}</h3>
            <div class="price">${moeda(m.preco)}</div>
            <a href="#" class="btn">Quero Garantir Essa Oferta</a>
        </div>
    `;
    const btn = card.querySelector(".btn");
    btn.addEventListener("click",(e)=>{
        e.preventDefault();
        window.open(linkWhats(gerarMensagem(m)),"_blank");
    });
    grid.appendChild(card);
});

// Header WhatsApp
document.getElementById("whatsHeader")
.href = linkWhats(encodeURIComponent("Olá! Gostaria de mais informações sobre as motos."));
</script>

</body>
</html>
