---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226011"
---
# <span data-ttu-id="59191-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59191-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="59191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59191-102">SYNOPSIS</span></span>
<span data-ttu-id="59191-103">Synapse Analytics SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59191-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="59191-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59191-104">SYNTAX</span></span>

### <span data-ttu-id="59191-105">CreateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="59191-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59191-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59191-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59191-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59191-107">DESCRIPTION</span></span>
<span data-ttu-id="59191-108">**AzSynapseSqlDatabase** Cmdlet은 Azure SYNAPSE Analytics SQL 데이터베이스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59191-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="59191-109">예제의</span><span class="sxs-lookup"><span data-stu-id="59191-109">EXAMPLES</span></span>

### <span data-ttu-id="59191-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="59191-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="59191-111">이 명령은 Azure Synapse Analytics SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59191-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="59191-112">변수</span><span class="sxs-lookup"><span data-stu-id="59191-112">PARAMETERS</span></span>

### <span data-ttu-id="59191-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59191-113">-AsJob</span></span>
<span data-ttu-id="59191-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="59191-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59191-115">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="59191-115">-Collation</span></span>
<span data-ttu-id="59191-116">데이터 정렬은 데이터를 정렬 및 비교 하는 규칙을 정의 하 고 SQL 풀을 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="59191-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="59191-117">기본 데이터 정렬은 SQL_Latin1_General_CP1_CI_AS입니다.</span><span class="sxs-lookup"><span data-stu-id="59191-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="59191-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59191-118">-DefaultProfile</span></span>
<span data-ttu-id="59191-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59191-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59191-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="59191-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="59191-121">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59191-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="59191-122">-이름</span><span class="sxs-lookup"><span data-stu-id="59191-122">-Name</span></span>
<span data-ttu-id="59191-123">Synapse SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59191-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="59191-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59191-124">-ResourceGroupName</span></span>
<span data-ttu-id="59191-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59191-125">Resource group name.</span></span>

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

### <span data-ttu-id="59191-126">태그</span><span class="sxs-lookup"><span data-stu-id="59191-126">-Tag</span></span>
<span data-ttu-id="59191-127">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="59191-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="59191-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59191-128">-WorkspaceName</span></span>
<span data-ttu-id="59191-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59191-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="59191-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="59191-130">-WorkspaceObject</span></span>
<span data-ttu-id="59191-131">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="59191-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="59191-132">-확인</span><span class="sxs-lookup"><span data-stu-id="59191-132">-Confirm</span></span>
<span data-ttu-id="59191-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59191-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59191-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59191-134">-WhatIf</span></span>
<span data-ttu-id="59191-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59191-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59191-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59191-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59191-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59191-137">CommonParameters</span></span>
<span data-ttu-id="59191-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59191-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59191-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="59191-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59191-140">입력</span><span class="sxs-lookup"><span data-stu-id="59191-140">INPUTS</span></span>

### <span data-ttu-id="59191-141">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="59191-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="59191-142">출력</span><span class="sxs-lookup"><span data-stu-id="59191-142">OUTPUTS</span></span>

### <span data-ttu-id="59191-143">Synapse. PSSynapseSqlDatabase/.</span><span class="sxs-lookup"><span data-stu-id="59191-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="59191-144">상속자</span><span class="sxs-lookup"><span data-stu-id="59191-144">NOTES</span></span>

## <span data-ttu-id="59191-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59191-145">RELATED LINKS</span></span>
