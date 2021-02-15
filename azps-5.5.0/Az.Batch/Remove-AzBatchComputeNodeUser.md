---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197004"
---
# <span data-ttu-id="1afd6-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="1afd6-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="1afd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1afd6-102">SYNOPSIS</span></span>
<span data-ttu-id="1afd6-103">Batch 계산 노드에서 사용자 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="1afd6-104">구문</span><span class="sxs-lookup"><span data-stu-id="1afd6-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1afd6-105">설명</span><span class="sxs-lookup"><span data-stu-id="1afd6-105">DESCRIPTION</span></span>
<span data-ttu-id="1afd6-106">**Remove-AzBatchComputeNodeUser** cmdlet은 Azure Batch 계산 노드에서 사용자 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="1afd6-107">예제</span><span class="sxs-lookup"><span data-stu-id="1afd6-107">EXAMPLES</span></span>

### <span data-ttu-id="1afd6-108">예제 1: 확인 없이 계산 노드에서 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="1afd6-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="1afd6-109">이 명령은 ComputeNode01이라는 계산 노드에서 User14라는 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="1afd6-110">계산 노드는 Pool01이라는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="1afd6-111">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="1afd6-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1afd6-112">따라서 명령은 확인을 요청하는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1afd6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1afd6-113">PARAMETERS</span></span>

### <span data-ttu-id="1afd6-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1afd6-114">-BatchContext</span></span>
<span data-ttu-id="1afd6-115">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1afd6-116">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1afd6-117">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1afd6-118">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1afd6-119">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1afd6-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="1afd6-120">-ComputeNodeId</span></span>
<span data-ttu-id="1afd6-121">이 cmdlet이 사용자 계정을 삭제하는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="1afd6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afd6-122">-DefaultProfile</span></span>
<span data-ttu-id="1afd6-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1afd6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1afd6-124">-Name</span></span>
<span data-ttu-id="1afd6-125">삭제할 사용자 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="1afd6-126">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afd6-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1afd6-127">-PoolId</span></span>
<span data-ttu-id="1afd6-128">사용자 계정을 삭제할 계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="1afd6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1afd6-129">-Confirm</span></span>
<span data-ttu-id="1afd6-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afd6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1afd6-131">-WhatIf</span></span>
<span data-ttu-id="1afd6-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1afd6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1afd6-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1afd6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afd6-134">CommonParameters</span></span>
<span data-ttu-id="1afd6-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1afd6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afd6-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1afd6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afd6-137">입력</span><span class="sxs-lookup"><span data-stu-id="1afd6-137">INPUTS</span></span>

### <span data-ttu-id="1afd6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1afd6-138">System.String</span></span>

### <span data-ttu-id="1afd6-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1afd6-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1afd6-140">출력</span><span class="sxs-lookup"><span data-stu-id="1afd6-140">OUTPUTS</span></span>

### <span data-ttu-id="1afd6-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="1afd6-141">System.Void</span></span>

## <span data-ttu-id="1afd6-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1afd6-142">NOTES</span></span>

## <span data-ttu-id="1afd6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1afd6-143">RELATED LINKS</span></span>

[<span data-ttu-id="1afd6-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="1afd6-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="1afd6-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1afd6-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1afd6-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1afd6-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
