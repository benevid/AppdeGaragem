# AppdeGaragem
Projeto App de Garagem - Flutterflow


**View Conversas**
```sql
create view public.conversas as
select
  c.id as conversa_id,
  c."userId" as conversa_userId,
  c."anuncioId" as conversa_anuncioId,
  a.titulo as anuncio_titulo,
  a."userId" as anuncio_userId,
  p.nome as profile_nome
from
  conversa c
  join anuncio a on c."anuncioId" = a.id
  join profile p on a."userId" = p."userId";
```

**Custom Function**

```dart
 /// MODIFY CODE ONLY BELOW THIS LINE
  // recebe uma data em string e converte para datetime
  try {
    // Se a string tem apenas 4 dígitos (ano), adiciona "-01-01"
    if (RegExp(r'^\d{4}$').hasMatch(dateString)) {
      dateString = '$dateString-01-01';
    }
    return DateTime.parse(dateString);
  } catch (e) {
    return null; // Return null if parsing fails
  }

  /// MODIFY CODE ONLY ABOVE THIS LINE
```
