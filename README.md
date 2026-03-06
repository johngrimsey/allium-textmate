# Allium TextMate Grammar

Syntax highlighting for [Allium](https://juxt.github.io/allium/) specification files (`.allium`).

## Installation

Clone (or download and unzip) this repository:

```bash
git clone https://github.com/overchain/allium-textmate.git
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
| Comments | `-- a comment` |
| Section dividers | `------------------------------------------------------------` |
| Control keywords | `rule`, `when`, `requires`, `ensures`, `let`, `invariant` |
| Declaration keywords | `value`, `entity`, `actor`, `surface`, `external`, `endpoint` |
| Import statements | `use "../shared/types.allium" as types` |
| Built-in types | `String`, `Integer`, `Timestamp`, `Record`, `Boolean`, `UUID`, `CSV` |
| Type names (declarations) | `value OrderStatus { ... }`, `rule PlaceOrder { ... }` |
| Type references | PascalCase names used as types, e.g. `status: OrderStatus` |
| Property declarations | `name: String` — property and type get distinct colours |
| Namespace-qualified types | `types.MyValueType` |
| Function/predicate calls | `OrderIsValid(order)`, `ResponseReturned(...)` |
| Endpoint declarations | `endpoint GET "/orders"` |
| HTTP methods | `GET`, `POST`, `PUT`, `PATCH`, `DELETE` |
| Parameter keywords | `query`, `body`, `response`, `semantics`, `note`, `base_path` |
| Annotations | `(required)`, `(optional)` |
| String literals | `'pending'`, `"/api/orders"` |
| Logical operators | `not`, `or`, `and`, `null`, `true`, `false` |
| Operators | `=`, `!=`, `=>` |
| Nullable markers | `?` |
