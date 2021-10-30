# fluentd-core-kube

fluentd-core-kube は、出力されたログを収集しDBまたはファイル等へ書き出すにあたり、必要不可欠なコアリソースです。
AION では、fluentd 環境を コア関連リソースとして、aion-core-manifests にて 定義しています。  

fluentd を動かすためには、fluentd-core-kube の他に、下記のようなレポジトリを参照して、設定を行う必要があります。  

* fluentd-for-docker-containers  

* fluentd-for-mongodb  

* fluentd-for-containers-mongodb-kube  

## 動作環境
fluentd-core-kube は、以下の動作環境を前提としています。  

OS: Linux OS  
CPU: ARM/AMD/Intel  
Kubernetes  

## サンプル定義ファイル  
本リポジトリには、fluentd-core-kube としてのサンプル定義ファイル fluentd-configmap.yaml が格納されています。  

## AION での fluentd の動作  
AION で fluentd を動かすためには、主にエッジコンピューティング環境の特性とシステム要求に留意して、aion-core-manifests に適切な追加設定を行う必要があります。  

## Dockerイメージの生成  
### 起動方法
以下のコマンドでDockerイメージを作成します。  
```
cd $HOME/端末名/Runtime/
git clone git@github.com.org:latonaio/fluentd-core-kube.git
cd fluentd-core-kube
make docker-build
```

### 現在利用しているプラグイン
現在のdockerイメージではfluentd用に以下のプラグインを使用しています。  

* fluent-plugin-mongo  

* fluent-plugin-rabbitmq  
