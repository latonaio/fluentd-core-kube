# fluentd-core-kube

fluentd-core-kube は、出力されたログを収集しDBまたはファイル等へ書き出すにあたり、必要不可欠なコアリソースです。  
AION では、fluentd 環境を コア関連リソースとして、aion-core-manifests にて 定義しています。  

fluentd を動かすためには、fluentd-core-kube の他に、下記のようなレポジトリを参照して、設定を行う必要があります。  

* fluentd-for-docker-containers-kube  

* fluentd-for-mongodb-kube  

* fluentd-docker-mongodb-kube  

# サンプル定義ファイル  
本リポジトリには、fluentd-core-kube としてのサンプル定義ファイル fluentd-configmap.yaml が格納されています。  

# AION での fluentd の動作  
AION で fluentd を動かすためには、主にエッジコンピューティング環境の特性とシステム要求に留意して、aion-core-manifests に適切な追加設定を行う必要があります。