---
-api-id: M:Windows.Security.Cryptography.Core.CryptographicEngine.SignHashedData(Windows.Security.Cryptography.Core.CryptographicKey,Windows.Storage.Streams.IBuffer)
-api-type: winrt method
---

<!-- Method syntax
public Windows.Storage.Streams.IBuffer SignHashedData(Windows.Security.Cryptography.Core.CryptographicKey key, Windows.Storage.Streams.IBuffer data)
-->

# Windows.Security.Cryptography.Core.CryptographicEngine.SignHashedData

## -description
Signs the hashed input data using the specified key.

## -parameters
### -param key
The key to use to sign the hash. This key must be an asymmetric key obtained from a [PersistedKeyProvider](persistedkeyprovider.md) or [AsymmetricKeyAlgorithmProvider](asymmetrickeyalgorithmprovider.md).

### -param data
The input data to sign. The data is a hashed value which can be obtained through incremental hash.

## -returns
The signed data.

## -remarks
<!--<rem  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">If the <mark type="param">key</mark> parameter is a persisted key, user input may be required for a hardware key, strongly protected key, or shared user key.</rem>-->
The input data supplied to the [SignHashedData](cryptographicengine_signhasheddata.md) method is a hashed value. To sign raw data that has not been hashed, use the [SignAsync](cryptographicengine_signasync.md) method.

If the key is a persisted key and the operation requires UI or takes a long time, use the [SignHashedDataAsync](cryptographicengine_signhasheddataasync.md) method instead.

## -examples

## -see-also
