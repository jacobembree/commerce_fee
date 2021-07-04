# commerce_fee
Commerce Fee submodule

Note: a modification is necessary in commerce file: commerce/src/Plugin/Field/FieldType/PluginItemDeriver.php
  * Modify method getDerivativeDefinitions()
  * add commerce_fee plugin to the $plugin_types array: 'commerce_fee' => $this->t('Commerce fee'),

OR

Get latest working patch from [here](https://www.drupal.org/project/commerce/issues/2903716) and add it to your `composer.json` similar to this and run composer install to patch commerce.

    "extra": {
        "enable-patching": true,
        "patches": {
          ...
            "drupal/commerce": {
                "Implement the ability to add fees to an order dgo.to/2903716": "https://www.drupal.org/files/issues/2020-11-18/add-plugin-type-2903716-72.patch"
            },
          ...