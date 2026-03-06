# Allium TextMate Grammar

Syntax highlighting for [Allium](https://juxt.github.io/allium/) specification files (`.allium`).

## Installation

Clone (or download and unzip) this repository:

```bash
git clone https://github.com/johngrimsey/allium-textmate.git
```

### IntelliJ IDEA / WebStorm / Rider

1. Open **Settings → Editor → TextMate Bundles**
2. Click **+** and select the cloned `allium-textmate` directory
3. Restart the IDE if prompted

### VS Code

Symlink the cloned directory into your VS Code extensions folder:

```bash
# macOS / Linux
ln -s "$(pwd)/allium-textmate" ~/.vscode/extensions/allium-language

# Windows (PowerShell, run as admin)
New-Item -ItemType SymbolicLink -Path "$env:USERPROFILE\.vscode\extensions\allium-language" -Target "$(Get-Location)\allium-textmate"
```

Restart VS Code.

### Sublime Text

1. Open **Preferences → Browse Packages…**
2. Copy (or symlink) the cloned `allium-textmate` directory into the opened `Packages/` folder
3. Restart Sublime Text

## What gets highlighted

| Element | Examples |
|---|---|
| Version marker | `-- allium: 2` |
| Comments | `-- a comment` |
| Section dividers | `------------------------------------------------------------` |
| Control keywords | `rule`, `when`, `requires`, `ensures`, `let`, `invariant`, `if`, `else`, `for` |
| Declaration keywords | `value`, `entity`, `actor`, `surface`, `external`, `endpoint`, `contract`, `variant`, `enum`, `given`, `config`, `default`, `deferred` |
| Import statements | `use "../shared/types.allium" as types` |
| Built-in types | `String`, `Integer`, `Decimal`, `Timestamp`, `Duration`, `Record`, `Boolean`, `UUID`, `CSV`, `Any`, `Set`, `List`, `ByteArray` |
| Generic types | `Set<Item>`, `List<Node?>` |
| Type names (declarations) | `value OrderStatus { ... }`, `contract Codec { ... }` |
| Type references | PascalCase names used as types, e.g. `status: OrderStatus` |
| Property declarations | `name: String` — property and type get distinct colours |
| Namespace-qualified refs | `types.MyValueType`, `core/config.timeout` |
| Function/predicate calls | `OrderIsValid(order)`, `ResponseReturned(...)` |
| Variant inheritance | `variant Leaf : Node { ... }` |
| Default instances | `default Role viewer = { ... }` |
| Surface keywords | `facing`, `context`, `exposes`, `provides`, `contracts`, `demands`, `fulfils`, `related`, `timeout`, `identified_by` |
| `@` annotations | `@guidance`, `@invariant`, `@guarantee` |
| Endpoint declarations | `endpoint GET "/orders"` |
| HTTP methods | `GET`, `POST`, `PUT`, `PATCH`, `DELETE` |
| Parameter keywords | `query`, `body`, `response`, `semantics`, `note`, `base_path` |
| Parameter annotations | `(required)`, `(optional)` |
| Expression keywords | `transitions_to`, `becomes`, `created`, `where`, `with`, `in` |
| Logical operators | `not`, `or`, `and`, `implies`, `exists`, `null`, `true`, `false` |
| Built-in values | `now`, `this` |
| Duration literals | `7.days`, `24.hours`, `30.seconds` |
| String literals | `'pending'`, `"/api/orders"` |
| Operators | `=`, `!=`, `>=`, `<=`, `>`, `<`, `+`, `-`, `*`, `/`, `=>`, `->`, `??` |
| Nullable markers | `?` |
| Open questions | `open question "Should admins ...?"` |
