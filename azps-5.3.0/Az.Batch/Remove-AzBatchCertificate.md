---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494095"
---
# <span data-ttu-id="b0e65-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e65-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="b0e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e65-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e65-103">계정에서 인증서를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="b0e65-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0e65-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0e65-105">설명</span><span class="sxs-lookup"><span data-stu-id="b0e65-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e65-106">**Remove-AzBatchCertificate** cmdlet은 지정된 Azure Batch 계정에서 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="b0e65-107">예제</span><span class="sxs-lookup"><span data-stu-id="b0e65-107">EXAMPLES</span></span>

### <span data-ttu-id="b0e65-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="b0e65-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="b0e65-109">이 명령은 지정된 지문이 있는 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="b0e65-110">예제 2: 모든 활성 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="b0e65-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="b0e65-111">이 명령은 Get-AzBatchCertificate cmdlet을 사용하여 활성화된 모든 인증서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="b0e65-112">이 명령은 파이프라인 연산자를 사용하여 활성 인증서를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0e65-113">해당 cmdlet은 각 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="b0e65-114">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="b0e65-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b0e65-115">따라서 명령은 확인을 요청하는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b0e65-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0e65-116">PARAMETERS</span></span>

### <span data-ttu-id="b0e65-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b0e65-117">-BatchContext</span></span>
<span data-ttu-id="b0e65-118">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b0e65-119">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b0e65-120">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b0e65-121">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b0e65-122">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e65-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e65-123">-DefaultProfile</span></span>
<span data-ttu-id="b0e65-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0e65-125">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="b0e65-125">-Thumbprint</span></span>
<span data-ttu-id="b0e65-126">이 cmdlet이 삭제하는 인증서의 지문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e65-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b0e65-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b0e65-128">지문 매개 변수를 파생하는 데 사용되는 *알고리즘을 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="b0e65-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b0e65-129">현재 유효한 값은 sha1뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-129">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e65-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0e65-130">-Confirm</span></span>
<span data-ttu-id="b0e65-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e65-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e65-132">-WhatIf</span></span>
<span data-ttu-id="b0e65-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b0e65-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e65-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e65-135">CommonParameters</span></span>
<span data-ttu-id="b0e65-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e65-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0e65-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e65-138">입력</span><span class="sxs-lookup"><span data-stu-id="b0e65-138">INPUTS</span></span>

### <span data-ttu-id="b0e65-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b0e65-139">System.String</span></span>

### <span data-ttu-id="b0e65-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b0e65-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b0e65-141">출력</span><span class="sxs-lookup"><span data-stu-id="b0e65-141">OUTPUTS</span></span>

### <span data-ttu-id="b0e65-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="b0e65-142">System.Void</span></span>

## <span data-ttu-id="b0e65-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0e65-143">NOTES</span></span>

## <span data-ttu-id="b0e65-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0e65-144">RELATED LINKS</span></span>

[<span data-ttu-id="b0e65-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e65-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="b0e65-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b0e65-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b0e65-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e65-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="b0e65-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="b0e65-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="b0e65-149">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0e65-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
