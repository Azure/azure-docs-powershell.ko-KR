---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047456"
---
# <span data-ttu-id="f7b53-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f7b53-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="f7b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b53-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b53-103">Synapse Analytics SQL 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f7b53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7b53-104">SYNTAX</span></span>

### <span data-ttu-id="f7b53-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f7b53-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b53-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b53-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7b53-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b53-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b53-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b53-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b53-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f7b53-109">DESCRIPTION</span></span>
<span data-ttu-id="f7b53-110">**업데이트 AzSynapseSqlDatabase** Cmdlet은 Azure SYNAPSE Analytics SQL 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f7b53-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f7b53-111">EXAMPLES</span></span>

### <span data-ttu-id="f7b53-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f7b53-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="f7b53-113">이 명령은 Azure Synapse Analytics SQL 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f7b53-114">변수</span><span class="sxs-lookup"><span data-stu-id="f7b53-114">PARAMETERS</span></span>

### <span data-ttu-id="f7b53-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7b53-115">-AsJob</span></span>
<span data-ttu-id="f7b53-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f7b53-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7b53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b53-117">-DefaultProfile</span></span>
<span data-ttu-id="f7b53-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b53-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7b53-119">-InputObject</span></span>
<span data-ttu-id="f7b53-120">일반적으로 파이프라인을 통해 전달 되는 SQL Database 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f7b53-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="f7b53-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="f7b53-122">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="f7b53-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f7b53-123">-Name</span></span>
<span data-ttu-id="f7b53-124">Synapse SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="f7b53-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7b53-125">-PassThru</span></span>
<span data-ttu-id="f7b53-126">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f7b53-127">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f7b53-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b53-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7b53-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-129">Resource group name.</span></span>

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

### <span data-ttu-id="f7b53-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7b53-130">-ResourceId</span></span>
<span data-ttu-id="f7b53-131">Synapse SQL 데이터베이스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="f7b53-132">태그</span><span class="sxs-lookup"><span data-stu-id="f7b53-132">-Tag</span></span>
<span data-ttu-id="f7b53-133">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="f7b53-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7b53-134">-WorkspaceName</span></span>
<span data-ttu-id="f7b53-135">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7b53-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f7b53-136">-WorkspaceObject</span></span>
<span data-ttu-id="f7b53-137">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f7b53-138">-확인</span><span class="sxs-lookup"><span data-stu-id="f7b53-138">-Confirm</span></span>
<span data-ttu-id="f7b53-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b53-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b53-140">-WhatIf</span></span>
<span data-ttu-id="f7b53-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b53-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b53-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b53-143">CommonParameters</span></span>
<span data-ttu-id="f7b53-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b53-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b53-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f7b53-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b53-146">입력</span><span class="sxs-lookup"><span data-stu-id="f7b53-146">INPUTS</span></span>

### <span data-ttu-id="f7b53-147">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="f7b53-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f7b53-148">Synapse. PSSynapseSqlDatabase/.</span><span class="sxs-lookup"><span data-stu-id="f7b53-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="f7b53-149">출력</span><span class="sxs-lookup"><span data-stu-id="f7b53-149">OUTPUTS</span></span>

### <span data-ttu-id="f7b53-150">Synapse. PSSynapseSqlDatabase/.</span><span class="sxs-lookup"><span data-stu-id="f7b53-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="f7b53-151">상속자</span><span class="sxs-lookup"><span data-stu-id="f7b53-151">NOTES</span></span>

## <span data-ttu-id="f7b53-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7b53-152">RELATED LINKS</span></span>
