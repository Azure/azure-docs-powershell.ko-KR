---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: a939ef485976a746e705de10a4706b03c63f910e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991886"
---
# <span data-ttu-id="03e46-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="03e46-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="03e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e46-102">SYNOPSIS</span></span>
<span data-ttu-id="03e46-103">Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="03e46-104">구문</span><span class="sxs-lookup"><span data-stu-id="03e46-104">SYNTAX</span></span>

### <span data-ttu-id="03e46-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="03e46-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03e46-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03e46-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03e46-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03e46-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03e46-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03e46-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e46-109">설명</span><span class="sxs-lookup"><span data-stu-id="03e46-109">DESCRIPTION</span></span>
<span data-ttu-id="03e46-110">**Update-AzSynapseSqlDatabase** cmdlet은 Azure Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="03e46-111">예제</span><span class="sxs-lookup"><span data-stu-id="03e46-111">EXAMPLES</span></span>

### <span data-ttu-id="03e46-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="03e46-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="03e46-113">이 명령은 Azure Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="03e46-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03e46-114">PARAMETERS</span></span>

### <span data-ttu-id="03e46-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03e46-115">-AsJob</span></span>
<span data-ttu-id="03e46-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03e46-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03e46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e46-117">-DefaultProfile</span></span>
<span data-ttu-id="03e46-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03e46-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03e46-119">-InputObject</span></span>
<span data-ttu-id="03e46-120">SQL 데이터베이스 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="03e46-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="03e46-122">데이터베이스의 최대 크기를 bytes로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-123">-Name</span><span class="sxs-lookup"><span data-stu-id="03e46-123">-Name</span></span>
<span data-ttu-id="03e46-124">Synapse 데이터베이스의 SQL.</span><span class="sxs-lookup"><span data-stu-id="03e46-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03e46-125">-PassThru</span></span>
<span data-ttu-id="03e46-126">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="03e46-127">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="03e46-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e46-128">-ResourceGroupName</span></span>
<span data-ttu-id="03e46-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03e46-130">-ResourceId</span></span>
<span data-ttu-id="03e46-131">데이터베이스의 Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="03e46-132">-Tag</span></span>
<span data-ttu-id="03e46-133">문자열, 리소스와 연결된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03e46-134">-WorkspaceName</span></span>
<span data-ttu-id="03e46-135">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="03e46-136">-WorkspaceObject</span></span>
<span data-ttu-id="03e46-137">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03e46-138">-확인</span><span class="sxs-lookup"><span data-stu-id="03e46-138">-Confirm</span></span>
<span data-ttu-id="03e46-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e46-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e46-140">-WhatIf</span></span>
<span data-ttu-id="03e46-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e46-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e46-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e46-143">CommonParameters</span></span>
<span data-ttu-id="03e46-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e46-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e46-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03e46-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e46-146">입력</span><span class="sxs-lookup"><span data-stu-id="03e46-146">INPUTS</span></span>

### <span data-ttu-id="03e46-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03e46-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="03e46-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="03e46-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="03e46-149">출력</span><span class="sxs-lookup"><span data-stu-id="03e46-149">OUTPUTS</span></span>

### <span data-ttu-id="03e46-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="03e46-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="03e46-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03e46-151">NOTES</span></span>

## <span data-ttu-id="03e46-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03e46-152">RELATED LINKS</span></span>
