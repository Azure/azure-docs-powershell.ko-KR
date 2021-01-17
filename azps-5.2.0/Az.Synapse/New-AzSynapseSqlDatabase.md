---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356532"
---
# <span data-ttu-id="31e67-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e67-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="31e67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e67-102">SYNOPSIS</span></span>
<span data-ttu-id="31e67-103">Synapse Analytics 데이터베이스를 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="31e67-104">구문</span><span class="sxs-lookup"><span data-stu-id="31e67-104">SYNTAX</span></span>

### <span data-ttu-id="31e67-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="31e67-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31e67-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31e67-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e67-107">설명</span><span class="sxs-lookup"><span data-stu-id="31e67-107">DESCRIPTION</span></span>
<span data-ttu-id="31e67-108">**Get-AzSynapseSqlDatabase** cmdlet은 Azure Synapse Analytics SQL 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="31e67-109">예제</span><span class="sxs-lookup"><span data-stu-id="31e67-109">EXAMPLES</span></span>

### <span data-ttu-id="31e67-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="31e67-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="31e67-111">이 명령은 Azure Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="31e67-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31e67-112">PARAMETERS</span></span>

### <span data-ttu-id="31e67-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31e67-113">-AsJob</span></span>
<span data-ttu-id="31e67-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="31e67-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31e67-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="31e67-115">-Collation</span></span>
<span data-ttu-id="31e67-116">데이터 정렬은 데이터를 정렬하고 비교하는 규칙을 정의하며 풀을 생성한 후에 변경할 SQL 없습니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="31e67-117">기본 데이터 SQL_Latin1_General_CP1_CI_AS입니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e67-118">-DefaultProfile</span></span>
<span data-ttu-id="31e67-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e67-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="31e67-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="31e67-121">데이터베이스의 최대 크기를 지정합니다(Bytes).</span><span class="sxs-lookup"><span data-stu-id="31e67-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e67-122">-Name</span><span class="sxs-lookup"><span data-stu-id="31e67-122">-Name</span></span>
<span data-ttu-id="31e67-123">데이터베이스의 Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e67-124">-ResourceGroupName</span></span>
<span data-ttu-id="31e67-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e67-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="31e67-126">-Tag</span></span>
<span data-ttu-id="31e67-127">리소스와 연결된 태그의 문자열 사전 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="31e67-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31e67-128">-WorkspaceName</span></span>
<span data-ttu-id="31e67-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e67-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="31e67-130">-WorkspaceObject</span></span>
<span data-ttu-id="31e67-131">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31e67-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31e67-132">-Confirm</span></span>
<span data-ttu-id="31e67-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e67-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e67-134">-WhatIf</span></span>
<span data-ttu-id="31e67-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="31e67-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e67-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e67-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e67-137">CommonParameters</span></span>
<span data-ttu-id="31e67-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31e67-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e67-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31e67-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e67-140">입력</span><span class="sxs-lookup"><span data-stu-id="31e67-140">INPUTS</span></span>

### <span data-ttu-id="31e67-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="31e67-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="31e67-142">출력</span><span class="sxs-lookup"><span data-stu-id="31e67-142">OUTPUTS</span></span>

### <span data-ttu-id="31e67-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31e67-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="31e67-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31e67-144">NOTES</span></span>

## <span data-ttu-id="31e67-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31e67-145">RELATED LINKS</span></span>
