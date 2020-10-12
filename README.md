# wvd-deploy-template


## 必須構成
- 仮想ネットワーク
- Azure ADDS or WSAD + AADC
- FileServer

## オプション構成
- Azure Bastion
- Azure Firewall
- Azure NetApp Files
- Virtual Network Gateway

1. Azure AD グループ (AAD DC Administrators) 作成 
2. 共有イメージギャラリー展開
3. Azure Image 展開
4. カスタムイメージ展開
5. 仮想ネットワーク展開
6. Azure ADDS 展開
7. ドメイン参加用ユーザー作成
8. ファイルサーバー VM 展開


1. 共有イメージギャラリー展開
2. Azure Image 展開
3. カスタムイメージ展開
4. 仮想ネットワーク展開
5. VPN ゲートウェイ 展開
7. ドメイン参加用ユーザー作成
8. ファイルサーバー VM 展開


## サブスクリプション単位の実行
```
New-AzSubscriptionDeployment `
  -Name wvdDemoDeployment `
  -Location japaneast `
  -TemplateUri "https://raw.githubusercontent.com/sny0421/wvd-deploy-template/master/subscription-main-template.json" `
  -prefixString WVD-DEMO
```
