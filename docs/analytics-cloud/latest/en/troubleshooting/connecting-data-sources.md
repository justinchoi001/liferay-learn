# Connecting Data Sources

Misconfigured environments or data sources can prevent or disrupt access to Liferay DXP (DXP) data sources. Here's how to troubleshoot DXP data source issues.

## Retry Authorization

**Error Message:** `Unknown error. Please retry authorization.`

DXP data source access requires that your DXP instance be publicly available and that your Analytics Cloud instance be [registered with the DXP instance as an OAuth application](../getting-started/connecting-data-sources/connecting-liferay-dxp-using-oauth.md).

**Resolution:**

1. Follow the steps for [adding a Liferay DXP data source](../getting-started/connecting-data-sources/connecting-liferay-dxp-using-oauth.md).

1. [Register Analytics Cloud with your DXP instance](../getting-started/connecting-data-sources/connecting-liferay-dxp-using-oauth.md#registering-analytics-cloud-with-your-liferay-dxp-instance).

## Unsupported Version

**Error Message:** `Unsupported version. This method of connection does not support the data source Liferay version. Make sure you are connecting to Liferay 7.0/7.1 instance or try a different method of connection.`

**Resolution:**

1. Make sure to [connect with a Liferay DXP 7.0 or 7.1 instance].

1. Follow the steps for [adding a Liferay DXP data source](../getting-started/connecting-data-sources/connecting-liferay-dxp-using-oauth.md).

1. If the error persists, make sure JSON web services are enabled on your DXP instance. They're enabled by default. If you disabled them using a [portal property](https://docs.liferay.com/dxp/portal/7.1-latest/propertiesdoc/portal.properties.html#JSON) setting json.web.service.enabled=false (e.g., set in a [portal-ext.properties file](https://learn.liferay.com/dxp/7.x/en/installation-and-upgrades/reference/portal-properties.html)), delete the setting or set the property value to true.

## Invalid Credentials; Authorization Expired

**Error Message:** `Invalid Credentials. The authorization for this data source has expired. Please reauthorize the token in the OAuth tab.`

This message appears in the log:

```
WARN [http-nio-8080-exec-14][AbstractOAuthService:88] Unsecure HTTP, Transport Layer Security is recommended
```

Connection to a DXP data source requires that the DXP instance's web server protocol be forwarded.

**Resolution:**

1. Follow steps for adding a DXP data source, paying particular attention to [register Analytics Cloud with your DXP instance](../getting-started/connecting-data-sources/connecting-liferay-dxp-using-oauth.md#registering-analytics-cloud-with-your-liferay-dxp-instance).

1. If the issue persists and the web server protocol is forwarded, set these [portal properties](https://docs.liferay.com/dxp/portal/7.1-latest/propertiesdoc/portal.properties.html) in a [portal-ext.properties](https://learn.liferay.com/dxp/7.x/en/installation-and-upgrades/reference/portal-properties.html) file in your DXP instance.

```
web.server.forwarded.protocol.enabled=true
redirect.url.security.mode=domain
redirect.url.domains.allowed=
```
