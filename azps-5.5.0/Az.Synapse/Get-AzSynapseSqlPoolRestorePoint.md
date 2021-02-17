---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207640"
---
# <span data-ttu-id="06d55-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="06d55-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="06d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d55-102">SYNOPSIS</span></span>
<span data-ttu-id="06d55-103">Synapse Analytics 풀을 복원할 수 있는 SQL 복원 지점을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="06d55-104">구문</span><span class="sxs-lookup"><span data-stu-id="06d55-104">SYNTAX</span></span>

### <span data-ttu-id="06d55-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="06d55-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d55-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06d55-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d55-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06d55-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06d55-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06d55-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06d55-109">설명</span><span class="sxs-lookup"><span data-stu-id="06d55-109">DESCRIPTION</span></span>
<span data-ttu-id="06d55-110">**Get-AzSynapseSqlPoolRestorePoint** cmdlet은 Azure Synapse Analytics SQL 복원할 수 있는 고유한 복원 지점을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="06d55-111">예제</span><span class="sxs-lookup"><span data-stu-id="06d55-111">EXAMPLES</span></span>

### <span data-ttu-id="06d55-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="06d55-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="06d55-113">이 명령은 ContosoSqlPool이라는 Azure Synapse Analytics SQL 사용 가능한 모든 복원 지점을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="06d55-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06d55-114">PARAMETERS</span></span>

### <span data-ttu-id="06d55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d55-115">-DefaultProfile</span></span>
<span data-ttu-id="06d55-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d55-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d55-117">-InputObject</span></span>
<span data-ttu-id="06d55-118">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06d55-119">-Name</span><span class="sxs-lookup"><span data-stu-id="06d55-119">-Name</span></span>
<span data-ttu-id="06d55-120">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d55-121">-ResourceGroupName</span></span>
<span data-ttu-id="06d55-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d55-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06d55-123">-ResourceId</span></span>
<span data-ttu-id="06d55-124">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d55-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06d55-125">-WorkspaceName</span></span>
<span data-ttu-id="06d55-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d55-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06d55-127">-WorkspaceObject</span></span>
<span data-ttu-id="06d55-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06d55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d55-129">CommonParameters</span></span>
<span data-ttu-id="06d55-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06d55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d55-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06d55-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d55-132">입력</span><span class="sxs-lookup"><span data-stu-id="06d55-132">INPUTS</span></span>

### <span data-ttu-id="06d55-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="06d55-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="06d55-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="06d55-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="06d55-135">출력</span><span class="sxs-lookup"><span data-stu-id="06d55-135">OUTPUTS</span></span>

### <span data-ttu-id="06d55-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="06d55-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="06d55-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06d55-137">NOTES</span></span>

## <span data-ttu-id="06d55-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06d55-138">RELATED LINKS</span></span>
