# Desenvolvendo um App de Garagem com FlutterFlow – Série Completa

Nesta série de vídeos, você acompanha passo a passo o desenvolvimento de um aplicativo mobile completo utilizando FlutterFlow, uma poderosa plataforma Low Code. Cada vídeo aborda uma etapa específica do projeto, desde a criação do banco de dados com Supabase até a implementação de funcionalidades como autenticação, menu lateral, cadastro, listagem de veículos e chat.

Entre no meu canal do Youtube: https://www.youtube.com/channel/UCi7gBAP6aJ4a9hklch_a1zw



## Código-fonte e funções utilizadas no projeto

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

## Sobre o autor:
Sou o Prof. Benevid Felix, docente da Universidade do Estado de Mato Grosso (UNEMAT), Campus de Sinop/MT. 
Leciono disciplinas de programação como C, Python, Automação com Inteligência Artificial e desenvolvimento com ferramentas Low Code. Possuo Mestrado pela PUCRS e Doutorado pela UFPR. 
Atuo na área de computação desde 2002 e sou entusiasta da cultura maker, com experiência em projetos de hardware utilizando ESP32, modelagem e impressão 3D, entre outros.

## Minhas redes sociais:
Instagram: https://instagram.com/benevid
GitHub: https://github.com/benevid
LinkedIn: https://linkedin.com/in/benevid
Facebook: https://facebook.com/benevid
X (Twitter): https://x.com/benevid
