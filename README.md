from fpdf import FPDF

# Create PDF class
class PDF(FPDF):
    def header(self):
        self.set_font('Arial', 'B', 12)
        self.cell(0, 10, 'Futebol 11: Uma Visão Geral', 0, 1, 'C')

    def chapter_title(self, title):
        self.set_font('Arial', 'B', 12)
        self.cell(0, 10, title, 0, 1, 'L')
        self.ln(4)

    def chapter_body(self, body):
        self.set_font('Arial', '', 12)
        self.multi_cell(0, 10, body)
        self.ln()

    def add_chapter(self, title, body):
        self.add_page()
        self.chapter_title(title)
        self.chapter_body(body)

# Create instance of PDF class
pdf = PDF()

# Add chapters
pdf.add_chapter('1. Introdução', """O futebol 11, também conhecido como futebol de campo, é um dos esportes mais populares do mundo. 
Este trabalho tem como objetivo explorar a história, as regras, as técnicas e táticas, além da importância física e treinamento no futebol 11. 
A popularidade global do futebol reflete sua capacidade de unir pessoas de diferentes culturas e nações, transcender barreiras linguísticas e promover valores como trabalho em equipe, disciplina e fair play.""")

pdf.add_chapter('2. Desenvolvimento', '')

pdf.add_chapter('2.1 História do Futebol 11', """O futebol moderno, como conhecemos hoje, teve suas origens na Inglaterra no século XIX. 
Antes da formalização das regras, várias formas de futebol eram jogadas em diferentes partes do mundo. 
Em 1863, a Football Association (FA) foi fundada em Londres, estabelecendo as primeiras regras padronizadas do jogo, 
que passaram a ser conhecidas como 'Regras de Cambridge'. Essas regras ajudaram a unificar os diversos estilos de jogo que existiam na época, 
promovendo uma estrutura mais organizada. 

Com o passar do tempo, o futebol se espalhou rapidamente pelo mundo, principalmente através das colônias britânicas e da migração. 
A Federação Internacional de Futebol (FIFA) foi fundada em 1904 para governar o esporte internacionalmente. 
O primeiro torneio mundial, a Copa do Mundo FIFA, foi realizado em 1930 no Uruguai. Desde então, o futebol cresceu exponencialmente, 
com ligas e competições em todos os continentes, atraindo bilhões de fãs e jogadores.""")

pdf.add_chapter('2.2 Regras Básicas', """O futebol 11 é jogado em um campo retangular com duas equipes de 11 jogadores cada. O objetivo é marcar gols na baliza adversária. 
O campo tem dimensões que variam entre 100-110 metros de comprimento e 64-75 metros de largura. As principais regras incluem:

- Duração do Jogo: O jogo é dividido em dois tempos de 45 minutos, com um intervalo de 15 minutos.
- Pontuação: Um gol é marcado quando a bola atravessa completamente a linha do gol entre os postes e sob a trave.
- Impedimento: Um jogador está em posição de impedimento se estiver mais próximo da linha do gol adversário do que a bola e o penúltimo defensor quando a bola é jogada para ele, exceto em seu próprio campo de defesa.
- Faltas e Infrações: Compreendem ações como empurrar, chutar ou bloquear o adversário de maneira imprópria. Faltas podem resultar em cobranças de faltas, pênaltis e advertências com cartões amarelo e vermelho.
- Cartões: O cartão amarelo é uma advertência, enquanto o cartão vermelho resulta na expulsão do jogador.""")

pdf.add_chapter('Dimensões Totais do Campo', """- Comprimento: Entre 90 e 120 metros (para jogos internacionais: 100-110 metros).
- Largura: Entre 45 e 90 metros (para jogos internacionais: 64-75 metros).""")

pdf.add_chapter('Área de Gol (Pequena Área)', """- Largura: 6 metros a partir de cada poste de gol.
- Profundidade: 5,5 metros.""")

pdf.add_chapter('Área de Pênalti (Grande Área)', """- Largura: 16,5 metros a partir de cada poste de gol.
- Profundidade: 16,5 metros.
- Marca de pênalti: 11 metros do centro do gol.""")

pdf.add_chapter('Círculo Central', """- Raio: 9,15 metros.""")

pdf.add_chapter('Arcos de Escanteio', """- Raio: 1 metro em cada canto do campo.""")

pdf.add_chapter('2.3 Técnicas e Táticas', '')

pdf.add_chapter('Técnicas Básicas', """- Drible: O drible envolve o controle da bola enquanto se move em torno de adversários, essencial para avançar no campo e criar oportunidades de gol.
- Passe: Passar a bola é crucial para manter a posse e envolver todos os jogadores. Passes podem ser curtos ou longos, dependendo da estratégia.
- Chute: O chute é a técnica de impulsionar a bola em direção ao gol, podendo ser realizado com diferentes partes do pé para variar a força e a precisão.
- Cabeceio: Utilizado para jogar a bola com a cabeça, geralmente em situações de cruzamentos e bolas altas.""")

pdf.add_chapter('Táticas de Jogo', """- 4-4-2: Uma das formações mais comuns, com quatro defensores, quatro meio-campistas e dois atacantes. Oferece equilíbrio entre defesa e ataque.
- 4-3-3: Focado no ataque, com quatro defensores, três meio-campistas e três atacantes. Utilizado por equipes que preferem pressionar o adversário.
- 3-5-2: Formação que utiliza três defensores, cinco meio-campistas e dois atacantes, permitindo maior controle do meio-campo.

Cada formação tem suas próprias estratégias de ataque e defesa, ajustadas conforme o adversário e as circunstâncias do jogo.""")

pdf.add_chapter('2.4 Importância Física e Treinamento', '')

pdf.add_chapter('Condicionamento Físico', """O condicionamento físico é essencial no futebol 11. Jogadores precisam de resistência para correr durante os 90 minutos, força para disputar a bola e velocidade para superar os adversários. Flexibilidade e agilidade também são importantes para prevenir lesões e realizar movimentos rápidos e precisos.""")

pdf.add_chapter('Prevenção de Lesões', """Lesões são comuns no futebol devido ao contato físico e à intensidade do jogo. Medidas de prevenção incluem:

- Aquecimento: Sessões de aquecimento antes dos jogos e treinos para preparar os músculos.
- Alongamento: Alongamentos antes e depois das atividades para manter a flexibilidade muscular.
- Equipamentos Adequados: Uso de caneleiras, chuteiras adequadas e, em alguns casos, protetores bucais.""")

pdf.add_chapter('Programas de Treinamento', """Os programas de treinamento são desenvolvidos para melhorar habilidades específicas e condicionamento físico geral. Eles incluem:

- Treinamento Aeróbico: Corridas de longa distância e exercícios de resistência para melhorar a capacidade cardiovascular.
- Treinamento de Força: Exercícios de musculação para aumentar a força muscular.
- Treinamento de Habilidades: Sessões práticas focadas em dribles, passes, chutes e cabeceios.
- Treinamento Tático: Simulações de jogo e exercícios para desenvolver estratégias de equipe.""")

pdf.add_chapter('2.5 Características do Futebol 11', """- Esporte de Equipe: O futebol 11 envolve 11 jogadores por equipe, com posições específicas como goleiro, defensores, meio-campistas e atacantes, cada um desempenhando um papel crucial.
- Campo Grande: O campo de jogo é significativamente maior do que em outras variantes de futebol, permitindo mais espaço para estratégias e táticas complexas.
- Intensidade e Resistência: Devido à duração e ao tamanho do campo, o futebol 11 exige alto nível de condicionamento físico e resistência dos jogadores.
- Táticas e Formações Variadas: Equipas utilizam diversas formações e táticas para se adaptar aos adversários e maximizar seu desempenho.
- Regulamentação Estrita: O jogo é regido por um conjunto abrangente de regras que garantem a fair play e a segurança dos jogadores.""")

pdf.add_chapter('3. Conclusão', """O futebol 11 é um esporte que combina habilidades técnicas, táticas e físicas. Além de ser uma paixão global, promove a saúde, o trabalho em equipe e a inclusão social. Com uma rica história e regras bem estabelecidas, continua a ser uma das atividades esportivas mais influentes e praticadas no mundo.""")

pdf.add_chapter('4. Bibliografia', """- Andrade, José Carlos. História do Futebol: Das Origens aos Dias Atuais. São Paulo: Editora Esportiva, 2015.
- Silva, Ricardo. Manual do Futebol: Técnicas e Táticas. Rio de Janeiro: Editora Desportiva, 2018.
- Souza, Maria Fernanda. Fisiologia e Treinamento no Futebol. Porto Alegre: Editora Saúde, 2020.
- Associação Brasileira de Futebol. Regras do Jogo. Disponível em: https://www.abfutebol.com.br/regras.""")

 Me dea só o conteúdo não  PDF copie  pra me o conteúdo 
