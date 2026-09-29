# assets/galeria/

Pasta reservada para as fotos do aulão de Ciências da Natureza (Juscimeira-MT, Projeto Pré-ENEM Digit@l MT).

## Como publicar as fotos após o evento

1. Salve as fotos aqui, nesta pasta (`assets/galeria/`), em formato `.jpg` ou `.png`. Recomendado: até ~1600px de largura, para carregar rápido.
2. Abra `index.html` e localize o bloco `GALERIA_FOTOS` (busque por "GALERIA DE FOTOS" no arquivo, perto do fim do `<script>`).
3. Para cada foto, adicione uma linha assim, com um texto alternativo descrevendo a cena (importante para acessibilidade):

   ```js
   const GALERIA_FOTOS=[
     {src:'assets/galeria/foto1.jpg', alt:'Estudantes participando do aulão em Juscimeira-MT'},
     {src:'assets/galeria/foto2.jpg', alt:'Professora Pâmella apresentando o dashboard do Raio-X'},
   ];
   ```

4. Salve e publique. O carrossel na aba "Galeria de fotos" é montado automaticamente a partir dessa lista — nenhuma outra alteração de código é necessária.

Enquanto a lista estiver vazia, a aba mostra automaticamente um aviso de "galeria em construção".
