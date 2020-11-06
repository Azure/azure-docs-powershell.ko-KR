---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 9bd02d11f0d8c6f60638b506fd09c953bc861b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530955"
---
# <span data-ttu-id="e38ed-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e38ed-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e38ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e38ed-103">키 자격 증명 모음에서 인증서 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e38ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e38ed-104">SYNTAX</span></span>

### <span data-ttu-id="e38ed-105">기본값</span><span class="sxs-lookup"><span data-stu-id="e38ed-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e38ed-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e38ed-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e38ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e38ed-107">DESCRIPTION</span></span>
<span data-ttu-id="e38ed-108">**AzureKeyVaultCertificateOperation** cmdlet은 키 자격 증명 모음에서 인증서 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="e38ed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e38ed-109">EXAMPLES</span></span>

### <span data-ttu-id="e38ed-110">예제 1: 인증서 작업 제거</span><span class="sxs-lookup"><span data-stu-id="e38ed-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

Id                        : https://contosokv01.vault.azure.net/certificates/testcert01/pending
Status                    : completed
StatusDetails             :
RequestId                 : f5dfd2ae486149a594dc98e800dceaaa
Target                    : https://contosokv01.vault.azure.net/certificates/testcert01
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
                            ==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="e38ed-111">이 명령은 확인 메시지를 표시 하지 않고 ContosoKV01 키 자격 증명 모음에서 TestCert01 이라는 인증서 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="e38ed-112">변수</span><span class="sxs-lookup"><span data-stu-id="e38ed-112">PARAMETERS</span></span>

### <span data-ttu-id="e38ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38ed-113">-DefaultProfile</span></span>
<span data-ttu-id="e38ed-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e38ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e38ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e38ed-115">-Force</span></span>
<span data-ttu-id="e38ed-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e38ed-117">-InputObject</span></span>
<span data-ttu-id="e38ed-118">작업 개체</span><span class="sxs-lookup"><span data-stu-id="e38ed-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e38ed-119">-Name</span></span>
<span data-ttu-id="e38ed-120">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e38ed-121">-PassThru</span></span>
<span data-ttu-id="e38ed-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e38ed-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e38ed-124">-VaultName</span></span>
<span data-ttu-id="e38ed-125">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e38ed-126">-Confirm</span></span>
<span data-ttu-id="e38ed-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e38ed-128">-WhatIf</span></span>
<span data-ttu-id="e38ed-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38ed-130">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e38ed-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38ed-132">CommonParameters</span></span>
<span data-ttu-id="e38ed-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e38ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38ed-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38ed-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38ed-135">입력</span><span class="sxs-lookup"><span data-stu-id="e38ed-135">INPUTS</span></span>

### <span data-ttu-id="e38ed-136">Microsoft. KeyVault. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e38ed-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>
<span data-ttu-id="e38ed-137">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e38ed-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e38ed-138">출력</span><span class="sxs-lookup"><span data-stu-id="e38ed-138">OUTPUTS</span></span>

### <span data-ttu-id="e38ed-139">Microsoft. KeyVault. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e38ed-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e38ed-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e38ed-140">NOTES</span></span>

## <span data-ttu-id="e38ed-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e38ed-141">RELATED LINKS</span></span>

[<span data-ttu-id="e38ed-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e38ed-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="e38ed-143">중지-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e38ed-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

