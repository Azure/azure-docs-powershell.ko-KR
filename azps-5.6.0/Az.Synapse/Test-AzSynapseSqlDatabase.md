---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e797cba0c05b6dbaee11d540b9efc3aca7e7efcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011259"
---
# <span data-ttu-id="4d4b4-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4d4b4-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="4d4b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4b4-103">Synapse Analytics 데이터베이스의 SQL 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="4d4b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d4b4-104">SYNTAX</span></span>

### <span data-ttu-id="4d4b4-105">TestByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4d4b4-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d4b4-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d4b4-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d4b4-107">설명</span><span class="sxs-lookup"><span data-stu-id="4d4b4-107">DESCRIPTION</span></span>
<span data-ttu-id="4d4b4-108">**Test-AzSynapseSqlDatabase** cmdlet은 Synapse Analytics 데이터베이스의 SQL 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="4d4b4-109">예제</span><span class="sxs-lookup"><span data-stu-id="4d4b4-109">EXAMPLES</span></span>

### <span data-ttu-id="4d4b4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d4b4-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="4d4b4-111">이 명령은 지정된 데이터베이스 데이터베이스의 SQL 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="4d4b4-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d4b4-112">PARAMETERS</span></span>

### <span data-ttu-id="4d4b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4b4-113">-DefaultProfile</span></span>
<span data-ttu-id="4d4b4-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d4b4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4d4b4-115">-Name</span></span>
<span data-ttu-id="4d4b4-116">Synapse 데이터베이스의 SQL.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="4d4b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d4b4-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4b4-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d4b4-119">-WorkspaceName</span></span>
<span data-ttu-id="4d4b4-120">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4b4-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4d4b4-121">-WorkspaceObject</span></span>
<span data-ttu-id="4d4b4-122">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4b4-123">CommonParameters</span></span>
<span data-ttu-id="4d4b4-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4b4-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d4b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4b4-126">입력</span><span class="sxs-lookup"><span data-stu-id="4d4b4-126">INPUTS</span></span>

### <span data-ttu-id="4d4b4-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d4b4-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4d4b4-128">출력</span><span class="sxs-lookup"><span data-stu-id="4d4b4-128">OUTPUTS</span></span>

### <span data-ttu-id="4d4b4-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d4b4-129">System.Boolean</span></span>

## <span data-ttu-id="4d4b4-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d4b4-130">NOTES</span></span>

## <span data-ttu-id="4d4b4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d4b4-131">RELATED LINKS</span></span>
