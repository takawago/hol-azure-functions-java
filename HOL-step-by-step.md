

# ローカル プロジェクトを作成する
このセクションでは、Visual Studio Code を使用して、ローカル Azure Functions プロジェクトを Java で作成します。 後からこの記事の中で、関数コードを Azure に発行します。

1. アクティビティ バーの Azure アイコンを選択し、 [Azure: Functions] 領域で [新しいプロジェクトの作成] アイコンを選択します。
![create-new-project](images/create-new-project.png "create-new-project.png")

2. プロジェクト ワークスペースのディレクトリの場所を選択し、 **[選択]** をクリックします。
   - 注意: これらの手順は、ワークスペースの外部で実行するように設計されています。 ここでは、ワークスペースに含まれるプロジェクト フォルダーは選択しないでください。

3. プロンプトで、次の情報を入力します。
   -  Select a language for your function project (関数プロジェクトの言語を選択してください): [`Java`] を選択します。
   -  Select a version of Java (Java のバージョンを選択してください): 関数が Azure で実行される Java バージョン または Java 8 を選択します。 ローカルで確認済みの Java バージョンを選択してください。
   -  Provide a group ID (グループ ID を指定してください): [`com.function`] を選択します。
   -  Provide an artifact ID (アーティファクト ID を指定してください): [`myFunction`] を選択します。
   -  Provide a version (バージョンを指定してください): [`1.0-SNAPSHOT`] を選択します。
   -  Provide a package name (パッケージ名を指定してください): [`com.function`] を選択します。
   -  Provide an app name (アプリ名を指定してください): [`myFunction-12345`] を選択します。
   -  [承認レベル]: [Anonymous] を選択します。この場合、すべてのユーザーが関数のエンドポイントを呼び出すことができます。 承認レベルについては、「承認キー」を参照してください。
   -  Select how you would like to open your project (プロジェクトを開く方法を選択してください): [`Add to workspace`] を選択します。

4. Visual Studio Code は、この情報を使用して、HTTP トリガーによる Azure Functions プロジェクトを生成します。 ローカル プロジェクト ファイルは、エクスプローラーで表示できます。 作成されるファイルの詳細については、「生成されるプロジェクト ファイル」を参照してください。

# 関数をローカルで実行する
Visual Studio Code を [Azure Functions Core Tools](https://docs.microsoft.com/ja-jp/azure/azure-functions/functions-run-local) と統合することで、このプロジェクトをローカルの開発用コンピューター上で実行してから、Azure に発行することができます。

1. 関数を呼び出すには、F5 キーを押して関数アプリ プロジェクトを起動します。 Core Tools からの出力がターミナル パネルに表示されます。 アプリがターミナル パネルで起動します。 HTTP によってトリガーされる関数の URL エンドポイントがローカルで実行されていることを確認できます。
![functions-vscode-f5.png](images/functions-vscode-f5.png "functions-vscode-f5.png")
Windows での実行に問題がある場合、Visual Studio Code の既定のターミナルが WSL Bash に設定されていないことをご確認ください。

2. Core Tools を実行したまま、**Azure: Functions** 領域に移動します。 [Functions] の [ローカル プロジェクト][Functions] を展開します。  関数を右クリック (Windows) または Ctrl キーを押しながらクリック (macOS) して、[Execute Function Now](今すぐ関数を実行) を選択します。
