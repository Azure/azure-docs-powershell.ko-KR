---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491524"
---
# <span data-ttu-id="6876d-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6876d-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="6876d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6876d-102">SYNOPSIS</span></span>
<span data-ttu-id="6876d-103">Synapse Analytics 데이터베이스를 SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6876d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6876d-104">SYNTAX</span></span>

### <span data-ttu-id="6876d-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6876d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6876d-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6876d-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6876d-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6876d-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6876d-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6876d-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6876d-109">설명</span><span class="sxs-lookup"><span data-stu-id="6876d-109">DESCRIPTION</span></span>
<span data-ttu-id="6876d-110">**Update-AzSynapseSqlDatabase** cmdlet은 Azure Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6876d-111">예제</span><span class="sxs-lookup"><span data-stu-id="6876d-111">EXAMPLES</span></span>

### <span data-ttu-id="6876d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6876d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="6876d-113">이 명령은 Azure Synapse Analytics SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6876d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6876d-114">PARAMETERS</span></span>

### <span data-ttu-id="6876d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6876d-115">-AsJob</span></span>
<span data-ttu-id="6876d-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6876d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6876d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6876d-117">-DefaultProfile</span></span>
<span data-ttu-id="6876d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6876d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6876d-119">-InputObject</span></span>
<span data-ttu-id="6876d-120">SQL 데이터베이스 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6876d-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6876d-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="6876d-122">데이터베이스의 최대 크기를 지정합니다(Bytes).</span><span class="sxs-lookup"><span data-stu-id="6876d-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="6876d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6876d-123">-Name</span></span>
<span data-ttu-id="6876d-124">데이터베이스의 Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="6876d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6876d-125">-PassThru</span></span>
<span data-ttu-id="6876d-126">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6876d-127">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6876d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6876d-128">-ResourceGroupName</span></span>
<span data-ttu-id="6876d-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-129">Resource group name.</span></span>

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

### <span data-ttu-id="6876d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6876d-130">-ResourceId</span></span>
<span data-ttu-id="6876d-131">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="6876d-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="6876d-132">-Tag</span></span>
<span data-ttu-id="6876d-133">리소스와 연결된 태그의 문자열 사전 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="6876d-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6876d-134">-WorkspaceName</span></span>
<span data-ttu-id="6876d-135">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6876d-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6876d-136">-WorkspaceObject</span></span>
<span data-ttu-id="6876d-137">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6876d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6876d-138">-Confirm</span></span>
<span data-ttu-id="6876d-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6876d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6876d-140">-WhatIf</span></span>
<span data-ttu-id="6876d-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6876d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6876d-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6876d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6876d-143">CommonParameters</span></span>
<span data-ttu-id="6876d-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6876d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6876d-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6876d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6876d-146">입력</span><span class="sxs-lookup"><span data-stu-id="6876d-146">INPUTS</span></span>

### <span data-ttu-id="6876d-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6876d-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6876d-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6876d-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="6876d-149">출력</span><span class="sxs-lookup"><span data-stu-id="6876d-149">OUTPUTS</span></span>

### <span data-ttu-id="6876d-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6876d-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="6876d-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6876d-151">NOTES</span></span>

## <span data-ttu-id="6876d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6876d-152">RELATED LINKS</span></span>
