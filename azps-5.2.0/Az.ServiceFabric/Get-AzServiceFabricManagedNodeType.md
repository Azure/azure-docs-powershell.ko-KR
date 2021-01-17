---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347805"
---
# <span data-ttu-id="2e8ee-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2e8ee-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="2e8ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8ee-103">관리되는 노드 유형 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="2e8ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e8ee-104">SYNTAX</span></span>

### <span data-ttu-id="2e8ee-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2e8ee-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e8ee-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2e8ee-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e8ee-107">설명</span><span class="sxs-lookup"><span data-stu-id="2e8ee-107">DESCRIPTION</span></span>
<span data-ttu-id="2e8ee-108">관리되는 노드 유형 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="2e8ee-109">예제</span><span class="sxs-lookup"><span data-stu-id="2e8ee-109">EXAMPLES</span></span>

### <span data-ttu-id="2e8ee-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2e8ee-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="2e8ee-111">노드 유형 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-111">Get node type details.</span></span>

### <span data-ttu-id="2e8ee-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2e8ee-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="2e8ee-113">지정된 클러스터에서 노드 형식 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="2e8ee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e8ee-114">PARAMETERS</span></span>

### <span data-ttu-id="2e8ee-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2e8ee-115">-ClusterName</span></span>
<span data-ttu-id="2e8ee-116">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2e8ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8ee-117">-DefaultProfile</span></span>
<span data-ttu-id="2e8ee-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e8ee-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2e8ee-119">-Name</span></span>
<span data-ttu-id="2e8ee-120">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="2e8ee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e8ee-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e8ee-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2e8ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8ee-123">CommonParameters</span></span>
<span data-ttu-id="2e8ee-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8ee-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e8ee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8ee-126">입력</span><span class="sxs-lookup"><span data-stu-id="2e8ee-126">INPUTS</span></span>

### <span data-ttu-id="2e8ee-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2e8ee-127">System.String</span></span>

## <span data-ttu-id="2e8ee-128">출력</span><span class="sxs-lookup"><span data-stu-id="2e8ee-128">OUTPUTS</span></span>

### <span data-ttu-id="2e8ee-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2e8ee-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="2e8ee-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e8ee-130">NOTES</span></span>

## <span data-ttu-id="2e8ee-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e8ee-131">RELATED LINKS</span></span>
