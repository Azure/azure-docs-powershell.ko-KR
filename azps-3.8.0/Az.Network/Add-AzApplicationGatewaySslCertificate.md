---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1d4014803f32fdb5e63fe375f2ea175d6f8e5460
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043783"
---
# <span data-ttu-id="cf6c6-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cf6c6-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cf6c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6c6-103">응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="cf6c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf6c6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf6c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cf6c6-105">DESCRIPTION</span></span>
<span data-ttu-id="cf6c6-106">**Add-AzApplicationGatewaySslCertificate** cmdlet은 응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="cf6c6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cf6c6-107">EXAMPLES</span></span>

### <span data-ttu-id="cf6c6-108">예제 1: 응용 프로그램 게이트웨이에 pfx를 사용 하 여 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="cf6c6-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음 Cert01 라는 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="cf6c6-110">예제 2: KeyVault 비밀 (버전-less secretId)을 사용 하 여 응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="cf6c6-111">비밀 정보를 가져오고이를 참조 `Add-AzApplicationGatewaySslCertificate` 하 여 이름을 사용 하는 응용 프로그램 게이트웨이에 추가 합니다 `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="cf6c6-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="cf6c6-112">참고: 여기에 버전 덜 secretId 제공 됨에 따라 Application Gateway는 KeyVault를 사용 하 여 인증서를 규칙적인 간격으로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="cf6c6-113">예제 3: KeyVault Secret (버전 secretId)를 사용 하 여 응용 프로그램 게이트웨이에 SSL 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="cf6c6-114">비밀 정보를 가져오고이를 참조 `Add-AzApplicationGatewaySslCertificate` 하 여 이름을 사용 하는 응용 프로그램 게이트웨이에 추가 합니다 `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="cf6c6-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="cf6c6-115">참고: Application Gateway가 KeyVault와 인증서를 동기화 해야 하는 경우에는 버전을 더 적게 secretId을 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="cf6c6-116">변수</span><span class="sxs-lookup"><span data-stu-id="cf6c6-116">PARAMETERS</span></span>

### <span data-ttu-id="cf6c6-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf6c6-117">-ApplicationGateway</span></span>
<span data-ttu-id="cf6c6-118">이 cmdlet이 SSL 인증서를 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="cf6c6-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cf6c6-119">-CertificateFile</span></span>
<span data-ttu-id="cf6c6-120">이 cmdlet에 추가 되는 SSL 인증서의 .pfx 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cf6c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6c6-121">-DefaultProfile</span></span>
<span data-ttu-id="cf6c6-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf6c6-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="cf6c6-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="cf6c6-124">KeyVault 비밀에 대 한 SecretId (uri)입니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="cf6c6-125">특정 버전의 비밀을 사용 해야 하는 경우이 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="cf6c6-126">-이름</span><span class="sxs-lookup"><span data-stu-id="cf6c6-126">-Name</span></span>
<span data-ttu-id="cf6c6-127">이 cmdlet에 추가 되는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cf6c6-128">-암호</span><span class="sxs-lookup"><span data-stu-id="cf6c6-128">-Password</span></span>
<span data-ttu-id="cf6c6-129">이 cmdlet이 추가 하는 SSL 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cf6c6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6c6-130">CommonParameters</span></span>
<span data-ttu-id="cf6c6-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6c6-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf6c6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6c6-133">입력</span><span class="sxs-lookup"><span data-stu-id="cf6c6-133">INPUTS</span></span>

### <span data-ttu-id="cf6c6-134">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf6c6-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cf6c6-135">출력</span><span class="sxs-lookup"><span data-stu-id="cf6c6-135">OUTPUTS</span></span>

### <span data-ttu-id="cf6c6-136">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf6c6-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cf6c6-137">상속자</span><span class="sxs-lookup"><span data-stu-id="cf6c6-137">NOTES</span></span>

## <span data-ttu-id="cf6c6-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf6c6-138">RELATED LINKS</span></span>

[<span data-ttu-id="cf6c6-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cf6c6-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cf6c6-140">새로운 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cf6c6-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cf6c6-141">제거-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cf6c6-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cf6c6-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cf6c6-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


