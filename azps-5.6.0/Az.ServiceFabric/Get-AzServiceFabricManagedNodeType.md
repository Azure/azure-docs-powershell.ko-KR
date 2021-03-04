---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 15ba499908a4a631a22f9064b1938d3b32fdafd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955627"
---
# <span data-ttu-id="1fb51-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1fb51-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="1fb51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb51-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb51-103">관리되는 노드 형식 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="1fb51-104">구문</span><span class="sxs-lookup"><span data-stu-id="1fb51-104">SYNTAX</span></span>

### <span data-ttu-id="1fb51-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1fb51-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb51-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1fb51-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fb51-107">설명</span><span class="sxs-lookup"><span data-stu-id="1fb51-107">DESCRIPTION</span></span>
<span data-ttu-id="1fb51-108">관리되는 노드 형식 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="1fb51-109">예제</span><span class="sxs-lookup"><span data-stu-id="1fb51-109">EXAMPLES</span></span>

### <span data-ttu-id="1fb51-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1fb51-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="1fb51-111">노드 형식 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-111">Get node type details.</span></span>

### <span data-ttu-id="1fb51-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1fb51-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="1fb51-113">지정된 클러스터 아래에서 노드 형식 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="1fb51-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fb51-114">PARAMETERS</span></span>

### <span data-ttu-id="1fb51-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1fb51-115">-ClusterName</span></span>
<span data-ttu-id="1fb51-116">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb51-117">-DefaultProfile</span></span>
<span data-ttu-id="1fb51-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb51-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1fb51-119">-Name</span></span>
<span data-ttu-id="1fb51-120">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb51-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb51-121">-ResourceGroupName</span></span>
<span data-ttu-id="1fb51-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb51-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb51-123">CommonParameters</span></span>
<span data-ttu-id="1fb51-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1fb51-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb51-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fb51-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb51-126">입력</span><span class="sxs-lookup"><span data-stu-id="1fb51-126">INPUTS</span></span>

### <span data-ttu-id="1fb51-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1fb51-127">System.String</span></span>

## <span data-ttu-id="1fb51-128">출력</span><span class="sxs-lookup"><span data-stu-id="1fb51-128">OUTPUTS</span></span>

### <span data-ttu-id="1fb51-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1fb51-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="1fb51-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1fb51-130">NOTES</span></span>

## <span data-ttu-id="1fb51-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fb51-131">RELATED LINKS</span></span>
