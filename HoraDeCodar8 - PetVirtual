class VirtualPet(val nome: String) {
    var nivelDeFome = 50
    var nivelFelicidade = 60
    var nivelDeCansaço = 30
    var idadePet = 1
    var sujeira = 0
    var vontadeBanheiro = 0

    // Funções para cuidar do pet

    fun alimentar() {
        vontadeBanheiro += 10
        nivelDeFome -= 20
        nivelFelicidade += 30
        if (nivelDeFome < 0) nivelDeFome = 0
        println("$nome foi alimentado. O nível de fome diminuiu.")
    }

    fun brincar() {
        sujeira += 20
        nivelFelicidade += 40
        println("$nome está brincando e se sentindo mais feliz.")
    }

    fun verificarStatus() {
        println("Status atual de $nome:")
        println("Nível de fome 🍽️: $nivelDeFome")
        println("Nível de felicidade 💗: $nivelFelicidade")
        println("Nível de cansaço 😴: $nivelDeCansaço")
        println("Nível do pet 🎈: $idadePet")
    }

    fun passarTempo() {
        // Simula a passagem do tempo
        nivelDeFome += 10
        nivelFelicidade -= 30
        nivelDeCansaço += 10
        println("fique atento com o passar do tempo!🕰️")

        // O pet só envelhece se estiver feliz
        if (nivelFelicidade >= 60) {
            idadePet++
            println("$nome cresceu! Agora está com $idadePet anos 🎉 !")
        }

        // Checagem de morte
        if (nivelDeFome >= 100 || nivelDeCansaço >= 100 || nivelFelicidade <= 0) {
            obito()
        }

        if (idadePet == 50) {
            println("Seu pet chegou aos 50 anos! Parabéns, você foi um(a) ótimo(a) pai/mãe de pet. 😎")
        }
    }

    fun descanso() {
        nivelDeCansaço -= 15
        nivelFelicidade += 30
        if (nivelDeCansaço < 0) nivelDeCansaço = 0
        println("$nome tirou uma soneca, agora se sente mais disposto! 🛏️ ")
    }

    fun obito() {
        println("$nome morreu por fome, cansaço extremo ou tristeza profunda. Que feio.")
        kotlin.system.exitProcess(0)
    }
}


fun main() {
    println("Bem-vindo ao Simulador de Animal de Estimação Virtual! 🐾")
    println("Digite o nome do seu animal de estimação:")
    val nomePet = readLine() ?: "Baltazar Guilherme Tenório"
    val pet = VirtualPet(nomePet)

    while (true) {
        println("\\nEscolha uma ação:")
        println("1. Alimentar $nomePet")
        println("2. Brincar com $nomePet")
        println("3. Verificar o status de $nomePet")
        println("4. Deixar $nomePet descansar")
        println("5. Sair")

        val escolha = readLine()?.toIntOrNull() ?: continue

        when (escolha) {
            1 -> pet.alimentar()
            2 -> pet.brincar()
            3 -> pet.verificarStatus()
            4 -> pet.descanso()
            5 -> {
                println("Saindo do Simulador de Animal de Estimação Virtual. Adeus!")
                return
            }
            else -> println("Escolha inválida. Tente novamente.")
        }

        pet.passarTempo()
    }
}
