---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 4d6fab247a56054b8c78914f5e47bc5737f8828f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966907"
---
# <span data-ttu-id="2d9ec-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="2d9ec-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="2d9ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9ec-103">지정된 클러스터에서 메모 풀을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="2d9ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="2d9ec-104">SYNTAX</span></span>

### <span data-ttu-id="2d9ec-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2d9ec-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d9ec-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d9ec-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d9ec-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d9ec-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d9ec-108">설명</span><span class="sxs-lookup"><span data-stu-id="2d9ec-108">DESCRIPTION</span></span>
<span data-ttu-id="2d9ec-109">지정된 클러스터에서 메모 풀을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="2d9ec-110">예제</span><span class="sxs-lookup"><span data-stu-id="2d9ec-110">EXAMPLES</span></span>

### <span data-ttu-id="2d9ec-111">지정된 클러스터 내의 모든 노드 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="2d9ec-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2d9ec-112">PARAMETERS</span></span>

### <span data-ttu-id="2d9ec-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2d9ec-113">-ClusterName</span></span>
<span data-ttu-id="2d9ec-114">관리되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9ec-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="2d9ec-115">-ClusterObject</span></span>
<span data-ttu-id="2d9ec-116">클러스터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9ec-117">-DefaultProfile</span></span>
<span data-ttu-id="2d9ec-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d9ec-119">-Id</span><span class="sxs-lookup"><span data-stu-id="2d9ec-119">-Id</span></span>
<span data-ttu-id="2d9ec-120">관리되는 Kubernetes 클러스터의 노드 풀 ID</span><span class="sxs-lookup"><span data-stu-id="2d9ec-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9ec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2d9ec-121">-Name</span></span>
<span data-ttu-id="2d9ec-122">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d9ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d9ec-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9ec-125">CommonParameters</span></span>
<span data-ttu-id="2d9ec-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9ec-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d9ec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9ec-128">입력</span><span class="sxs-lookup"><span data-stu-id="2d9ec-128">INPUTS</span></span>

### <span data-ttu-id="2d9ec-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2d9ec-129">System.String</span></span>

## <span data-ttu-id="2d9ec-130">출력</span><span class="sxs-lookup"><span data-stu-id="2d9ec-130">OUTPUTS</span></span>

### <span data-ttu-id="2d9ec-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="2d9ec-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="2d9ec-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2d9ec-132">NOTES</span></span>

## <span data-ttu-id="2d9ec-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d9ec-133">RELATED LINKS</span></span>
