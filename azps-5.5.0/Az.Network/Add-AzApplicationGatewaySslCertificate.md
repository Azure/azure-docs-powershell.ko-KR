---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207048"
---
# <span data-ttu-id="9f79e-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f79e-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9f79e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f79e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f79e-103">애플리케이션 게이트웨이에 SSL 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9f79e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f79e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f79e-105">설명</span><span class="sxs-lookup"><span data-stu-id="9f79e-105">DESCRIPTION</span></span>
<span data-ttu-id="9f79e-106">**Add-AzApplicationGatewaySslCertificate** cmdlet은 애플리케이션 게이트웨이에 SSL 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="9f79e-107">예제</span><span class="sxs-lookup"><span data-stu-id="9f79e-107">EXAMPLES</span></span>

### <span data-ttu-id="9f79e-108">예제 1: 애플리케이션 게이트웨이에 pfx를 사용하여 SSL 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="9f79e-109">이 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 얻은 다음 Cert01이라는 SSL 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="9f79e-110">예제 2: KeyVault Secret(version-less secretId)을 사용하여 애플리케이션 게이트웨이에 SSL 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9f79e-111">비밀을 얻게 하여 이름을 지정하여 Application Gateway에 추가하기 위해 해당 비밀을 `Add-AzApplicationGatewaySslCertificate` `Cert01` 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="9f79e-112">참고: 버전이 적은 secretId가 여기에 제공될 때 Application Gateway는 KeyVault와 정기적으로 인증서를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="9f79e-113">예제 3: KeyVault Secret(versioned secretId)을 사용하여 애플리케이션 게이트웨이에 SSL 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="9f79e-114">비밀을 얻게 하여 이름을 지정하여 Application Gateway에 추가하기 위해 해당 비밀을 `Add-AzApplicationGatewaySslCertificate` `Cert01` 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="9f79e-115">참고: Application Gateway가 인증서를 KeyVault와 동기화해야 하는 경우 버전이 적은 secretId를 제공하십시오.</span><span class="sxs-lookup"><span data-stu-id="9f79e-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="9f79e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f79e-116">PARAMETERS</span></span>

### <span data-ttu-id="9f79e-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f79e-117">-ApplicationGateway</span></span>
<span data-ttu-id="9f79e-118">이 cmdlet에서 SSL 인증서를 추가하는 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="9f79e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9f79e-119">-CertificateFile</span></span>
<span data-ttu-id="9f79e-120">이 cmdlet이 추가하는 SSL 인증서의 .pfx 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9f79e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f79e-121">-DefaultProfile</span></span>
<span data-ttu-id="9f79e-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f79e-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="9f79e-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="9f79e-124">KeyVault 비밀의 SecretId(uri)입니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="9f79e-125">특정 버전의 비밀을 사용해야 하는 경우 이 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="9f79e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9f79e-126">-Name</span></span>
<span data-ttu-id="9f79e-127">이 cmdlet이 추가하는 SSL 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9f79e-128">-Password</span><span class="sxs-lookup"><span data-stu-id="9f79e-128">-Password</span></span>
<span data-ttu-id="9f79e-129">이 cmdlet이 추가하는 SSL 인증서의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9f79e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f79e-130">CommonParameters</span></span>
<span data-ttu-id="9f79e-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f79e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f79e-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9f79e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f79e-133">입력</span><span class="sxs-lookup"><span data-stu-id="9f79e-133">INPUTS</span></span>

### <span data-ttu-id="9f79e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f79e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f79e-135">출력</span><span class="sxs-lookup"><span data-stu-id="9f79e-135">OUTPUTS</span></span>

### <span data-ttu-id="9f79e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f79e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f79e-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f79e-137">NOTES</span></span>

## <span data-ttu-id="9f79e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f79e-138">RELATED LINKS</span></span>

[<span data-ttu-id="9f79e-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f79e-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9f79e-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f79e-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9f79e-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f79e-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9f79e-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9f79e-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


