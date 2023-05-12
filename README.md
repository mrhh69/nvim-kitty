# vim-kitty - kitty config syntax highlighting for vim

Syntax highlighting for Kitty terminal config files.

Keywords based on `v0.27.1`

See [screenshot](https://github.com/fladson/vim-kitty/wiki) for a visual explanation of what this plugin does.

## File type detection

Any `*.conf` or `*.session` files in kitty's configuration directory is considered.

You can always add `# vim:ft=kitty` at the beginning of any file to make sure
the syntax is loaded, or you can set it temporarily with `:set ft=kitty`.

ex:

`init.lua`
```lua
vim.filetype.add({
	filename = {
		['kitty.conf'] = 'kitty',
	},
	pattern = {
		['.*%.[sS]'] = 'asm6502',
		['.*/kitty/.*%.conf'] = 'kitty',
	},

})
```
