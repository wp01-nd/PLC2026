# TP1 - [Título do Trabalho Prático]

## Autor
- **Nome:** Wu Hou Pan
- **ID:** a109381
- **Foto:** <img width="244" height="326" alt="WhatsApp Image 2026-10-08 at 14 40 42" src="https://github.com/user-attachments/assets/54e22a80-2a33-457c-af98-10e520e46395" />

import re

def md_para_html(texto):
    saida = []
    lista = None  

    for linha in texto.split('\n'):
        
        if re.match(r'^\s*\d+\.\s+', linha):
            tipo = 'ol'
            item = re.sub(r'^\s*\d+\.\s+', '', linha)
        
        
        elif re.match(r'^\s*[-*+]\s+', linha):
            tipo = 'ul'
            item = re.sub(r'^\s*[-*+]\s+', '', linha) # Substitui o fatiamento rígido [2:]
        else:
            tipo = None

        
        if tipo != lista:
            if lista:
                saida.append(f'</{lista}>')
            if tipo:
                saida.append(f'<{tipo}>')
            lista = tipo

        if tipo:
            saida.append(f'  <li>{item}</li>') # Adicionei 2 espaços para identar o HTML :)
        else:
            saida.append(linha)

  
    if lista:
        saida.append(f'</{lista}>')

    return '\n'.join(saida)


if __name__ == '__main__':
    exemplo = """Frutas:
- Maçã
* Banana
+ Laranja

Passos:
1. Lavar
2. Cortar
3. Comer"""
    
    print(md_para_html(exemplo))
