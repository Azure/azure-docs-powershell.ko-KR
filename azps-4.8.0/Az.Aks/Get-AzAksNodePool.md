---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213413"
---
# <span data-ttu-id="64637-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="64637-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="64637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64637-102">SYNOPSIS</span></span>
<span data-ttu-id="64637-103">지정 된 클러스터에서 메모 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64637-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="64637-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64637-104">SYNTAX</span></span>

### <span data-ttu-id="64637-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="64637-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64637-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64637-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64637-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64637-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64637-108">설명은</span><span class="sxs-lookup"><span data-stu-id="64637-108">DESCRIPTION</span></span>
<span data-ttu-id="64637-109">지정 된 클러스터에서 메모 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64637-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="64637-110">예제의</span><span class="sxs-lookup"><span data-stu-id="64637-110">EXAMPLES</span></span>

### <span data-ttu-id="64637-111">지정 된 클러스터 내의 모든 노드 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="64637-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="64637-112">변수</span><span class="sxs-lookup"><span data-stu-id="64637-112">PARAMETERS</span></span>

### <span data-ttu-id="64637-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64637-113">-ClusterName</span></span>
<span data-ttu-id="64637-114">관리 되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64637-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="64637-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="64637-115">-ClusterObject</span></span>
<span data-ttu-id="64637-116">클러스터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="64637-116">The cluster object.</span></span>

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

### <span data-ttu-id="64637-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64637-117">-DefaultProfile</span></span>
<span data-ttu-id="64637-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64637-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64637-119">-Id</span><span class="sxs-lookup"><span data-stu-id="64637-119">-Id</span></span>
<span data-ttu-id="64637-120">관리 되는 Kubernetes 클러스터의 노드 풀 Id</span><span class="sxs-lookup"><span data-stu-id="64637-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="64637-121">-이름</span><span class="sxs-lookup"><span data-stu-id="64637-121">-Name</span></span>
<span data-ttu-id="64637-122">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64637-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="64637-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64637-123">-ResourceGroupName</span></span>
<span data-ttu-id="64637-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64637-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="64637-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64637-125">CommonParameters</span></span>
<span data-ttu-id="64637-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64637-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64637-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64637-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64637-128">입력</span><span class="sxs-lookup"><span data-stu-id="64637-128">INPUTS</span></span>

### <span data-ttu-id="64637-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64637-129">System.String</span></span>

## <span data-ttu-id="64637-130">출력</span><span class="sxs-lookup"><span data-stu-id="64637-130">OUTPUTS</span></span>

### <span data-ttu-id="64637-131">Aks. PSNodePool 풀</span><span class="sxs-lookup"><span data-stu-id="64637-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="64637-132">상속자</span><span class="sxs-lookup"><span data-stu-id="64637-132">NOTES</span></span>

## <span data-ttu-id="64637-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64637-133">RELATED LINKS</span></span>
