## yay

This PKGBUILD of `yay` removes the `sudo` dependency.

To make sure no features are lost, use the following alias (place it in your shell's rc file)

```
alias yay="yay --sudo $(which doas)"
```

