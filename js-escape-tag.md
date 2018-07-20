# JavaScriptで特殊文字を HTML エンティティに変換する方法

|特殊文字|エンティティ|
|---|---|
|&amp; |&amp;amp; |
|&lt; |&amp;lt; |
|&gt; |&amp;gt; |
|&quot; |&amp;quot; |
|&#39; |&amp;#39; |

```
function escape_tag(val)
{
  return val.replace(/\&/g, '&amp;')
    .replace( /</g, '&lt;')
    .replace(/>/g, '&gt;')
    .replace(/\"/g, '&quot;')
    .replace(/\'/g, '&#39;');
}
```
