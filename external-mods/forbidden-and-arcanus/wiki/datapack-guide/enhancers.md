# Enhancers

Enhancers are special catalysts that allow the Hephaestus Forge and the Clibano to unlock new powers. \
\
Enhancers can be configured using JSON files within a data pack in the path `data/<namespace>/forbidden_arcanus/enhancer/definition`.



| Name          | Description                                         | Value                                                                                                                                                        | Required |
| ------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- |
| `description` | The description which is shown in the item tooltip. | A map with [Enhancer Targets](enhancers.md#enhancer-target) as keys and [JSON text components](https://minecraft.wiki/w/Raw\_JSON\_text\_format) as values.  | true     |
| `effects`     | The effects the enhancer has.                       |  A list of [Enhancer Effects](enhancers.md#enhancer-effect).                                                                                                 | true     |



### Example JSON

{% code lineNumbers="true" %}
```json
{
  "description": {
    "clibano": {
      "translate": "item.forbidden_arcanus.enhancer.crimson_stone.clibano"
    },
    "hephaestus_forge": {
      "translate": "item.forbidden_arcanus.enhancer.crimson_stone.hephaestus_forge"
    }
  },
  "effects": [
    {
      "type": "forbidden_arcanus:multiply_required_essence",
      "conditions": [],
      "essence_type": "souls",
      "multiplier": 0.5
    },
    {
      "type": "forbidden_arcanus:multiply_soul_duration",
      "conditions": [],
      "multiplier": 1.3
    }
  ]
}
```
{% endcode %}



### Enhancer Target

Currently there are two valid enhancer targets:

* `hephaestus_forge`
* `clibano`



### Enhancer Effect

Enhancer Effects determine the effects the Enhancer has. The following effects are possible:

* `multiply_required_essence`
* `modify_required_essence`
* `multiply_soul_duration`



#### Multiply Required Essence

Multiplies the given essence type with the given multiplier. Can be used to either increase or decrease the needed essence amount.

Enhancer Target: `hephaestus_forge`

| Name           | Description                 | Value                                         | Required |
| -------------- | --------------------------- | --------------------------------------------- | -------- |
| `type`         | The effect type.            | `forbidden_arcanus:multiply_required_essence` | true     |
| `essence_type` | The essence type to modify. |  An essence type.                             | true     |
| `multiplier`   | The multiplier to apply.    |  A double value.                              | true     |



#### Modify Required Essence

Add the provided value to the given essence type. The essence amount cannot get negative.

Enhancer Target: `hephaestus_forge`

| Name           | Description                 | Value                                       | Required |
| -------------- | --------------------------- | ------------------------------------------- | -------- |
| `type`         | The effect type.            | `forbidden_arcanus:modify_required_essence` | true     |
| `essence_type` | The essence type to modify. |  An essence type.                           | true     |
| `value`        | The value to add.           |  An int value.                              | true     |



#### Multiply Soul Duration

Multiplies the soul duration with the given multiplier.

Enhancer Target: `clibano`

| Name         | Description              | Value                                      | Required |
| ------------ | ------------------------ | ------------------------------------------ | -------- |
| `type`       | The effect type.         | `forbidden_arcanus:multiply_soul_duration` | true     |
| `multiplier` | The multiplier to apply. |  A double value. Range: 0.0-10.0           | true     |
