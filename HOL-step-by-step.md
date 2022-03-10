# ローカル プロジェクトを作成する
このセクションでは、Visual Studio Code を使用して、ローカル Azure Functions プロジェクトを Java で作成します。 後からこの記事の中で、関数コードを Azure に発行します。

1. アクティビティ バーの Azure アイコンを選択し、 [Azure: Functions] 領域で [新しいプロジェクトの作成] アイコンを選択します。
   
   ![create-new-project](images/create-new-project.png "create-new-project.png")

2. プロジェクト ワークスペースのディレクトリの場所を選択し、 **[選択]** をクリックします。
   - 注意: これらの手順は、ワークスペースの外部で実行するように設計されています。 ここでは、ワークスペースに含まれるプロジェクト フォルダーは選択しないでください。

3. プロンプトで、次の情報を入力します。
   -  Select a language for your function project (関数プロジェクトの言語を選択してください): [] を選択します。
   -  Select a version of Java (Java のバージョンを選択してください): 関数が Azure で実行される Java バージョン または Java 8 を選択します。 ローカルで確認済みの Java バージョンを選択してください。
   -  Provide a group ID (グループ ID を指定してください): [] を選択します。
   -  Provide an artifact ID (アーティファクト ID を指定してください): [] を選択します。
   -  Provide a version (バージョンを指定してください): [] を選択します。
   -  Provide a package name (パッケージ名を指定してください): [] を選択します。
   -  Provide an app name (アプリ名を指定してください): [] を選択します。
   -  [承認レベル]: [] を選択します。この場合、すべてのユーザーが関数のエンドポイントを呼び出すことができます。 承認レベルについては、「承認キー」を参照してください。
   -  Select how you would like to open your project (プロジェクトを開く方法を選択してください): [] を選択します。

4. Visual Studio Code は、この情報を使用して、HTTP トリガーによる Azure Functions プロジェクトを生成します。 ローカル プロジェクト ファイルは、エクスプローラーで表示できます。 作成されるファイルの詳細については、「生成されるプロジェクト ファイル」を参照してください。

# 関数をローカルで実行する
Visual Studio Code を Azure Functions Core Tools と統合することで、このプロジェクトをローカルの開発用コンピューター上で実行してから、Azure に発行することができます。



