---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: f1b944e2673c9682a0194c4996fa4d2b34fae97b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952155"
---
# <span data-ttu-id="8b839-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b839-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8b839-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b839-102">SYNOPSIS</span></span>
<span data-ttu-id="8b839-103">애플리케이션 게이트웨이에 대한 SSL 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="8b839-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b839-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b839-105">설명</span><span class="sxs-lookup"><span data-stu-id="8b839-105">DESCRIPTION</span></span>
<span data-ttu-id="8b839-106">**Set-AzApplicationGatewaySslCertificate** cmdlet은 애플리케이션 게이트웨이에 대한 SSL 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="8b839-107">예제</span><span class="sxs-lookup"><span data-stu-id="8b839-107">EXAMPLES</span></span>

### <span data-ttu-id="8b839-108">예제 1: Application Gateway에서 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="8b839-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="8b839-109">ApplicationGateway01이라는 애플리케이션 게이트웨이에 대한 기존 SSL 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="8b839-110">예제 2: Application Gateway에서 KeyVault Secret(version-less secretId)를 사용하여 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="8b839-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8b839-111">를 사용하여 비밀을 얻고 기존 SSL 인증서를 `Set-AzApplicationGatewaySslCertificate` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="8b839-112">예제 3: Application Gateway의 KeyVault Secret를 사용하여 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="8b839-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8b839-113">를 사용하여 비밀을 얻고 기존 SSL 인증서를 `Set-AzApplicationGatewaySslCertificate` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="8b839-114">참고: Application Gateway가 KeyVault와 인증서를 동기화해야 하는 경우 버전이 적은 secretId를 제공하십시오.</span><span class="sxs-lookup"><span data-stu-id="8b839-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="8b839-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b839-115">PARAMETERS</span></span>

### <span data-ttu-id="8b839-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b839-116">-ApplicationGateway</span></span>
<span data-ttu-id="8b839-117">SSL(Secure Socket Layer) 인증서가 연결된 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b839-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8b839-118">-CertificateFile</span></span>
<span data-ttu-id="8b839-119">SSL 인증서의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-119">Specifies the path of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b839-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b839-120">-DefaultProfile</span></span>
<span data-ttu-id="8b839-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b839-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="8b839-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="8b839-123">KeyVault Secret의 SecretId(uri)입니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="8b839-124">특정 버전의 비밀을 사용해야 하는 경우 이 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-124">Use this option when a specific version of secret needs to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b839-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8b839-125">-Name</span></span>
<span data-ttu-id="8b839-126">SSL 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-126">Specifies the name of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b839-127">-Password</span><span class="sxs-lookup"><span data-stu-id="8b839-127">-Password</span></span>
<span data-ttu-id="8b839-128">SSL 인증서의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b839-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b839-129">CommonParameters</span></span>
<span data-ttu-id="8b839-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b839-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b839-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8b839-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b839-132">입력</span><span class="sxs-lookup"><span data-stu-id="8b839-132">INPUTS</span></span>

### <span data-ttu-id="8b839-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b839-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b839-134">출력</span><span class="sxs-lookup"><span data-stu-id="8b839-134">OUTPUTS</span></span>

### <span data-ttu-id="8b839-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b839-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b839-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b839-136">NOTES</span></span>

## <span data-ttu-id="8b839-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b839-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b839-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b839-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8b839-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b839-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8b839-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b839-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8b839-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8b839-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


