---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd51ca4bc6d238d2aac1e4dccea4ad3a89bc8d35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535871"
---
# <span data-ttu-id="e04ca-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e04ca-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="e04ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e04ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e04ca-103">키 자격 증명 모음에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e04ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e04ca-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificatePolicy] <PSKeyVaultCertificatePolicy> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e04ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e04ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e04ca-106">**AzureKeyVaultCertificate** Cmdlet은 Azure key vault의 키 보관소에서 인증서 등록 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e04ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e04ca-107">EXAMPLES</span></span>

### <span data-ttu-id="e04ca-108">예제 1: 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="e04ca-108">Example 1: Add a certificate</span></span>
```powershell
PS C:\> $Policy = New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"

Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="e04ca-109">첫 번째 명령은 New-AzureKeyVaultCertificatePolicy cmdlet을 사용 하 여 인증서 정책을 만든 다음 $Policy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>
<span data-ttu-id="e04ca-110">두 번째 명령은 **Add-AzureKeyVaultCertificate** 를 사용 하 여 프로세스를 시작 하 여 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>
<span data-ttu-id="e04ca-111">세 번째 명령은 Get-AzureKeyVaultCertificateOperation cmdlet을 사용 하 여 작업을 폴링하여 작업이 완료 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>
<span data-ttu-id="e04ca-112">마지막 명령은 Get-AzureKeyVaultCertificate cmdlet을 사용 하 여 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="e04ca-113">변수</span><span class="sxs-lookup"><span data-stu-id="e04ca-113">PARAMETERS</span></span>

### <span data-ttu-id="e04ca-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e04ca-114">-CertificatePolicy</span></span>
<span data-ttu-id="e04ca-115">**KeyVaultCertificatePolicy** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e04ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04ca-116">-DefaultProfile</span></span>
<span data-ttu-id="e04ca-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e04ca-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04ca-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e04ca-118">-Name</span></span>
<span data-ttu-id="e04ca-119">추가할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-119">Specifies the name of the certificate to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04ca-120">태그</span><span class="sxs-lookup"><span data-stu-id="e04ca-120">-Tag</span></span>
<span data-ttu-id="e04ca-121">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e04ca-122">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e04ca-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04ca-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e04ca-123">-VaultName</span></span>
<span data-ttu-id="e04ca-124">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-124">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04ca-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e04ca-125">-Confirm</span></span>
<span data-ttu-id="e04ca-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04ca-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04ca-127">-WhatIf</span></span>
<span data-ttu-id="e04ca-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e04ca-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04ca-130">CommonParameters</span></span>
<span data-ttu-id="e04ca-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e04ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04ca-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04ca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04ca-133">입력</span><span class="sxs-lookup"><span data-stu-id="e04ca-133">INPUTS</span></span>

### <span data-ttu-id="e04ca-134">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e04ca-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>
<span data-ttu-id="e04ca-135">매개 변수: CertificatePolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e04ca-135">Parameters: CertificatePolicy (ByValue)</span></span>

## <span data-ttu-id="e04ca-136">출력</span><span class="sxs-lookup"><span data-stu-id="e04ca-136">OUTPUTS</span></span>

### <span data-ttu-id="e04ca-137">Microsoft. KeyVault. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e04ca-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e04ca-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e04ca-138">NOTES</span></span>

## <span data-ttu-id="e04ca-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e04ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="e04ca-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e04ca-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e04ca-141">가져오기-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e04ca-141">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="e04ca-142">제거-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e04ca-142">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
