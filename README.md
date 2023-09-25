# ALBと統合したAutoScaling
## 構成
* HTTPでALBのDNS名にアクセス
* ターゲットグループにASGを指定
* EC2上のhttpdにアクセス

![sc-cfn-dev02](https://github.com/Toru-Kubota/AWS-CFn-Dev02/assets/102895466/4ce392d2-080d-4cfa-8eba-a645a8aa2cbb)

## パラメーター
### 02_02_SecurityGroup.yaml
* AllowedIP: 許可するグローバルIP
### 02_04_LaunchTemplate.yaml
* Prefix: 起動テンプレート名
### 02_05_ALB.yaml
* Prefix: ALB/TG名
### 02_06_AutoScalingGroup.yaml
* Prefix: ASG名