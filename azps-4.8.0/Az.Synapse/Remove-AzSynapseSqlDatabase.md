---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056847"
---
# <span data-ttu-id="390d1-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="390d1-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="390d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="390d1-102">SYNOPSIS</span></span>
<span data-ttu-id="390d1-103">Synapse Analytics SQL 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="390d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="390d1-104">SYNTAX</span></span>

### <span data-ttu-id="390d1-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="390d1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="390d1-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="390d1-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="390d1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="390d1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="390d1-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="390d1-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="390d1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="390d1-109">DESCRIPTION</span></span>
<span data-ttu-id="390d1-110">**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 데이터베이스를 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="390d1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="390d1-111">EXAMPLES</span></span>

### <span data-ttu-id="390d1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="390d1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="390d1-113">이 명령은 Azure Synapse Analytics SQL 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="390d1-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="390d1-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="390d1-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="390d1-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="390d1-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="390d1-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="390d1-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="390d1-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="390d1-119">이 명령은 지정 된 리소스 ID를 사용 하 여 Azure Synapse Analytics SQL 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="390d1-120">변수</span><span class="sxs-lookup"><span data-stu-id="390d1-120">PARAMETERS</span></span>

### <span data-ttu-id="390d1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="390d1-121">-AsJob</span></span>
<span data-ttu-id="390d1-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="390d1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="390d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="390d1-123">-DefaultProfile</span></span>
<span data-ttu-id="390d1-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="390d1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="390d1-125">-InputObject</span></span>
<span data-ttu-id="390d1-126">일반적으로 파이프라인을 통해 전달 되는 SQL Database 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-126">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="390d1-127">-이름</span><span class="sxs-lookup"><span data-stu-id="390d1-127">-Name</span></span>
<span data-ttu-id="390d1-128">Synapse SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-128">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="390d1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="390d1-129">-PassThru</span></span>
<span data-ttu-id="390d1-130">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="390d1-131">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="390d1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="390d1-132">-ResourceGroupName</span></span>
<span data-ttu-id="390d1-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-133">Resource group name.</span></span>

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

### <span data-ttu-id="390d1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="390d1-134">-ResourceId</span></span>
<span data-ttu-id="390d1-135">Synapse SQL 데이터베이스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-135">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="390d1-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="390d1-136">-WorkspaceName</span></span>
<span data-ttu-id="390d1-137">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="390d1-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="390d1-138">-WorkspaceObject</span></span>
<span data-ttu-id="390d1-139">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="390d1-140">-확인</span><span class="sxs-lookup"><span data-stu-id="390d1-140">-Confirm</span></span>
<span data-ttu-id="390d1-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="390d1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="390d1-142">-WhatIf</span></span>
<span data-ttu-id="390d1-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="390d1-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="390d1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="390d1-145">CommonParameters</span></span>
<span data-ttu-id="390d1-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="390d1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="390d1-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="390d1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="390d1-148">입력</span><span class="sxs-lookup"><span data-stu-id="390d1-148">INPUTS</span></span>

### <span data-ttu-id="390d1-149">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="390d1-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="390d1-150">Synapse. PSSynapseSqlDatabase/.</span><span class="sxs-lookup"><span data-stu-id="390d1-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="390d1-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="390d1-151">System.String</span></span>

## <span data-ttu-id="390d1-152">출력</span><span class="sxs-lookup"><span data-stu-id="390d1-152">OUTPUTS</span></span>

### <span data-ttu-id="390d1-153">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="390d1-153">System.Boolean</span></span>

## <span data-ttu-id="390d1-154">상속자</span><span class="sxs-lookup"><span data-stu-id="390d1-154">NOTES</span></span>

## <span data-ttu-id="390d1-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="390d1-155">RELATED LINKS</span></span>
