---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213159"
---
# <span data-ttu-id="9b3a5-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9b3a5-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9b3a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3a5-103">Synapse Analytics SQL 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9b3a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b3a5-104">SYNTAX</span></span>

### <span data-ttu-id="9b3a5-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b3a5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3a5-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b3a5-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3a5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b3a5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3a5-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b3a5-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b3a5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9b3a5-109">DESCRIPTION</span></span>
<span data-ttu-id="9b3a5-110">**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9b3a5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9b3a5-111">EXAMPLES</span></span>

### <span data-ttu-id="9b3a5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b3a5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="9b3a5-113">이 명령은 Azure Synapse Analytics SQL 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="9b3a5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9b3a5-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="9b3a5-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9b3a5-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="9b3a5-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="9b3a5-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9b3a5-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="9b3a5-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="9b3a5-119">이 명령은 지정 된 리소스 ID를 사용 하 여 Azure Synapse Analytics SQL 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="9b3a5-120">변수</span><span class="sxs-lookup"><span data-stu-id="9b3a5-120">PARAMETERS</span></span>

### <span data-ttu-id="9b3a5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b3a5-121">-AsJob</span></span>
<span data-ttu-id="9b3a5-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9b3a5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b3a5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3a5-123">-DefaultProfile</span></span>
<span data-ttu-id="9b3a5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3a5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b3a5-125">-InputObject</span></span>
<span data-ttu-id="9b3a5-126">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b3a5-127">-이름</span><span class="sxs-lookup"><span data-stu-id="9b3a5-127">-Name</span></span>
<span data-ttu-id="9b3a5-128">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3a5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b3a5-129">-PassThru</span></span>
<span data-ttu-id="9b3a5-130">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9b3a5-131">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9b3a5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3a5-132">-ResourceGroupName</span></span>
<span data-ttu-id="9b3a5-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-133">Resource group name.</span></span>

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

### <span data-ttu-id="9b3a5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b3a5-134">-ResourceId</span></span>
<span data-ttu-id="9b3a5-135">Synapse SQL 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-135">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b3a5-136">-버전</span><span class="sxs-lookup"><span data-stu-id="9b3a5-136">-Version</span></span>
<span data-ttu-id="9b3a5-137">Synapse SQL 풀의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="9b3a5-138">예를 들면 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-138">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3a5-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b3a5-139">-WorkspaceName</span></span>
<span data-ttu-id="9b3a5-140">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-140">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9b3a5-141">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9b3a5-141">-WorkspaceObject</span></span>
<span data-ttu-id="9b3a5-142">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-142">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9b3a5-143">-확인</span><span class="sxs-lookup"><span data-stu-id="9b3a5-143">-Confirm</span></span>
<span data-ttu-id="9b3a5-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3a5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3a5-145">-WhatIf</span></span>
<span data-ttu-id="9b3a5-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b3a5-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3a5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3a5-148">CommonParameters</span></span>
<span data-ttu-id="9b3a5-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3a5-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3a5-151">입력</span><span class="sxs-lookup"><span data-stu-id="9b3a5-151">INPUTS</span></span>

### <span data-ttu-id="9b3a5-152">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9b3a5-153">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="9b3a5-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="9b3a5-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b3a5-154">System.String</span></span>

## <span data-ttu-id="9b3a5-155">출력</span><span class="sxs-lookup"><span data-stu-id="9b3a5-155">OUTPUTS</span></span>

### <span data-ttu-id="9b3a5-156">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9b3a5-156">System.Boolean</span></span>

## <span data-ttu-id="9b3a5-157">상속자</span><span class="sxs-lookup"><span data-stu-id="9b3a5-157">NOTES</span></span>

## <span data-ttu-id="9b3a5-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b3a5-158">RELATED LINKS</span></span>
