# TP1 - [Título do Trabalho Prático]

## Autor
- **Nome:** Wu Hou Pan
- **ID:** a109381
- **Foto:** <img width="244" height="326" alt="WhatsApp Image 2026-10-08 at 14 40 42" src="https://github.com/user-attachments/assets/54e22a80-2a33-457c-af98-10e520e46395" /> 




Token	Regex	Nota
comentário	\#.*	ignorado
VAR	\?\w+	?nome, ?s
LANG	@[A-Za-z]{2}	@en
STRING	"[^"]*"	as aspas são removidas do valor
NUM	\d+	convertido para int
CONCEPT	[A-Za-z_]\w*(:\w+)?	dbo:MusicalArtist, foaf:name, a
LBRACE, RBRACE, DOT	{ } .	delimitadores
LIMIT	—	palavra reservada
