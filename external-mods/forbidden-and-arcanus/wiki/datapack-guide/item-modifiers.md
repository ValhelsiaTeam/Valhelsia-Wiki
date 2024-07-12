# Item Modifiers

Item Modifiers add special abilities to your tools.\
\
Item Modifiers can be configured using JSON files within a data pack in the path `data/<namespace>/forbidden_arcanus/item_modifier`.



{% hint style="warning" %}
Currently, the modifier effects are hardcoded and cannot be changed through data packs.
{% endhint %}



| Name                        | Description                                                                  | Value                                                            | Required |
| --------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------- | -------- |
| `predicate`                 | Determines which item the modifier can be applied to.                        | An item predicate.                                               | true     |
| `incompatible_items`        | An additional item filter for the predicate.                                 | An item, a list of items, or an item tag.                        | false    |
| `incompatible_enchantments` | Determines which enchantments are incompatible with this modifier.           | An enchantment, a list of enchantments, or an enchantment tag.   | false    |
| `components_to_remove`      | These data components get removed from the item after applying the modifier. | One data component or a list of data components.                 | false    |
| `display`                   | Everything related to the representation of the modifier.                    | A [Display Settings](item-modifiers.md#display-settings) object. | true     |



### Example JSON

The following code is used to create the Eternal item modifier.

{% code lineNumbers="true" %}
```json
{
  "components_to_remove": [
    "minecraft:damage",
    "minecraft:max_damage"
  ],
  "display": {
    "name": {
      "translate": "modifier.forbidden_arcanus.eternal"
    },
    "texture": "forbidden_arcanus:textures/gui/tooltip/eternal.png",
    "tooltip_color": {
      "end": -13551304,
      "start": -5589601
    }
  },
  "incompatible_enchantments": "#forbidden_arcanus:modifier/eternal_incompatible",
  "incompatible_items": "#forbidden_arcanus:modifier/eternal_incompatible",
  "predicate": {
    "predicates": {
      "valhelsia_core:all_of": {
        "valhelsia_core:has_component": [
          "minecraft:max_damage",
          "minecraft:damage"
        ]
      }
    }
  }
}
```
{% endcode %}



### Display Settings

| Name            | Description                                     | Value                                                                       | Required |
| --------------- | ----------------------------------------------- | --------------------------------------------------------------------------- | -------- |
| `name`          | The prefix that gets added to the item.         |  A [JSON text component](https://minecraft.wiki/w/Raw\_JSON\_text\_format). | true     |
| `texture`       | The texture for the custom tooltip decorations. | A valid resource location.                                                  | true     |
| `tooltip_color` | The colors for the custom tooltip border.       | A pair consisting of two int values: `start` and `end`.                     | true     |
