---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 43b4fae77aa0bf6ed76280ce633d3e1c3397e502
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386338"
---
# <span data-ttu-id="0635f-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0635f-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0635f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0635f-102">SYNOPSIS</span></span>
<span data-ttu-id="0635f-103">키 자격 증명 모음에서 인증서 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="0635f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0635f-104">SYNTAX</span></span>

### <span data-ttu-id="0635f-105">기본값</span><span class="sxs-lookup"><span data-stu-id="0635f-105">Default</span></span>
```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0635f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0635f-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0635f-107">설명</span><span class="sxs-lookup"><span data-stu-id="0635f-107">DESCRIPTION</span></span>
<span data-ttu-id="0635f-108">**Remove-AzKeyVaultCertificateOperation** cmdlet은 키 자격 증명 모음에서 인증서 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-108">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="0635f-109">예제</span><span class="sxs-lookup"><span data-stu-id="0635f-109">EXAMPLES</span></span>

### <span data-ttu-id="0635f-110">예제 1: 인증서 작업 제거</span><span class="sxs-lookup"><span data-stu-id="0635f-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

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

<span data-ttu-id="0635f-111">이 명령은 확인 메시지를 표시하지 않고 ContosoKV01 키 자격 증명 모음에서 TestCert01이라는 인증서 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="0635f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0635f-112">PARAMETERS</span></span>

### <span data-ttu-id="0635f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0635f-113">-DefaultProfile</span></span>
<span data-ttu-id="0635f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0635f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0635f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0635f-115">-Force</span></span>
<span data-ttu-id="0635f-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0635f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0635f-117">-InputObject</span></span>
<span data-ttu-id="0635f-118">작업 개체</span><span class="sxs-lookup"><span data-stu-id="0635f-118">Operation object</span></span>

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

### <span data-ttu-id="0635f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0635f-119">-Name</span></span>
<span data-ttu-id="0635f-120">인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="0635f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0635f-121">-PassThru</span></span>
<span data-ttu-id="0635f-122">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0635f-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0635f-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0635f-124">-VaultName</span></span>
<span data-ttu-id="0635f-125">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="0635f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0635f-126">-Confirm</span></span>
<span data-ttu-id="0635f-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0635f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0635f-128">-WhatIf</span></span>
<span data-ttu-id="0635f-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0635f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0635f-130">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0635f-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0635f-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0635f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0635f-132">CommonParameters</span></span>
<span data-ttu-id="0635f-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0635f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0635f-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0635f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0635f-135">입력</span><span class="sxs-lookup"><span data-stu-id="0635f-135">INPUTS</span></span>

### <span data-ttu-id="0635f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0635f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0635f-137">출력</span><span class="sxs-lookup"><span data-stu-id="0635f-137">OUTPUTS</span></span>

### <span data-ttu-id="0635f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0635f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="0635f-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0635f-139">NOTES</span></span>

## <span data-ttu-id="0635f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0635f-140">RELATED LINKS</span></span>

[<span data-ttu-id="0635f-141">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0635f-141">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="0635f-142">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="0635f-142">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

