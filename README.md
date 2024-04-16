# オープンリソース版pymolのインストール

#Pymolの環境を作成
conda create -n pymol　

#作成した環境に入る
conda activate pymol

#環境内にPymolをインストールする
conda install -c conda-forge pymol-open-source


$ pymol
Traceback (most recent call last):
  File "/home/~ /miniconda3/envs/pymol/lib/python3.12/site-packages/pymol/__init__.py", line 72, in <module>
    import pymol
  File "/home/~ /miniconda3/envs/pymol/lib/python3.12/site-packages/pymol/__init__.py", line 558, in <module>
    import pymol._cmd
ImportError: libGL.so.1: cannot open shared object file: No such file or directory

と出たので、いろいろ調べて下記で解決

 sudo apt-get install libgl1-mesa-dev

 Do you want to continue? [Y/n] Y

 でどゎーっと更新が行われ

 ~$ pymol
 でPymolがじっこうできるようになった
 
