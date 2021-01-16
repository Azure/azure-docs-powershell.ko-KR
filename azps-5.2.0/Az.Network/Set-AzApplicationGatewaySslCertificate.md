---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1dd4285b75f8c1c067f15be34a334d4d48fb4f7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372254"
---
# <span data-ttu-id="3fe27-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fe27-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3fe27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fe27-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe27-103">애플리케이션 게이트웨이에 대한 SSL 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="3fe27-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fe27-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fe27-105">설명</span><span class="sxs-lookup"><span data-stu-id="3fe27-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe27-106">**Set-AzApplicationGatewaySslCertificate** cmdlet은 애플리케이션 게이트웨이에 대한 SSL 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="3fe27-107">예제</span><span class="sxs-lookup"><span data-stu-id="3fe27-107">EXAMPLES</span></span>

### <span data-ttu-id="3fe27-108">예제 1: Application Gateway에서 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="3fe27-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="3fe27-109">ApplicationGateway01이라는 애플리케이션 게이트웨이에 대한 기존 SSL 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="3fe27-110">예제 2: Application Gateway에서 KeyVault Secret(version-less secretId)을 사용하여 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="3fe27-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="3fe27-111">비밀을 다운로드하고 다음을 사용하여 기존 SSL 인증서를 `Set-AzApplicationGatewaySslCertificate` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="3fe27-112">예제 3: Application Gateway에서 KeyVault 비밀을 사용하여 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="3fe27-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="3fe27-113">비밀을 다운로드하고 다음을 사용하여 기존 SSL 인증서를 `Set-AzApplicationGatewaySslCertificate` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="3fe27-114">참고: Application Gateway가 인증서를 KeyVault와 동기화해야 하는 경우 버전이 적은 secretId를 제공하십시오.</span><span class="sxs-lookup"><span data-stu-id="3fe27-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="3fe27-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fe27-115">PARAMETERS</span></span>

### <span data-ttu-id="3fe27-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fe27-116">-ApplicationGateway</span></span>
<span data-ttu-id="3fe27-117">SSL(Secure Socket Layer) 인증서가 연결된 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="3fe27-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3fe27-118">-CertificateFile</span></span>
<span data-ttu-id="3fe27-119">SSL 인증서의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="3fe27-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe27-120">-DefaultProfile</span></span>
<span data-ttu-id="3fe27-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fe27-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="3fe27-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="3fe27-123">KeyVault 비밀의 SecretId(uri)입니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="3fe27-124">특정 버전의 비밀을 사용해야 하는 경우 이 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="3fe27-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3fe27-125">-Name</span></span>
<span data-ttu-id="3fe27-126">SSL 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="3fe27-127">-Password</span><span class="sxs-lookup"><span data-stu-id="3fe27-127">-Password</span></span>
<span data-ttu-id="3fe27-128">SSL 인증서의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="3fe27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe27-129">CommonParameters</span></span>
<span data-ttu-id="3fe27-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3fe27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe27-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3fe27-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe27-132">입력</span><span class="sxs-lookup"><span data-stu-id="3fe27-132">INPUTS</span></span>

### <span data-ttu-id="3fe27-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fe27-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3fe27-134">출력</span><span class="sxs-lookup"><span data-stu-id="3fe27-134">OUTPUTS</span></span>

### <span data-ttu-id="3fe27-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fe27-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3fe27-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3fe27-136">NOTES</span></span>

## <span data-ttu-id="3fe27-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fe27-137">RELATED LINKS</span></span>

[<span data-ttu-id="3fe27-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fe27-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3fe27-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fe27-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3fe27-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fe27-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3fe27-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fe27-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


