gtagsで飛ぶ gtagJump
	--- Fly with the gtags "tagJump" ---

	使い方(How to use)
		gfly.pluginとgflyフォルダを~/.local/share/gedit/plugins/にコピー
		copy "gtagJump.plugin" and "gtagJump/" to ~/.local/share/gedit/plugins/
		
			~(home)/
				.local/
					share/
						gedit/
							plugins/
								gtagJump.plugin
								gtagJump/
		
		編集→設定→プラグインでgflyを有効にする
		"edit"->"Preference"->"Plugins" and check "gtagJump"
		
		プロジェクトのフォルダでgtagsのデータベースを作る
		Create gtags database for your project
		
			src$ gtags -v
			src$ ls
			GTAGS GRTAGS GSYMS GPATH ...(your files)
		
		シンボル名の上にカーソルがあるときにF3を押す
		Push F3 on the symbol
		
			som|eFunction();
				F3
			|void someFunction() {
		
		Ctrl + F3 で呼び出し元に飛べます
		You can jump invoker when you push Ctrl + F3
		
			void someFunc|tion() {
				Ctrl + F3
			|someFunction();
		
		選択肢が複数ある場合にはダイアログが表示されます
		The dialog when there are multiple choices
		上下で選択してEnterキーを押してください．
		Use up and down key to select and push the Enter key
		
		Pythonを書いているのであれば，
		gtagsなしでも編集中のファイルの関数やクラスの定義へ飛ぶことができます
		writing Python, you can jump to definitions of functions and classes
		in the editing file without gtags.
		
	注意(Notes)
		
		GNU globalが必要です
		you need GNU global
		
			$ sudo apt-get install global
		
	キーバインディングを変更したい(You want to change key binding)
		
		__init__.pyを編集
		edit __init__.py
		
		geditを再起動
		restert gedit
		
	既知のバグ(Known Bugs)
		globalが使えない状況の場合の動作
		when the situation cannot use "global"
		他のファイルに飛んだ時のスクロール
		Scroll when jump to other file
		
	書いた人(Author)
		Masatoshi Tsushima
		Twitter: @utisam

