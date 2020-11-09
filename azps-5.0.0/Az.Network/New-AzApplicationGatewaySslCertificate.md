---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: a5a1533038f8e11a30dd3fdeedd590b8186597b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310259"
---
# <span data-ttu-id="59559-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59559-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="59559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59559-102">SYNOPSIS</span></span>
<span data-ttu-id="59559-103">Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59559-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="59559-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59559-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59559-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59559-105">DESCRIPTION</span></span>
<span data-ttu-id="59559-106">**AzApplicationGatewaySslCertificate** Cmdlet은 Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59559-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="59559-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59559-107">EXAMPLES</span></span>

### <span data-ttu-id="59559-108">예제 1: Azure application gateway에 대 한 SSL 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59559-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="59559-109">이 명령은 기본 응용 프로그램 게이트웨이에 대 한 Cert01 이라는 SSL 인증서를 만들고 결과를 명명 된 변수 $Cert에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="59559-110">예제 2: KeyVault 비밀 (버전 감소 secretId)을 사용 하 여 SSL 인증서를 만들고 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="59559-111">를 사용 하 여 비밀을 가져오고 SSL 인증서를 만듭니다 `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="59559-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="59559-112">참고: 여기에 버전 덜 secretId 제공 됨에 따라 Application Gateway는 KeyVault를 사용 하 여 인증서를 규칙적인 간격으로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="59559-113">예제 3: KeyVault 비밀을 사용 하 여 SSL 인증서를 만들고 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="59559-114">를 사용 하 여 비밀을 가져오고 SSL 인증서를 만듭니다 `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="59559-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="59559-115">참고: Application Gateway가 KeyVault와 인증서를 동기화 해야 하는 경우에는 버전을 더 적게 secretId을 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="59559-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="59559-116">변수</span><span class="sxs-lookup"><span data-stu-id="59559-116">PARAMETERS</span></span>

### <span data-ttu-id="59559-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="59559-117">-CertificateFile</span></span>
<span data-ttu-id="59559-118">이 cmdlet이 만드는 SSL 인증서의 .pfx 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="59559-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59559-119">-DefaultProfile</span></span>
<span data-ttu-id="59559-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59559-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59559-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="59559-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="59559-122">KeyVault 비밀에 대 한 SecretId (uri)입니다.</span><span class="sxs-lookup"><span data-stu-id="59559-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="59559-123">특정 버전의 비밀을 사용 해야 하는 경우이 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="59559-124">-이름</span><span class="sxs-lookup"><span data-stu-id="59559-124">-Name</span></span>
<span data-ttu-id="59559-125">이 cmdlet이 만드는 SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="59559-126">-암호</span><span class="sxs-lookup"><span data-stu-id="59559-126">-Password</span></span>
<span data-ttu-id="59559-127">이 cmdlet이 만드는 SSL의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="59559-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59559-128">CommonParameters</span></span>
<span data-ttu-id="59559-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59559-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59559-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59559-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59559-131">입력</span><span class="sxs-lookup"><span data-stu-id="59559-131">INPUTS</span></span>

### <span data-ttu-id="59559-132">않아야</span><span class="sxs-lookup"><span data-stu-id="59559-132">None</span></span>

## <span data-ttu-id="59559-133">출력</span><span class="sxs-lookup"><span data-stu-id="59559-133">OUTPUTS</span></span>

### <span data-ttu-id="59559-134">PSApplicationGatewaySslCertificate에 대 한.</span><span class="sxs-lookup"><span data-stu-id="59559-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="59559-135">상속자</span><span class="sxs-lookup"><span data-stu-id="59559-135">NOTES</span></span>

## <span data-ttu-id="59559-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59559-136">RELATED LINKS</span></span>

[<span data-ttu-id="59559-137">추가-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59559-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="59559-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59559-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="59559-139">제거-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59559-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="59559-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="59559-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


