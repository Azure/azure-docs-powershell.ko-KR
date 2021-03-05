---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 4b6d508dde18544c00ac3539921e83bd235e6fef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998979"
---
# <span data-ttu-id="14492-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="14492-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="14492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14492-102">SYNOPSIS</span></span>
<span data-ttu-id="14492-103">Batch 계산 노드에서 사용자 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="14492-104">구문</span><span class="sxs-lookup"><span data-stu-id="14492-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14492-105">설명</span><span class="sxs-lookup"><span data-stu-id="14492-105">DESCRIPTION</span></span>
<span data-ttu-id="14492-106">**Remove-AzBatchComputeNodeUser** cmdlet은 Azure Batch 계산 노드에서 사용자 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="14492-107">예제</span><span class="sxs-lookup"><span data-stu-id="14492-107">EXAMPLES</span></span>

### <span data-ttu-id="14492-108">예제 1: 확인 없이 계산 노드에서 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="14492-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="14492-109">이 명령은 ComputeNode01이라는 계산 노드에서 User14라는 사용자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="14492-110">계산 노드는 Pool01이라는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14492-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="14492-111">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="14492-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="14492-112">따라서 명령을 확인하라는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14492-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="14492-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14492-113">PARAMETERS</span></span>

### <span data-ttu-id="14492-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="14492-114">-BatchContext</span></span>
<span data-ttu-id="14492-115">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14492-116">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="14492-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="14492-117">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14492-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="14492-118">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="14492-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="14492-119">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="14492-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="14492-120">-ComputeNodeId</span></span>
<span data-ttu-id="14492-121">이 cmdlet이 사용자 계정을 삭제하는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="14492-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14492-122">-DefaultProfile</span></span>
<span data-ttu-id="14492-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14492-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14492-124">-Name</span><span class="sxs-lookup"><span data-stu-id="14492-124">-Name</span></span>
<span data-ttu-id="14492-125">삭제할 사용자 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="14492-126">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="14492-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="14492-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="14492-127">-PoolId</span></span>
<span data-ttu-id="14492-128">사용자 계정을 삭제할 계산 노드가 포함된 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="14492-129">-확인</span><span class="sxs-lookup"><span data-stu-id="14492-129">-Confirm</span></span>
<span data-ttu-id="14492-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="14492-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14492-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14492-131">-WhatIf</span></span>
<span data-ttu-id="14492-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="14492-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14492-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14492-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14492-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14492-134">CommonParameters</span></span>
<span data-ttu-id="14492-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14492-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14492-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14492-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14492-137">입력</span><span class="sxs-lookup"><span data-stu-id="14492-137">INPUTS</span></span>

### <span data-ttu-id="14492-138">System.String</span><span class="sxs-lookup"><span data-stu-id="14492-138">System.String</span></span>

### <span data-ttu-id="14492-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="14492-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="14492-140">출력</span><span class="sxs-lookup"><span data-stu-id="14492-140">OUTPUTS</span></span>

### <span data-ttu-id="14492-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="14492-141">System.Void</span></span>

## <span data-ttu-id="14492-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14492-142">NOTES</span></span>

## <span data-ttu-id="14492-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14492-143">RELATED LINKS</span></span>

[<span data-ttu-id="14492-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="14492-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="14492-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="14492-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="14492-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="14492-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
