classDiagram
    class Membro {
        -String nome
        -String email
        -String cpf
        -String telefone
        +assinarPlano(Plano plano)
        +fazerReserva(Sala sala, Data data)
        +realizarCheckin()
    }

    class Plano {
        -String nome
        -float valorMensal
        -int horasCredito
        +atualizarValor(float novoValor)
        +consultarBeneficios()
        +verificarHoras(Membro membro)
    }

    class Sala {
        -int numero
        -int capacidadeMax
        -float precoHora
        +verificarDisponibilidade(Data data, Hora inicio, Hora fim)
        +adicionarRecurso(Recurso recurso)
        +calcularPrecoAdicional(int horasExtras)
    }

    class Recurso {
        -String nome
        -String codigoPatrimonio
        -String statusConservacao
        +atualizarStatus()
        +registrarManutencao()
        +obterDetalhes()
    }

    class Reserva {
        -Date data
        -Time horaInicio
        -Time horaTermino
        -String status
        +confirmarReserva()
        +cancelarReserva()
        +concluirReserva()
    }

    class CheckIn {
        -DateTime dataHoraEntrada
        -DateTime dataHoraSaida
        -String localAcesso
        +registrarEntrada()
        +registrarSaida()
        +calcularTempoPermanencia()
    }

    Plano "0..1" -- "0..*" Membro : possui <
    Membro "1" -- "0..*" Reserva : realiza >
    Membro "1" -- "0..*" CheckIn : registra >
    Sala "1" -- "0..*" Reserva : alocada em <
    Sala "1" *-- "0..*" Recurso : contém >