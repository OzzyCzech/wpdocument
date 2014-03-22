# WP Document

Super simple database document for Wordpress

    class Something extends \om\WpDocument {
      public $propertyone = true;
      /** @var bool */
      public $propertytwo = 'default value';

      public function __construct() {
        $this->currency = 'CZK'; // TODO from options
      }

    }

Simplify from id creation and save updates

    $something = Something::fromId(1);
    $something->propertyone = fasle;
    $something->propertytwo = 'add something';
    $something->save(); // that's all


## Key properties

- super simple document interface
- constructor free parent
- table prefix support
- late static binding table names