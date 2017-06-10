# liquid-types-spacemacs

Forked version of the official Spacemacs layer for LiquidHaskell. 

Integrates with Stack (using `stack exec`).

## Install

Add this layer to your private layers:

```elisp
    git clone https://github.com/mrkgnao/liquid-types-spacemacs .emacs.d/private/liquid-types
```    

Note that `~/.spacemacs.d/layers` is also fine.

Activate the layer in your `~/.spacemacs`:

```elisp
dotspacemacs-configuration-layers '(... syntax-checking haskell liquid-types)
```

Finally, set up the Flycheck checkers. Add the following in your `user-config` (or modify anything similar that might already be there):

```elisp
  (with-eval-after-load 'intero
    (flycheck-add-next-checker 'intero
                               'haskell-liquid
                               '(error . haskell-hlint)))
```

    

    
