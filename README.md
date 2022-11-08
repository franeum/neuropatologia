# neuropatologia

## blackscreen:

```bash
ffmpeg -i mbuto.mp4 -vf "blackdetect=d=0.1:pix_th=.1" -an -f null - 2>&1 | grep blackdetect > provuma.txt
```

## fragments:

```bash
pip install --upgrade scenedetect[opencv]
scenedetect -i mbuto.mp4 detect-content -t 19.5 list-scenes
```

*19.5 potrebbe essere il valore giusto per intercettare il cambio di scene*