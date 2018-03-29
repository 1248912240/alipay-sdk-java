
```
�������ԣ�JAVA
����JDK�汾��1.5
��Ȩ�����Ͻ��ڷ�����
```

## ��Ҫ���ļ�����˵��
```
DefaultAlipayClient.java
public DefaultAlipayClient(String serverUrl, String appId, String privateKey);
```
+ ���ܣ����췽��
+ ���룺
    + serverUrl �ǿգ������������ַ�����ԣ�http://openapi.alipaydev.com/gateway.do ���ϣ�https://openapi.alipay.com/gateway.do ��
    + appId �ǿգ�Ӧ��ID
    + privateKey �ǿգ�˽Կ
+ ��������ÿͻ���ʵ������

```
DefaultAlipayClient.java
public <T extends AlipayResponse> T execute(AlipayRequest<T> request);
```
+ ���ܣ�ִ��������ã������ڲ���Ҫ��Ȩ�ӿڵ��ã�
+ ���룺request �ӿ��������
+ �����T  ���󷵻ض���

```
DefaultAlipayClient.java
public <T extends AlipayResponse> T execute(AlipayRequest<T> request, String accessToken);
```
+ ���ܣ�ִ��������ã���������Ҫ��Ȩ�ӿڵ��ã�
+ ���룺
    + request �ӿ��������
    + authToken ��Ȩ����
+ �����T  ���󷵻ض���

## ����ʾ��


## ǩ�������
```
AlipaySignature.java
public static String rsaSign(Map<String, String> params, String privateKey, String charset);
```
+ ���ܣ�RSAǩ��
+ ���룺
    + params ��ǩ������map
    + privateKey ˽Կ
    + charset ǩ�������ʽ
+ �����ǩ�����

```
AlipaySignature.java
public static boolean rsaCheckV2(Map<String, String> params, String publicKey, String charset);
```
+ ���ܣ�RSA��ǩ
+ ���룺
    + params ǩ����������map
    + publicKey ��Կ
    + charset ǩ�������ʽ
+ �������ǩ���

```
AlipaySignature.java
public static boolean rsaCheckContent(String content, String sign, String publicKey,String charset);
```
+ ���ܣ�RSA��ǩ
+ ���룺
    + content ǩ�����������ַ���
    + sign ǩ��
    + publicKey ��Կ
    + charset ǩ�������ʽ
+ �������ǩ���

