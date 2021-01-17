---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345609"
---
# <span data-ttu-id="1598f-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="1598f-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="1598f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1598f-102">SYNOPSIS</span></span>
<span data-ttu-id="1598f-103">지정된 Batch 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="1598f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1598f-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1598f-105">설명</span><span class="sxs-lookup"><span data-stu-id="1598f-105">DESCRIPTION</span></span>
<span data-ttu-id="1598f-106">**Remove-AzBatchPool** cmdlet은 지정된 Azure Batch 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="1598f-107">Force 매개 변수를 사용하지 않는 한 확인 메시지가 *표시됩니다.*</span><span class="sxs-lookup"><span data-stu-id="1598f-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="1598f-108">예제</span><span class="sxs-lookup"><span data-stu-id="1598f-108">EXAMPLES</span></span>

### <span data-ttu-id="1598f-109">예제 1: 풀 ID로 Batch 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="1598f-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="1598f-110">이 명령은 ID MyPool을 사용하여 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="1598f-111">삭제 작업이 수행되기 전에 사용자에게 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="1598f-112">예제 2: 강제로 모든 Batch 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="1598f-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="1598f-113">이 명령은 모든 Batch 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="1598f-114">Force *매개* 변수가 있기 때문에 확인 프롬프트가 표시 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="1598f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1598f-115">PARAMETERS</span></span>

### <span data-ttu-id="1598f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1598f-116">-BatchContext</span></span>
<span data-ttu-id="1598f-117">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1598f-118">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1598f-119">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1598f-120">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1598f-121">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1598f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1598f-122">-DefaultProfile</span></span>
<span data-ttu-id="1598f-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1598f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1598f-124">-Force</span></span>
<span data-ttu-id="1598f-125">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1598f-126">-Id</span><span class="sxs-lookup"><span data-stu-id="1598f-126">-Id</span></span>
<span data-ttu-id="1598f-127">삭제할 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="1598f-128">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="1598f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1598f-129">-Confirm</span></span>
<span data-ttu-id="1598f-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1598f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1598f-131">-WhatIf</span></span>
<span data-ttu-id="1598f-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1598f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1598f-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1598f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1598f-134">CommonParameters</span></span>
<span data-ttu-id="1598f-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1598f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1598f-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1598f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1598f-137">입력</span><span class="sxs-lookup"><span data-stu-id="1598f-137">INPUTS</span></span>

### <span data-ttu-id="1598f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1598f-138">System.String</span></span>

### <span data-ttu-id="1598f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1598f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1598f-140">출력</span><span class="sxs-lookup"><span data-stu-id="1598f-140">OUTPUTS</span></span>

### <span data-ttu-id="1598f-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1598f-141">System.Void</span></span>

## <span data-ttu-id="1598f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1598f-142">NOTES</span></span>

## <span data-ttu-id="1598f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1598f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1598f-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1598f-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1598f-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="1598f-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="1598f-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="1598f-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="1598f-147">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1598f-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
