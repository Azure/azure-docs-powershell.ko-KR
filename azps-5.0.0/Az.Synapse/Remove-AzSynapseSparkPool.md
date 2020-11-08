---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217139"
---
# <span data-ttu-id="feda0-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="feda0-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="feda0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feda0-102">SYNOPSIS</span></span>
<span data-ttu-id="feda0-103">Synapse Analytics Spark 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="feda0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="feda0-104">SYNTAX</span></span>

### <span data-ttu-id="feda0-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="feda0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feda0-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="feda0-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feda0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="feda0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feda0-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="feda0-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feda0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="feda0-109">DESCRIPTION</span></span>
<span data-ttu-id="feda0-110">**AzSynapseSparkPool** Cmdlet은 Azure Synapse Analytics Spark 풀을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="feda0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="feda0-111">EXAMPLES</span></span>

### <span data-ttu-id="feda0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="feda0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="feda0-113">이 명령은 Azure Synapse Analytics Spark 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="feda0-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="feda0-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="feda0-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="feda0-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="feda0-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="feda0-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="feda0-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="feda0-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="feda0-119">이 명령은 리소스 ID를 사용 하 여 Azure Synapse Analytics Spark 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="feda0-120">변수</span><span class="sxs-lookup"><span data-stu-id="feda0-120">PARAMETERS</span></span>

### <span data-ttu-id="feda0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="feda0-121">-AsJob</span></span>
<span data-ttu-id="feda0-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="feda0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="feda0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feda0-123">-DefaultProfile</span></span>
<span data-ttu-id="feda0-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feda0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feda0-125">-InputObject</span></span>
<span data-ttu-id="feda0-126">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-126">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-127">-이름</span><span class="sxs-lookup"><span data-stu-id="feda0-127">-Name</span></span>
<span data-ttu-id="feda0-128">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-128">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="feda0-129">-PassThru</span></span>
<span data-ttu-id="feda0-130">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="feda0-131">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="feda0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feda0-132">-ResourceGroupName</span></span>
<span data-ttu-id="feda0-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="feda0-134">-ResourceId</span></span>
<span data-ttu-id="feda0-135">Synapse Spark 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-135">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="feda0-136">-WorkspaceName</span></span>
<span data-ttu-id="feda0-137">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="feda0-138">-WorkspaceObject</span></span>
<span data-ttu-id="feda0-139">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feda0-140">-확인</span><span class="sxs-lookup"><span data-stu-id="feda0-140">-Confirm</span></span>
<span data-ttu-id="feda0-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feda0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feda0-142">-WhatIf</span></span>
<span data-ttu-id="feda0-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feda0-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feda0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feda0-145">CommonParameters</span></span>
<span data-ttu-id="feda0-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="feda0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feda0-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="feda0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feda0-148">입력</span><span class="sxs-lookup"><span data-stu-id="feda0-148">INPUTS</span></span>

### <span data-ttu-id="feda0-149">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="feda0-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="feda0-150">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="feda0-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="feda0-151">출력</span><span class="sxs-lookup"><span data-stu-id="feda0-151">OUTPUTS</span></span>

### <span data-ttu-id="feda0-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="feda0-152">System.Boolean</span></span>

## <span data-ttu-id="feda0-153">상속자</span><span class="sxs-lookup"><span data-stu-id="feda0-153">NOTES</span></span>

## <span data-ttu-id="feda0-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="feda0-154">RELATED LINKS</span></span>
