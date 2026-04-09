# seminar2_anaconda_explanation
**1. anacondaとは何か**

---

Anaconda は「Pythonツールパッケージ」である



* Python本体とよく使われるライブラリがあらかじめ含まれている

* condaで環境を管理する

  >相互に独立したenvironmentを作成することができ、異なる環境で異なるバージョンのpythonやpackageをインストールできる，

  >複数のプログラムで異なるバージョンのpythonやpackageが必要な場合に非常に有用である

---

**2. Anacondaの使い方**

---
- 法政大学の貸与PCにはすでにanacondaおよびanaconda navigator（GUIのanaconda操作ツール）がインストールされているが、環境変数が設定されていないため、事前に設定が必要である
  - anacondaのscriptを環境変数に追加する
 
  - anacondaのコマンドライン操作

    （1）cmdコマンドウィンドウで仮想環境を作成する
    
    ```bash
    win+R
    ```
    
    ```bash
    cmd
    ```
    
    ```bash
    conda create -n 自分で付ける環境名 python=必要なバージョン
    ```
    
    example:
    ```bash
    conda create -n myenv python=3.10
    ```
    >具体的なpythonのバージョンを指定しない場合は最新バージョンがインストールされる
    
    >anaconda navigatorを使って仮想環境を作成することも可能である
 
    （2）仮想環境を有効化する
    
    ```bash
    conda activate 自分で付ける環境名
    ```
    （3）仮想環境を終了する
    
    ```bash
    conda deactivate
    ```
    （4）仮想環境を削除する
 
    ```bash
    conda remove -n 自分で付ける環境名 --all
    ```
    
    （5）pythonライブラリのインストールコマンド
      >packageをインストールするためのコマンドライン操作であり、ide上でもインストール可能である
      >コマンドラインでインストールする場合は必ず先に仮想環境を有効化すること
      
    ```bash
    conda install numpy=2.4.0
    ```

---
**3. ide上でanacondaを使用する**

---
- 皆さんはどのideを使っていますか？pycharm？ visual studio code？
 
  **（1） pycharmでのanacondaの使用方法**
  
     A.```New Project```で：```Python Interpreter```を見つける

     B.```Conda Environment```を選択する

     C.```Existing environment```を選択する

     D.パスを指定する。例：```anaconda/envs/myenv/python.exe```

     E.プロジェクトを作成する

  **（2）vs codeでのanacondaの使用方法**
  
     **A. Pythonプラグインをインストールする**

    - VS Code を開く → ```拡張（Extensions）```

    - ```Python extension for Visual Studio Code```をインストールする

     **B. プロジェクトフォルダを開く**

    - ```VS Code → File → Open Folder```でプロジェクトフォルダを開く
 
     **C. anaconda環境を選択する**
  
    - ```Ctrl + Shift + P```を押す

    - ```Python: Select Interpreter```と入力してクリックする
 
    - 作成した環境を選択する。例：```自分で付ける環境名 (conda)```
 
     **D. 成功したかどうかを確認する**

    ```test.py```を新規作成：
    ```python
    import sys
    print(sys.executable)
    ```
    以下のパスが含まれていれば：
        
    ```anaconda/envs/自分で付ける環境名```
        
    成功である

    **E. ターミナルの同期**

  VS Code のターミナルで：```conda activate 自分で付ける環境名```を実行する
# seminar2_anaconda_explanation
**1.什么是anaconda**

---

Anaconda 是一个“Python工具包”



* 自带 Python 和常用库

* 用 conda 管理环境

  >可以创建相互隔离的environment，在不同的环境下可以安装不同版本的python，以及package，

  >在需要应对每个几个程序需要不同版本的python或者package的时候很有用

---

**2.如何使用Anaconda**

---
- 法政大学的貸与PC已经安装了anaconda以及anaconda navigator（有图像界面的anaconda的操作台）但是没有配置环境变量，需要先做一定的设定
  - 添加anaconda的script到环境变量中
 
  - anaconda的命令行操作

    （1）cmd命令窗口创建虚拟环境
    
    ```bash
    win+R
    ```
    
    ```bash
    cmd
    ```
    
    ```bash
    conda create -n 自己起的环境名 python=需要的版本号
    ```
    
    example:
    ```bash
    conda create -n myenv python=3.10
    ```
    >不加具体的python版本号就会下载最新版本的python
    
    >也可以通过anaconda navigator创建虚拟环境
 
    （2）激活虚拟环境
    
    ```bash
    conda activate 自己起的环境名
    ```
    （3）退出虚拟环境
    
    ```bash
    conda deactivate
    ```
    （4）删除虚拟环境
 
    ```bash
    conda remove -n 自己起的环境名 --all
    ```
    
    （5）python库函数的安装命令
      >安装package的命令行操作，也可以在ide里安装
      >使用命令行安装注意要先激活虚拟环境
      
    ```bash
    conda install numpy=2.4.0
    ```

---
**3.在ide上使用anaconda**

---
- 大家使用什么ide？pycharm？ visual studio code？
 
  **（1） pycharm上anaconda的使用方法**
  
     A.在```New Project```中找到：```Python Interpreter```

     B.选择：```Conda Environment```

     C.选：```Existing environment```

     D.找到路径，比如：```anaconda/envs/myenv/python.exe```

     E.创建项目

  **（2）vs code上anaconda的使用方法**
  
     **A.安装 Python 插件**

    - 打开 VS Code → ```扩展（Extensions）```

    - 安装：```Python extension for Visual Studio Code```

     **B.打开项目文件夹**

    - 打开你的项目文件夹：```VS Code → File → Open Folder```
 
     **C.选择anaconda环境**
  
    - 按```Ctrl + Shift + P```

    - 输入并点击：```Python: Select Interpreter```
 
    - 选择你创建的环境，例如：```自己起的环境名 (conda)```
 
     **D.测试是否成功**

    新建 ```test.py```：
    ```python
    import sys
    print(sys.executable)
    ```
    如果路径里有：
        
    ```anaconda/envs/自己起的环境名```
        
    说明成功

    **E.终端同步**

  在 VS Code 终端输入：```conda activate 自己起的环境名```

