```php
use App\Models\Users\User;
use App\Models\Database;

$db = new Database($_SERVER['DOCUMENT_ROOT'] . DIRECTORY_SEPARATOR . 'settings.json');
$maoDeMatos = $db->getUser('De Matos', 'Mao');

echo '<h2>';
echo ucfirst($maoDeMatos->getName());         // Print user name in h2 tag
echo '</h2>' . PHP_EOL;

echo PHP_EOL . '<code class="php_code">';
print_r($maoDeMatos->getSkills());            // Print user skills array in code block
echo '</code>' . PHP_EOL;

echo PHP_EOL;
echo 'Website Url : ';
echo '<a href="' . $maoDeMatos->getWebsiteUrl() . '">';
echo $maoDeMatos->getWebsiteUrl();            // Print user website url
echo '</a>';
```

## Mao De Matos
```php
Array
(
  [Frontend] => Array
  (
    [0] => "HTML"
    [1] => "CSS"
    [2] => "JavaScript/JQuery"
  )
  [Backend] => Array
  (
    [0] => "PHP"
    [1] => "MySQL/MariaDB"
  )
)
```
Website Url : http://maodematos.rf.gd/

<!---
MaoDeMatos/MaoDeMatos is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
