# commerce_fee
Commerce Fee submodule

Note: a modification is necessary in commerce file: commerce/src/Plugin/Field/FieldType/PluginItemDeriver.php
  * Modify method getDerivativeDefinitions()
  * add commerce_fee_policy to the $plugin_types:
  
    $plugin_types = [
      'commerce_condition' => $this->t('Condition'),
      'commerce_promotion_offer' => $this->t('Promotion offer'),
      'commerce_fee_policy' => $this->t('Fee policy'),
    ];  