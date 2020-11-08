---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215749"
---
# <span data-ttu-id="80bce-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="80bce-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="80bce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80bce-102">SYNOPSIS</span></span>
<span data-ttu-id="80bce-103">Synapse Analytics SQL 풀을 복원할 수 있는 고유한 복원 지점을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="80bce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80bce-104">SYNTAX</span></span>

### <span data-ttu-id="80bce-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="80bce-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80bce-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bce-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80bce-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bce-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80bce-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80bce-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80bce-109">설명은</span><span class="sxs-lookup"><span data-stu-id="80bce-109">DESCRIPTION</span></span>
<span data-ttu-id="80bce-110">**AzSynapseSqlPoolRestorePoint** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 복원할 수 있는 고유한 복원 지점을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="80bce-111">예제의</span><span class="sxs-lookup"><span data-stu-id="80bce-111">EXAMPLES</span></span>

### <span data-ttu-id="80bce-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="80bce-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="80bce-113">이 명령은 ContosoSqlPool 이라는 Azure Synapse Analytics SQL 풀에 대해 사용 가능한 모든 복원 지점을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="80bce-114">변수</span><span class="sxs-lookup"><span data-stu-id="80bce-114">PARAMETERS</span></span>

### <span data-ttu-id="80bce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bce-115">-DefaultProfile</span></span>
<span data-ttu-id="80bce-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80bce-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80bce-117">-InputObject</span></span>
<span data-ttu-id="80bce-118">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="80bce-119">-이름</span><span class="sxs-lookup"><span data-stu-id="80bce-119">-Name</span></span>
<span data-ttu-id="80bce-120">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="80bce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80bce-121">-ResourceGroupName</span></span>
<span data-ttu-id="80bce-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-122">Resource group name.</span></span>

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

### <span data-ttu-id="80bce-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80bce-123">-ResourceId</span></span>
<span data-ttu-id="80bce-124">Synapse SQL 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="80bce-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="80bce-125">-WorkspaceName</span></span>
<span data-ttu-id="80bce-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="80bce-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="80bce-127">-WorkspaceObject</span></span>
<span data-ttu-id="80bce-128">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="80bce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bce-129">CommonParameters</span></span>
<span data-ttu-id="80bce-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80bce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bce-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80bce-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bce-132">입력</span><span class="sxs-lookup"><span data-stu-id="80bce-132">INPUTS</span></span>

### <span data-ttu-id="80bce-133">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="80bce-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="80bce-134">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="80bce-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="80bce-135">출력</span><span class="sxs-lookup"><span data-stu-id="80bce-135">OUTPUTS</span></span>

### <span data-ttu-id="80bce-136">Synapse. RestorePoint/.</span><span class="sxs-lookup"><span data-stu-id="80bce-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="80bce-137">상속자</span><span class="sxs-lookup"><span data-stu-id="80bce-137">NOTES</span></span>

## <span data-ttu-id="80bce-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80bce-138">RELATED LINKS</span></span>
