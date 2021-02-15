---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193692"
---
# <span data-ttu-id="36da4-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36da4-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="36da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36da4-102">SYNOPSIS</span></span>
<span data-ttu-id="36da4-103">Azure 애플리케이션 게이트웨이에 대한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="36da4-104">구문</span><span class="sxs-lookup"><span data-stu-id="36da4-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36da4-105">설명</span><span class="sxs-lookup"><span data-stu-id="36da4-105">DESCRIPTION</span></span>
<span data-ttu-id="36da4-106">**New-AzApplicationGatewaySslCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="36da4-107">예제</span><span class="sxs-lookup"><span data-stu-id="36da4-107">EXAMPLES</span></span>

### <span data-ttu-id="36da4-108">예제 1: Azure 애플리케이션 게이트웨이에 대한 SSL 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="36da4-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="36da4-109">이 명령은 기본 애플리케이션 게이트웨이에 대해 Cert01이라는 SSL 인증서를 만들고 결과를 Cert01이라는 이름의 변수에 $Cert.</span><span class="sxs-lookup"><span data-stu-id="36da4-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="36da4-110">예제 2: KeyVault Secret(version-less secretId)을 사용하여 SSL 인증서를 만들고 애플리케이션 게이트웨이에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="36da4-111">비밀을 사용하고 를 사용하여 SSL 인증서를 `New-AzApplicationGatewaySslCertificate` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="36da4-112">참고: 버전이 적은 secretId가 여기에 제공될 때 Application Gateway는 KeyVault와 정기적으로 인증서를 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="36da4-113">예제 3: KeyVault 비밀을 사용하여 SSL 인증서를 만들고 Application Gateway에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="36da4-114">비밀을 사용하고 를 사용하여 SSL 인증서를 `New-AzApplicationGatewaySslCertificate` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="36da4-115">참고: Application Gateway가 인증서를 KeyVault와 동기화해야 하는 경우 버전이 적은 secretId를 제공하십시오.</span><span class="sxs-lookup"><span data-stu-id="36da4-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="36da4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36da4-116">PARAMETERS</span></span>

### <span data-ttu-id="36da4-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="36da4-117">-CertificateFile</span></span>
<span data-ttu-id="36da4-118">이 cmdlet에서 만드는 SSL 인증서의 .pfx 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="36da4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36da4-119">-DefaultProfile</span></span>
<span data-ttu-id="36da4-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36da4-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="36da4-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="36da4-122">KeyVault 비밀의 SecretId(uri)입니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="36da4-123">특정 버전의 비밀을 사용해야 하는 경우 이 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="36da4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="36da4-124">-Name</span></span>
<span data-ttu-id="36da4-125">이 cmdlet에서 만드는 SSL 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="36da4-126">-Password</span><span class="sxs-lookup"><span data-stu-id="36da4-126">-Password</span></span>
<span data-ttu-id="36da4-127">이 cmdlet에서 만드는 SSL의 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="36da4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36da4-128">CommonParameters</span></span>
<span data-ttu-id="36da4-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36da4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36da4-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36da4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36da4-131">입력</span><span class="sxs-lookup"><span data-stu-id="36da4-131">INPUTS</span></span>

### <span data-ttu-id="36da4-132">없음</span><span class="sxs-lookup"><span data-stu-id="36da4-132">None</span></span>

## <span data-ttu-id="36da4-133">출력</span><span class="sxs-lookup"><span data-stu-id="36da4-133">OUTPUTS</span></span>

### <span data-ttu-id="36da4-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36da4-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="36da4-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36da4-135">NOTES</span></span>

## <span data-ttu-id="36da4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36da4-136">RELATED LINKS</span></span>

[<span data-ttu-id="36da4-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36da4-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="36da4-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36da4-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="36da4-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36da4-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="36da4-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="36da4-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


