# TP1 - [Título do Trabalho Prático]

## Autor
- **Nome:** Wu Hou Pan
- **ID:** a109381
- **Foto:** <img width="244" height="326" alt="WhatsApp Image 2026-10-08 at 14 40 42" src="https://github.com/user-attachments/assets/54e22a80-2a33-457c-af98-10e520e46395" /> 




Resumo
Construir um analisador léxico em Python para uma linguagem de query semelhante ao SPARQL. O programa lê texto do stdin e produz a lista de tokens reconhecidos, sem interpretar o seu significado.

Tokens reconhecidos

Token	Descrição	Exemplo
COMENT	# até ao fim da linha (ignorado)	# comentário
VAR	? seguido de alfanuméricos	?nome
LANG	@ seguido de 2 letras	@en
STRING	qualquer sequência entre aspas	"Chuck Berry"
PR	palavras reservadas	select, where, LIMIT
DELIM	delimitadores	{, }, .
NUM	sequência de dígitos	1000
CONC	conceito: alfanuméricos com : opcional	dbo:MusicalArtist, a
ERRO	qualquer outro carater que não seja espaço	%
Lista de Resultados
analexico.py - Script principal em Python com a implementação do analisador léxico.
exemplo.txt - Ficheiro de teste.
res.txt - Ficheiro gerado com o resultado
