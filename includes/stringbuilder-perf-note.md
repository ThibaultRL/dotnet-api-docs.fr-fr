L’indexation de base de caractères avec le <xref:System.Text.StringBuilder.Chars%2A> propriété peut être très lente dans les conditions suivantes :

- Le <xref:System.Text.StringBuilder> instance est importante (par exemple, il se compose de plusieurs dizaines de milliers de caractères).
- Le <xref:System.Text.StringBuilder> est « volumineuses ». Autrement dit, des appels répétés à des méthodes telles que <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> ont développé automatiquement l’objet <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> propriété et des blocs de nouveau alloués de la mémoire à celle-ci.

Performances sont gravement affectés, car chaque accès caractère parcourt la liste de liés ensemble de segments pour rechercher l’index dans la mémoire tampon correcte.

> [!NOTE]
>  Même pour un grand « volumineuses » <xref:System.Text.StringBuilder> de l’objet, à l’aide de la <xref:System.Text.StringBuilder.Chars%2A> propriété pour l’accès à un ou un petit nombre de caractères basé sur les index a un impact sur les performances négligeable ; en général, c’est une **0(n)** opération. L’impact sur les performances se produit lors de l’itération des caractères contenus dans le <xref:System.Text.StringBuilder> objet, qui est un **O(n^2)** opération. 

Si vous rencontrez des problèmes de performances lors de l’indexation de base de caractères avec <xref:System.Text.StringBuilder> des objets, vous pouvez utiliser une des solutions suivantes :

- Convertir le <xref:System.Text.StringBuilder> à l’instance un <xref:System.String> en appelant le <xref:System.Text.StringBuilder.ToString%2A> (méthode), puis accéder aux caractères dans la chaîne.

- Copiez le contenu existants <xref:System.Text.StringBuilder> une taille de l’objet vers un nouveau <xref:System.Text.StringBuilder> objet. Améliorent les performances, car le nouveau <xref:System.Text.StringBuilder> objet n’est pas volumineuse. Exemple :

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- Définir la capacité initiale de la <xref:System.Text.StringBuilder> objet à une valeur qui est égale à sa valeur maximale attendue en appelant le <xref:System.Text.StringBuilder.%23ctor(System.Int32)> constructeur. Notez que cette opération alloue l’intégralité du bloc de systèmes de mémoire même le <xref:System.Text.StringBuilder> rarement atteint sa capacité maximale.
