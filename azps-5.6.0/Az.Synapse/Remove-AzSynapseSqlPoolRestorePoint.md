---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971611"
---
# <span data-ttu-id="20937-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="20937-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="20937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20937-102">SYNOPSIS</span></span>
<span data-ttu-id="20937-103">Synapse Analytics SQL 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="20937-104">구문</span><span class="sxs-lookup"><span data-stu-id="20937-104">SYNTAX</span></span>

### <span data-ttu-id="20937-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="20937-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20937-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20937-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20937-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20937-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20937-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20937-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20937-109">설명</span><span class="sxs-lookup"><span data-stu-id="20937-109">DESCRIPTION</span></span>
<span data-ttu-id="20937-110">**Remove-AzSynapseSqlPoolRestorePoint** cmdlet은 Azure Synapse Analytics SQL 복원 지점을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="20937-111">예제</span><span class="sxs-lookup"><span data-stu-id="20937-111">EXAMPLES</span></span>

### <span data-ttu-id="20937-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="20937-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="20937-113">이 명령은 Azure Synapse Analytics SQL 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="20937-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="20937-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="20937-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="20937-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="20937-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="20937-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="20937-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="20937-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="20937-119">이 명령은 지정된 리소스 ID를 사용하여 Azure Synapse Analytics SQL 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="20937-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="20937-120">PARAMETERS</span></span>

### <span data-ttu-id="20937-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20937-121">-AsJob</span></span>
<span data-ttu-id="20937-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="20937-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20937-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20937-123">-DefaultProfile</span></span>
<span data-ttu-id="20937-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20937-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20937-125">-Force</span><span class="sxs-lookup"><span data-stu-id="20937-125">-Force</span></span>
<span data-ttu-id="20937-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20937-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="20937-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20937-127">-InputObject</span></span>
<span data-ttu-id="20937-128">SQL 복원 지점 만들기 시간 입력 개체입니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="20937-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20937-129">-Name</span><span class="sxs-lookup"><span data-stu-id="20937-129">-Name</span></span>
<span data-ttu-id="20937-130">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20937-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20937-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20937-131">-PassThru</span></span>
<span data-ttu-id="20937-132">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20937-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="20937-133">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="20937-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20937-134">-ResourceGroupName</span></span>
<span data-ttu-id="20937-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20937-135">Resource group name.</span></span>

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

### <span data-ttu-id="20937-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20937-136">-ResourceId</span></span>
<span data-ttu-id="20937-137">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="20937-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="20937-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="20937-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="20937-139">Synapse SQL 지점 만들기 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="20937-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20937-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="20937-140">-SqlPoolObject</span></span>
<span data-ttu-id="20937-141">일반적으로 파이프라인을 통해 전달되는 Sql Pool 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="20937-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20937-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20937-142">-WorkspaceName</span></span>
<span data-ttu-id="20937-143">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20937-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="20937-144">-확인</span><span class="sxs-lookup"><span data-stu-id="20937-144">-Confirm</span></span>
<span data-ttu-id="20937-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="20937-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20937-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20937-146">-WhatIf</span></span>
<span data-ttu-id="20937-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="20937-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20937-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20937-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20937-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20937-149">CommonParameters</span></span>
<span data-ttu-id="20937-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20937-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20937-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20937-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20937-152">입력</span><span class="sxs-lookup"><span data-stu-id="20937-152">INPUTS</span></span>

### <span data-ttu-id="20937-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="20937-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="20937-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="20937-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="20937-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="20937-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="20937-156">System.String</span><span class="sxs-lookup"><span data-stu-id="20937-156">System.String</span></span>

## <span data-ttu-id="20937-157">출력</span><span class="sxs-lookup"><span data-stu-id="20937-157">OUTPUTS</span></span>

### <span data-ttu-id="20937-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20937-158">System.Boolean</span></span>

## <span data-ttu-id="20937-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20937-159">NOTES</span></span>

## <span data-ttu-id="20937-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20937-160">RELATED LINKS</span></span>
