# Hephaestus Forge Rituals

Rituals are special crafting recipes executed at the [Hephaestus Forge](../blocks/hephaestus-forge/) multiblock. However, they don't use the default Minecraft recipe system and thus can't be modified with mods like KubeJS in the normal way.\
\
Rituals can be configured using JSON files within a data pack in the path `data/<namespace>/forbidden_arcanus/hephaestus_forge/ritual`.



| Name               | Description                                                                                | Value                                                                      | Required |
| ------------------ | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- | -------- |
| `inputs`           | These are the items placed on the surrounding pedestals.                                   | An array of [ritual inputs](hephaestus-forge-rituals.md#ritual-input).     | true     |
| `main_ingredient`  | The item placed in the main slot of the Forge.                                             | An ingredient. Must not be empty.                                          | true     |
| `result`           | The result of the ritual.                                                                  | A [ritual result](hephaestus-forge-rituals.md#ritual-result).              | true     |
| `essences`         | The required essence amounts.                                                              | An[ essences definition](hephaestus-forge-rituals.md#essences-definition). | true     |
| `forger_tier`      | The required forge tier.                                                                   | An int. Defaults to 1.                                                     | false    |
| `match_tier_exact` | If the forge tier needs to exactly match the required `forge_tier` for the ritual to work. | A boolean. Defaults to false.                                              | false    |
| `enhancers`        | The required [Enhancers](../items/enhancer-relics.md) for the ritual.                      | Either one enhancer (by ID) or a list (containing IDs).                    | false    |
| `magic_circle`     | The magic circle to display while the ritual is active.                                    | A magic circle (by ID)                                                     | true     |
| `duration`         | The duration the ritual takes to complete (in ticks).                                      |  A positive int. Defaults to 500.                                          | false    |



### Example JSON

The following JSON file is used to create the Terrastomp Prism ritual. More examples can be found on the [GitHub](https://github.com/stal111/Forbidden-Arcanus/tree/189c3ca451af186415e3e2f3f0fbb4d8226819b6/src/generated/resources/data/forbidden\_arcanus/forbidden\_arcanus/hephaestus\_forge/ritual).

{% code lineNumbers="true" %}
```json
{
  "enhancers": "forbidden_arcanus:elementarium",
  "essences": {
    "aureal": 300,
    "blood": 1500,
    "souls": 9
  },
  "forge_tier": 2,
  "inputs": [
    {
      "amount": 2,
      "ingredient": {
        "item": "minecraft:flint"
      }
    },
    {
      "amount": 2,
      "ingredient": {
        "item": "minecraft:dripstone_block"
      }
    },
    {
      "amount": 2,
      "ingredient": {
        "item": "minecraft:pointed_dripstone"
      }
    }
  ],
  "magic_circle": "forbidden_arcanus:create_item",
  "main_ingredient": {
    "item": "minecraft:diamond_block"
  },
  "result": {
    "type": "forbidden_arcanus:create_item",
    "result_item": {
      "count": 1,
      "id": "forbidden_arcanus:terrastomp_prism"
    }
  }
}
```
{% endcode %}



### Ritual Input



| Name         | Description                                                     | Value                             | Required |
| ------------ | --------------------------------------------------------------- | --------------------------------- | -------- |
| `ingredient` | An acceptable ingredient.                                       | An ingredient. Must not be empty. | true     |
| `amount`     | The number of items on pedestals the ingredient needs to match. |  A positive int.                  | false    |



### Ritual Result

The ritual result determines the outcome of the ritual. Currently there are two types:&#x20;

* `forbidden_arcanus:create_item`
* `forbidden_arcanus:upgrade_tier`

#### Create Item

Places the `result_item` in the main slot of the forge.

| Name          | Description            | Value                           | Required |
| ------------- | ---------------------- | ------------------------------- | -------- |
| `type`        | The result type.       | `forbidden_arcanus:create_item` | true     |
| `result_item` | The result item stack. | An item.                        | true     |



#### Upgrade Tier

Upgrades the forge tier to the next one if a higher one is available.

<table><thead><tr><th width="187">Name</th><th>Description</th><th>Value</th><th>Required</th></tr></thead><tbody><tr><td><code>type</code></td><td>The result type.</td><td><code>forbidden_arcanus:upgrade_tier</code></td><td>true</td></tr></tbody></table>



### Essences Definition

| Name         | Description               | Value               | Required |
| ------------ | ------------------------- | ------------------- | -------- |
| `aureal`     | The amount of aureal.     | A non-negative int. | false    |
| `blood`      | The amount of blood.      | A non-negative int. | false    |
| `souls`      | The amount of souls.      | A non-negative int. | false    |
| `experience` | The amount of experience. | A non-negative int. | false    |
