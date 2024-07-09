# Magic Circles

A magic circle consists of two textures: one inner texture and one outer texture. Currently magic circles are only displayed during rituals executed at the [Hephaestus Forge](../blocks/hephaestus-forge/).\
\
Magic Circles can be configured using JSON files within a data pack in the path `data/<namespace>/forbidden_arcanus/magic_circle`.



| Name            | Description        | Value                       | Required |
| --------------- | ------------------ | --------------------------- | -------- |
| `inner_texture` | The inner texture. | A valid resource location.  | true     |
| `outer_texture` | The outer texture. |  A valid resource location. | true     |



### Built-in types

F\&A currently provides three different built-in magic circles you can use.

* `create_item`
* `upgrade_tier`
* `upgrade_final_tier`



### Example JSON

{% code lineNumbers="true" %}
```json
{
  "inner_texture": "forbidden_arcanus:textures/effect/magic_circle/inner/union.png",
  "outer_texture": "forbidden_arcanus:textures/effect/magic_circle/outer/pure.png"
}
```
{% endcode %}
