# Issue:
https://github.com/mason-org/mason.nvim/issues/1578

# Solution:
## Works:
- https://github.com/mason-org/mason.nvim/issues/1578#issuecomment-2455253723

tested:
- ARM Cromebook - Lenovo 300e

```
sudo install clangd jq
mkdir -p ~/.local/share/nvim/mason/packages/clangd/mason-schemas
cd ~/.local/share/nvim/mason/packages/clangd
curl https://raw.githubusercontent.com/clangd/vscode-clangd/master/package.json \
    | jq .contributes.configuration > mason-schemas/lsp.json
echo '{"schema_version":"1.1","primary_source":{"type":"local"},"name":"clangd","links":{"share":{"mason-schemas/lsp/clangd.json":"mason-schemas/lsp.json"}}}' \
    > mason-receipt.json
```

## alt:
- https://github.com/mason-org/mason.nvim/issues/1578#issuecomment-2725266573
- https://github.com/mason-org/mason.nvim/issues/1578#issuecomment-2927987751
- https://github.com/mason-org/mason.nvim/issues/1578#issuecomment-3292680782

# sch:
- https://www.google.com/search?q=mason+aarch64+The+current+platform+is+unsupported
- https://www.google.com/search?q=mason+ARM+The+current+platform+is+unsupported
- https://www.google.com/search?q=mason+The+current+platform+is+unsupported

# discuss:
https://stackoverflow.com/questions/77631658/encountering-the-current-platform-is-unsupported-error-while-installing-clangd
https://www.reddit.com/r/neovim/comments/18xhrxa/mason_clangd_lsp_doesnt_work_on_arm_how_to/
