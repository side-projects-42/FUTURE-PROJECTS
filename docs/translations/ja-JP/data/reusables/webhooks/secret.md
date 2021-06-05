webhookのシークレットを設定することで、ペイロードのURLに送信される`POST`リクエストが、{% data variables.product.product_name %}からのものであることが保証できます。 シークレットを設定すると、webhookの`POST`リクエスト中の{% if currentVersion == "free-pro-team@latest" or currentVersion ver_gt "enterprise-server@2.22" or currentVersion == "github-ae@latest" %}`X-Hub-Signature`及び`X-Hub-Signature-256`ヘッダ{% elsif currentVersion ver_lt "enterprise-server@2.23" %}`X-Hub-Signature`ヘッダ{% elsif currentVersion == "github-ae@latest" %}`X-Hub-Signature-256`ヘッダ{% endif %}を受信することになります。 署名ヘッダでシークレットを使用してwebhookのペイロードをセキュアに保つ方法に関する詳細については、「[webhookをセキュアに保つ](/webhooks/securing/)」を参照してください。