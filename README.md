# impacto-resultado
<script>
    function enviarWhatsApp() {
        // Captura os valores dos campos do formulário
        const nome = document.getElementById("nome").value;
        const dataNascimento = document.getElementById("data_nascimento").value;
        const idade = document.getElementById("idade").value;
        const email = document.getElementById("email").value;
        const telefone = document.getElementById("telefone").value;
        const altura = document.getElementById("altura").value;
        const peso = document.getElementById("peso").value;
        const objetivo = document.getElementById("objetivo").value;
        
        // Coletar os valores de rádio (sim/não)
        const atividadeFisica = document.querySelector('input[name="atividade_fisica"]:checked') ? document.querySelector('input[name="atividade_fisica"]:checked').value : "Não informado";
        const tipoAtividade = document.getElementById("tipo_atividade").value;
        const tempoParado = document.getElementById("tempo_parado").value;
        const frequencia = document.getElementById("frequencia").value;

        const problemasSaude = [...document.querySelectorAll('input[name="problemas_saude"]:checked')].map(e => e.value).join(", ") || "Nenhum";

        const medicamentos = document.querySelector('input[name="medicamentos"]:checked') ? document.querySelector('input[name="medicamentos"]:checked').value : "Não informado";
        const medicamentosNome = document.getElementById("medicamentos_nome").value;

        const lesao = document.querySelector('input[name="lesao"]:checked') ? document.querySelector('input[name="lesao"]:checked').value : "Não informado";
        const lesaoLocal = document.getElementById("lesao_local").value;

        const cirurgia = document.querySelector('input[name="cirurgia"]:checked') ? document.querySelector('input[name="cirurgia"]:checked').value : "Não informado";
        const cirurgiaNome = document.getElementById("cirurgia_nome").value;

        const refeicoes = document.getElementById("refeicoes").value;
        const agua = document.getElementById("agua").value;
        
        const alcool = document.querySelector('input[name="alcool"]:checked') ? document.querySelector('input[name="alcool"]:checked').value : "Não informado";
        const fuma = document.querySelector('input[name="fuma"]:checked') ? document.querySelector('input[name="fuma"]:checked').value : "Não informado";

        const restricoes = document.querySelector('input[name="restricoes"]:checked') ? document.querySelector('input[name="restricoes"]:checked').value : "Não informado";
        const restricoesNome = document.getElementById("restricoes_nome").value;

        const rotina = document.querySelector('input[name="rotina"]:checked') ? document.querySelector('input[name="rotina"]:checked').value : "Não informado";
        const sono = document.getElementById("sono").value;

        const estresse = document.querySelector('input[name="estresse"]:checked') ? document.querySelector('input[name="estresse"]:checked').value : "Não informado";

        const diasTreino = [...document.querySelectorAll('input[name="dias_treino"]:checked')].map(e => e.value).join(", ") || "Nenhum selecionado";
        const horariosTreino = document.querySelector('input[name="horarios_treino"]:checked') ? document.querySelector('input[name="horarios_treino"]:checked').value : "Não informado";
        const tempoTreino = document.getElementById("tempo_treino").value;

        // Criar a mensagem formatada
        const mensagem = `*Ficha de Anamnese - Impacto Resultados*%0A%0A`
            + `*Nome:* ${nome}%0A`
            + `*Data de Nascimento:* ${dataNascimento}%0A`
            + `*Idade:* ${idade}%0A`
            + `*E-mail:* ${email}%0A`
            + `*Telefone:* ${telefone}%0A`
            + `*Altura:* ${altura} cm%0A`
            + `*Peso:* ${peso} kg%0A%0A`
            + `*Objetivo:* ${objetivo}%0A%0A`
            + `*Prática de atividade física:* ${atividadeFisica}%0A`
            + `*Tipo de atividade:* ${tipoAtividade || "Não informado"}%0A`
            + `*Tempo parado:* ${tempoParado || "Não informado"}%0A`
            + `*Frequência semanal desejada:* ${frequencia || "Não informado"} vezes por semana%0A%0A`
            + `*Problemas de saúde:* ${problemasSaude}%0A`
            + `*Uso de medicamentos:* ${medicamentos}%0A`
            + `*Quais medicamentos:* ${medicamentosNome || "Nenhum"}%0A`
            + `*Possui lesão:* ${lesao}%0A`
            + `*Local da lesão:* ${lesaoLocal || "Nenhum"}%0A`
            + `*Já fez cirurgia:* ${cirurgia}%0A`
            + `*Detalhes da cirurgia:* ${cirurgiaNome || "Nenhuma"}%0A%0A`
            + `*Refeições diárias:* ${refeicoes} refeições%0A`
            + `*Consumo de água:* ${agua} litros/dia%0A`
            + `*Consome álcool:* ${alcool}%0A`
            + `*Fuma:* ${fuma}%0A`
            + `*Restrições alimentares:* ${restricoes}%0A`
            + `*Quais restrições:* ${restricoesNome || "Nenhuma"}%0A%0A`
            + `*Rotina de trabalho:* ${rotina}%0A`
            + `*Horas de sono:* ${sono} horas/noite%0A`
            + `*Nível de estresse:* ${estresse}%0A%0A`
            + `*Dias disponíveis para treino:* ${diasTreino}%0A`
            + `*Melhor horário para treino:* ${horariosTreino}%0A`
            + `*Tempo disponível por dia para treino:* ${tempoTreino}%0A`;

        // Criar o link do WhatsApp
        const url = `https://wa.me/5548988359457?text=${mensagem}`;

        // Abrir o WhatsApp
        window.open(url, '_blank');
    }
</script>
