# Prompt desenvolvido para o Lovable do jogo Alessa.
Criar um jogo de **caça-palavras temático e educativo** onde o jogador não procura apenas palavras aleatórias mas encontrar dentre 10 palavras que estão acentuadas corretamente.  No grid haverá além das letras aleatórias, 10 palavras escritas de forma incorreta e 10 palavras escritas de forma correta, e pode ser dispostas em horizontal, vertical e diagonal em ambos sentidos (da direita para esquerda ou contrário). 

A mecânica principal é:

> selecionar somente as palavras corretas dentro do grid.
> 

A lista de palavras segue no banco de dados a seguir contendo sua escrita correta, a incorreta e a explicação para a acentuação.

export const wordsDatabase = {
//Palavras oxítonas acentuadas
oxitonas: [
["vatapa", "Vatapá", "Oxítona terminada em A"],
["sofa", "sofá", "Oxítona terminada em A"],
["gamba", "gambá", "Oxítona terminada em A"],
["Para", "Pará", "Oxítona terminada em A"],
["cafe", "café", "Oxítona terminada em E"],
["voce", "você", "Oxítona terminada em E"],
["Tiete", "Tietê", "Oxítona terminada em E"],
["portugues", "português", "Oxítona terminada em E seguido de S"],
["avo", "avó", "Oxítona terminada em O"],
["jilo", "jiló", "Oxítona terminada em O"],
["cipo", "cipó", "Oxítona terminada em O"],
["carijo", "carijó", "Oxítona terminada em O"],
["chapeu", "chapéu", "Oxítona terminada em ditongo aberto ÉU"],
["trofeu", "troféu", "Oxítona terminada em ditongo aberto ÉU"],
["papeis", "papéis", "Oxítona terminada em ditongo aberto ÉI seguido de S"],
["fieis", "fiéis", "Oxítona terminada em ditongo aberto ÉI seguido de S"],
["heroi", "herói", "Oxítona terminada em ditongo aberto ÓI"],
["Niteroi", "Niterói", "Oxítona terminada em ditongo aberto ÓI"],
["anzois", "anzóis", "Oxítona terminada em ditongo aberto ÓI seguido de S"],
["destroi", "destrói", "Oxítona terminada em ditongo aberto ÓI"],
["parabens", "parabéns", "Oxítona terminada em ENS"],
["armazens", "armazéns", "Oxítona terminada em ENS"],
["alguem", "alguém", "Oxítona terminada em EM"],
["mantem", "mantém", "Oxítona terminada em EM"],
["porem", "porém", "Oxítona terminada em EM"],
["tambem", "também", "Oxítona terminada em EM"],
["acai", "açaí", "Oxítona acentuada pela regra do hiato"],
["Piaui", "Piauí", "Oxítona acentuada pela regra do hiato"],
["jacaranda", "jacarandá", "Oxítona terminada em A"],
["contrafile", "contrafilé", "Oxítona terminada em E"],
],

//Palavras paroxítonas acentuadas
paroxitonas: [
["facil", "fácil", "Paroxítona terminada em L"],
["hifen", "hífen", "Paroxítona terminada em N"],
["album", "álbum", "Paroxítona terminada em UM"],
["cadaver", "cadáver", "Paroxítona terminada em R"],
["albuns", "álbuns", "Paroxítona terminada em UNS"],
["torax", "tórax", "Paroxítona terminada em X"],
["juri", "júri", "Paroxítona terminada em I"],
["lapis", "lápis", "Paroxítona terminada em IS"],
["virus", "vírus", "Paroxítona terminada em US"],
["biceps", "bíceps", "Paroxítona terminada em PS"],
["orfao", "órfão", "Paroxítona terminada em ÃO"],
["ima", "ímã", "Paroxítona terminada em Ã"],
["proton", "próton", "Paroxítona terminada em ON"],
["amavel", "amável", "Paroxítona terminada em L"],
["carater", "caráter", "Paroxítona terminada em R"],
["individuos", "indivíduos", "Paroxítona terminada em ditongo"],
["precarias", "precárias", "Paroxítona terminada em ditongo seguido de S"],
["serie", "série", "Paroxítona terminada em ditongo"],
["historia", "história", "Paroxítona terminada em ditongo"],
["homogenea", "homogênea", "Paroxítona terminada em ditongo"],
["medio", "médio", "Paroxítona terminada em ditongo"],
["bromelia", "bromélia", "Paroxítona terminada em ditongo"],
["imoveis", "imóveis", "Paroxítona terminada em ditongo seguido de S"],
["agua", "água", "Paroxítona terminada em ditongo"],
["distancia", "distância", "Paroxítona terminada em ditongo"],
["industria", "indústria", "Paroxítona terminada em ditongo"],
["radio", "rádio", "Paroxítona terminada em ditongo"],
["cenario", "cenário", "Paroxítona terminada em ditongo"],
["saude", "saúde", "Paroxítona acentuada pela regra do hiato"],
["incluido", "incluído", "Paroxítona acentuada pela regra do hiato"],
],

//Palavras proparoxítonas acentuadas
proparoxitonas: [
["medico", "médico", "Proparoxítona (todas são acentuadas)"],
["lampada", "lâmpada", "Proparoxítona (todas são acentuadas)"],
["especifico", "específico", "Proparoxítona (todas são acentuadas)"],
["penultimo", "penúltimo", "Proparoxítona (todas são acentuadas)"],
["pagina", "página", "Proparoxítona (todas são acentuadas)"],
["antonimo", "antônimo", "Proparoxítona (todas são acentuadas)"],
["atomo", "átomo", "Proparoxítona (todas são acentuadas)"],
["relampago", "relâmpago", "Proparoxítona (todas são acentuadas)"],
["caotico", "caótico", "Proparoxítona (todas são acentuadas)"],
["unica", "única", "Proparoxítona (todas são acentuadas)"],
["politica", "política", "Proparoxítona (todas são acentuadas)"],
["atlantico", "atlântico", "Proparoxítona (todas são acentuadas)"],
["domestico", "doméstico", "Proparoxítona (todas são acentuadas)"],
["tecnicas", "técnicas", "Proparoxítona (todas são acentuadas)"],
["cerebro", "cérebro", "Proparoxítona (todas são acentuadas)"],
["ergometrica", "ergométrica", "Proparoxítona (todas são acentuadas)"],
["artifices", "artífices", "Proparoxítona (todas são acentuadas)"],
["ebano", "ébano", "Proparoxítona (todas são acentuadas)"],
["incredulo", "incrédulo", "Proparoxítona (todas são acentuadas)"],
["sonambulo", "sonâmbulo", "Proparoxítona (todas são acentuadas)"],
["valvula", "válvula", "Proparoxítona (todas são acentuadas)"],
["idolo", "ídolo", "Proparoxítona (todas são acentuadas)"],
["seculo", "século", "Proparoxítona (todas são acentuadas)"],
["exito", "êxito", "Proparoxítona (todas são acentuadas)"],
["codigos", "códigos", "Proparoxítona (todas são acentuadas)"],
["simbolos", "símbolos", "Proparoxítona (todas são acentuadas)"],
["decada", "década", "Proparoxítona (todas são acentuadas)"],
["esferografica", "esferográfica", "Proparoxítona (todas são acentuadas)"],
["interim", "ínterim", "Proparoxítona (todas são acentuadas)"],
["aerolito", "aerólito", "Proparoxítona (todas são acentuadas)"],
],

//Palavras hiatos i e u acentuados
hiatos: [
["acai", "açaí", "I tônico em hiato sozinho na sílaba"],
["baus", "baús", "U tônico em hiato seguido de S"],
["cai", "caí", "I tônico em hiato sozinho na sílaba"],
["faisca", "faísca", "I tônico em hiato seguido de S"],
["Paraiba", "Paraíba", "I tônico em hiato sozinho na sílaba"],
["egoista", "egoísta", "I tônico em hiato seguido de S"],
["ruido", "ruído", "I tônico em hiato sozinho na sílaba"],
["saude", "saúde", "U tônico em hiato sozinho na sílaba"],
["sauva", "saúva", "U tônico em hiato sozinho na sílaba"],
["balaustre", "balaústre", "U tônico em hiato seguido de S"],
["incluiram", "incluíram", "I tônico em hiato sozinho na sílaba"],
["paises", "países", "I tônico em hiato seguido de S"],
["prejuizo", "prejuízo", "I tônico em hiato sozinho na sílaba"],
["veiculo", "veículo", "I tônico em hiato sozinho na sílaba"],
["juizes", "juízes", "I tônico em hiato sozinho na sílaba"],
["Piaui", "Piauí", "I tônico em hiato após ditongo em oxítona"],
["tuiuiu", "tuiuiú", "U tônico em hiato após ditongo em oxítona"],
["teiu", "teiú", "U tônico em hiato após ditongo em oxítona"],
[
"tuiuius",
"tuiuiús",
"U tônico em hiato seguido de S após ditongo em oxítona",
],
["saida", "saída", "I tônico em hiato sozinho na sílaba"],
["ciume", "ciúme", "U tônico em hiato sozinho na sílaba"],
["atribuida", "atribuída", "I tônico em hiato sozinho na sílaba"],
["reune", "reúne", "U tônico em hiato sozinho na sílaba"],
["raizes", "raízes", "I tônico em hiato sozinho na sílaba"],
["pais", "país", "I tônico em hiato seguido de S"],
["incluido", "incluído", "I tônico em hiato sozinho na sílaba"],
["Icarai", "Icaraí", "I tônico em hiato sozinho na sílaba"],
["construisse", "construísse", "I tônico em hiato seguido de S"],
["genuina", "genuína", "I tônico em hiato sozinho na sílaba"],
["reunem", "reúnem", "U tônico em hiato sozinho na sílaba"],
],

//Exceções a regra de palavras acentuadas
excessoes: [
["raínha", "rainha", "Hiato seguido de NH"],
["baínha", "bainha", "Hiato seguido de NH"],
["moínho", "moinho", "Hiato seguido de NH"],
["Saára", "Saara", "Hiato de vogais repetidas"],
["Moóca", "Mooca", "Hiato de vogais repetidas"],
["xiíta", "xiita", "Hiato de vogais repetidas"],
["vadiíce", "vadiice", "Hiato de vogais repetidas"],
["semeêmos", "semeemos", "Hiato de vogais repetidas"],
["crêem", "creem", "Hiatos -eem não são mais acentuados"],
["lêem", "leem", "Hiatos -eem não são mais acentuados"],
["dêem", "deem", "Hiatos -eem não são mais acentuados"],
["vôo", "voo", "Hiatos -oo não são mais acentuados"],
["enjôo", "enjoo", "Hiatos -oo não são mais acentuados"],
["dôo", "doo", "Hiatos -oo não são mais acentuados"],
["zôo", "zoo", "Hiatos -oo não são mais acentuados"],
[
"feiúra",
"feiura",
"I ou U tônico após ditongo decrescente em paroxítona",
],
[
"baiúca",
"baiuca",
"I ou U tônico após ditongo decrescente em paroxítona",
],
[
"bocaiúva",
"bocaiuva",
"I ou U tônico após ditongo decrescente em paroxítona",
],
[
"sauípe",
"sauipe",
"I ou U tônico após ditongo decrescente em paroxítona",
],
["juíz", "juiz", "Forma sílaba com letra que não seja S (no caso, Z)"],
["raúl", "Raul", "Forma sílaba com letra que não seja S (no caso, L)"],
["ruím", "ruim", "Forma sílaba com letra que não seja S (no caso, M)"],
["caír", "cair", "Forma sílaba com letra que não seja S (no caso, R)"],
["saír", "sair", "Forma sílaba com letra que não seja S (no caso, R)"],
["aínda", "ainda", "Forma sílaba com letra que não seja S (no caso, N)"],
["saíndo", "saindo", "Forma sílaba com letra que não seja S (no caso, N)"],
["diúrno", "diurno", "Forma sílaba com letra que não seja S (no caso, N)"],
[
"amendoím",
"amendoim",
"Forma sílaba com letra que não seja S (no caso, M)",
],
["cauím", "cauim", "Forma sílaba com letra que não seja S (no caso, M)"],
["saíu", "saiu", "Forma sílaba com letra que não seja S (no caso, U)"],
],
};

Usar somente as palavras contidas neste banco de dados.

A cada palavra selecionada pelo mouse haverá uma reação do avatar do jogo que ficará no canto inferior do grid (sem cobrir o caça palavras). Caso o jogador acerte, haverá confetes, emissão de som em festejo e o avatar ficará feliz. caso o jogador erre, leve avermelhar nas bordas da tela com emissão de som de buzina leve e avatar fica com cara desapontada. No canto inferior da tela uma caixa de mensagem surge com a regra explicando a acentuação daquela palavra. 

Layout

não está engessado mas gostaria que fosse dark e vermelho. trouxe paleta de cores de sugestão. Para a página inicial, gostaria de um board simples como a imagem a seguir sugere. 

<img width="1914" height="997" alt="image" src="https://github.com/user-attachments/assets/55ab9c1b-476b-44ee-8f53-807f15eb9f1c" />


<img width="1911" height="926" alt="image" src="https://github.com/user-attachments/assets/44650ed2-2fa1-4380-aac4-d173c34d1af4" />


As imagens do avatar do jogo (a Alessinha) estão em seguida como sugestão:

<img width="413" height="415" alt="image" src="https://github.com/user-attachments/assets/be53387d-c388-486e-8cb5-2f3597d07ca5" />
<img width="416" height="398" alt="image" src="https://github.com/user-attachments/assets/3cfad0f7-b6d6-4e6d-a38a-4247bf620247" />
<img width="410" height="403" alt="image" src="https://github.com/user-attachments/assets/b5d5d658-e114-4003-8246-b31550c34b93" />
<img width="825" height="810" alt="image" src="https://github.com/user-attachments/assets/f4c3d0b5-e99e-4827-91c5-36f19f211b10" />
<img width="470" height="505" alt="image" src="https://github.com/user-attachments/assets/b3dd1090-3aa9-49f7-9224-134fe93e17fc" />
<img width="409" height="415" alt="image" src="https://github.com/user-attachments/assets/0f318eb7-e521-4cb5-8c4d-02bcd31f39fe" />


As imagens de avatar dos jogadores devem ser as imagens que virá em anexo podendo somente ser cortadas para melhor ajuste nas bordas ou cores de fundo

<img width="717" height="678" alt="image" src="https://github.com/user-attachments/assets/a38c1058-d8b1-454a-b675-8e81db809d61" />
<img width="759" height="774" alt="image" src="https://github.com/user-attachments/assets/25877873-8cf5-48b6-9403-3efaeeff335c" />
<img width="693" height="681" alt="image" src="https://github.com/user-attachments/assets/30504b33-bdf6-46fb-88fa-5a03ebc15948" />
<img width="492" height="477" alt="image" src="https://github.com/user-attachments/assets/e8467670-6e6b-422a-a735-eb73a2f47539" />
<img width="546" height="537" alt="image" src="https://github.com/user-attachments/assets/d7177663-cad6-4a04-bfcb-ec531433ea73" />
<img width="448" height="473" alt="image" src="https://github.com/user-attachments/assets/d6c8c115-9291-4cea-944d-1a7dbc1a982f" />
<img width="717" height="744" alt="image" src="https://github.com/user-attachments/assets/ff9bbba7-62a1-4d13-b131-646030e518ee" />
<img width="657" height="654" alt="image" src="https://github.com/user-attachments/assets/0ad2bcd9-8f16-4e8b-b520-4e4bd645c717" />
<img width="734" height="759" alt="image" src="https://github.com/user-attachments/assets/a5a58429-cb21-4581-9407-e887bc2ace90" />
<img width="716" height="753" alt="image" src="https://github.com/user-attachments/assets/eb655a81-53c3-428c-9565-a14c82456752" />
<img width="708" height="705" alt="image" src="https://github.com/user-attachments/assets/e688e874-2d2a-42c3-8566-ffd141838fd4" />


Paletas de cores

- -brick-ember: #bc0a0aff;
--evergreen: #172815ff;
--soft-blush: #f8e7e3ff;
--faded-copper: #8f754fff;
--black: #000000ff;

Na página Rank trago um esboço geral da disposição dos elementos como exemplo que virão dentro do grid assim como a tela inicial :

<img width="1250" height="775" alt="image" src="https://github.com/user-attachments/assets/cba6d336-162c-470e-bbdf-42d97c630bfa" />


No grid da página do jogo conterá o caça-palavras. uma caixa de chat box lateral que irá interagir com o jogador a medida que ele clicar nas palavras, dando frases de incentivo curtas se acertar e explicações ortográficas do banco de dados das palavras quando errar. 

abaixo irá o avatar da Alessinha que reagirá a cada acerto ou erro. 

<img width="1738" height="905" alt="image" src="https://github.com/user-attachments/assets/942c8094-049d-44af-9153-d9686c8db1ec" />


faça uma página para configurações onde o jogador pode editar nome, escolher novamente o avatar e mutar avisos sonoros e música.

Os dados do jogo devem ficar salvos na máquina e o ranking deve ser organizado em planilha no google sheets.
