---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: a60bcb20610449b9f76ff3e62684da43a2a792c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959979"
---
# <span data-ttu-id="10aa3-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="10aa3-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="10aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="10aa3-103">Synapse Analytics 데이터베이스를 SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="10aa3-104">구문</span><span class="sxs-lookup"><span data-stu-id="10aa3-104">SYNTAX</span></span>

### <span data-ttu-id="10aa3-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="10aa3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10aa3-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10aa3-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10aa3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10aa3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10aa3-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10aa3-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10aa3-109">설명</span><span class="sxs-lookup"><span data-stu-id="10aa3-109">DESCRIPTION</span></span>
<span data-ttu-id="10aa3-110">**Remove-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="10aa3-111">예제</span><span class="sxs-lookup"><span data-stu-id="10aa3-111">EXAMPLES</span></span>

### <span data-ttu-id="10aa3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="10aa3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="10aa3-113">이 명령은 Azure Synapse Analytics SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="10aa3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="10aa3-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="10aa3-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="10aa3-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="10aa3-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="10aa3-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="10aa3-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="10aa3-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="10aa3-119">이 명령은 지정된 리소스 ID로 Azure Synapse Analytics SQL 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="10aa3-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="10aa3-120">PARAMETERS</span></span>

### <span data-ttu-id="10aa3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10aa3-121">-AsJob</span></span>
<span data-ttu-id="10aa3-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="10aa3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10aa3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10aa3-123">-DefaultProfile</span></span>
<span data-ttu-id="10aa3-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10aa3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="10aa3-125">-Force</span></span>
<span data-ttu-id="10aa3-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="10aa3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10aa3-127">-InputObject</span></span>
<span data-ttu-id="10aa3-128">SQL 데이터베이스 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-128">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10aa3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="10aa3-129">-Name</span></span>
<span data-ttu-id="10aa3-130">Synapse 데이터베이스의 SQL.</span><span class="sxs-lookup"><span data-stu-id="10aa3-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="10aa3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10aa3-131">-PassThru</span></span>
<span data-ttu-id="10aa3-132">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="10aa3-133">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="10aa3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10aa3-134">-ResourceGroupName</span></span>
<span data-ttu-id="10aa3-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-135">Resource group name.</span></span>

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

### <span data-ttu-id="10aa3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10aa3-136">-ResourceId</span></span>
<span data-ttu-id="10aa3-137">데이터베이스의 Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="10aa3-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10aa3-138">-WorkspaceName</span></span>
<span data-ttu-id="10aa3-139">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="10aa3-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="10aa3-140">-WorkspaceObject</span></span>
<span data-ttu-id="10aa3-141">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="10aa3-142">-확인</span><span class="sxs-lookup"><span data-stu-id="10aa3-142">-Confirm</span></span>
<span data-ttu-id="10aa3-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10aa3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10aa3-144">-WhatIf</span></span>
<span data-ttu-id="10aa3-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10aa3-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10aa3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10aa3-147">CommonParameters</span></span>
<span data-ttu-id="10aa3-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10aa3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10aa3-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10aa3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10aa3-150">입력</span><span class="sxs-lookup"><span data-stu-id="10aa3-150">INPUTS</span></span>

### <span data-ttu-id="10aa3-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="10aa3-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="10aa3-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="10aa3-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="10aa3-153">System.String</span><span class="sxs-lookup"><span data-stu-id="10aa3-153">System.String</span></span>

## <span data-ttu-id="10aa3-154">출력</span><span class="sxs-lookup"><span data-stu-id="10aa3-154">OUTPUTS</span></span>

### <span data-ttu-id="10aa3-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10aa3-155">System.Boolean</span></span>

## <span data-ttu-id="10aa3-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10aa3-156">NOTES</span></span>

## <span data-ttu-id="10aa3-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10aa3-157">RELATED LINKS</span></span>
