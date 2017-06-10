# liquid-types-spacemacs

Forked version of the official Spacemacs layer for LiquidHaskell. 

Integrates with Stack (using `stack exec`).

## Install

First, install Liquid Haskell: either globally (which is what I've done), or project-locally like Intero does (haven't tested this). For the former, just run

```sh
$ stack install liquidhaskell
```

Next, add this repo to your private layers:

```sh
$ git clone https://github.com/mrkgnao/liquid-types-spacemacs .emacs.d/private/liquid-types
```    

(Note that `~/.spacemacs.d/layers` is also fine. It's what I use, and may be a better choice if you use an `~/.spacemacs.d/init.el` file.)

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

    

    
