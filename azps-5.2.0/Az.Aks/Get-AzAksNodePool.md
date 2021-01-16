---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354237"
---
# <span data-ttu-id="2db88-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="2db88-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="2db88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db88-102">SYNOPSIS</span></span>
<span data-ttu-id="2db88-103">지정된 클러스터에서 메모 풀을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="2db88-104">구문</span><span class="sxs-lookup"><span data-stu-id="2db88-104">SYNTAX</span></span>

### <span data-ttu-id="2db88-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2db88-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db88-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db88-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db88-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db88-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db88-108">설명</span><span class="sxs-lookup"><span data-stu-id="2db88-108">DESCRIPTION</span></span>
<span data-ttu-id="2db88-109">지정된 클러스터에서 메모 풀을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="2db88-110">예제</span><span class="sxs-lookup"><span data-stu-id="2db88-110">EXAMPLES</span></span>

### <span data-ttu-id="2db88-111">지정된 클러스터 내의 모든 노드 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="2db88-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2db88-112">PARAMETERS</span></span>

### <span data-ttu-id="2db88-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2db88-113">-ClusterName</span></span>
<span data-ttu-id="2db88-114">관리되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="2db88-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="2db88-115">-ClusterObject</span></span>
<span data-ttu-id="2db88-116">클러스터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-116">The cluster object.</span></span>

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

### <span data-ttu-id="2db88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db88-117">-DefaultProfile</span></span>
<span data-ttu-id="2db88-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db88-119">-Id</span><span class="sxs-lookup"><span data-stu-id="2db88-119">-Id</span></span>
<span data-ttu-id="2db88-120">관리되는 Kubernetes 클러스터의 노드 풀 ID</span><span class="sxs-lookup"><span data-stu-id="2db88-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="2db88-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2db88-121">-Name</span></span>
<span data-ttu-id="2db88-122">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="2db88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db88-123">-ResourceGroupName</span></span>
<span data-ttu-id="2db88-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2db88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db88-125">CommonParameters</span></span>
<span data-ttu-id="2db88-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2db88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db88-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2db88-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db88-128">입력</span><span class="sxs-lookup"><span data-stu-id="2db88-128">INPUTS</span></span>

### <span data-ttu-id="2db88-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2db88-129">System.String</span></span>

## <span data-ttu-id="2db88-130">출력</span><span class="sxs-lookup"><span data-stu-id="2db88-130">OUTPUTS</span></span>

### <span data-ttu-id="2db88-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="2db88-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="2db88-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2db88-132">NOTES</span></span>

## <span data-ttu-id="2db88-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2db88-133">RELATED LINKS</span></span>
