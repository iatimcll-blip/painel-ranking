<script>
const ADMIN_PASSWORD = "123456"; // Troque por uma senha forte

function solicitarSenha() {
    const senha = prompt("Digite a senha de administrador:");
    if (senha === ADMIN_PASSWORD) {
        sessionStorage.setItem("admin", "true");
        alert("Modo administrador ativado.");
        document.getElementById("adminArea").style.display = "block";
    } else {
        alert("Senha incorreta.");
    }
}

function verificarAdmin() {
    if (sessionStorage.getItem("admin") === "true") {
        document.getElementById("adminArea").style.display = "block";
    }
}

window.onload = verificarAdmin;
</script>
