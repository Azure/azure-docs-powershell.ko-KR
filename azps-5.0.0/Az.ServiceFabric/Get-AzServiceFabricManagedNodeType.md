---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307889"
---
# <span data-ttu-id="78edf-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="78edf-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="78edf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78edf-102">SYNOPSIS</span></span>
<span data-ttu-id="78edf-103">관리 노드 형식 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="78edf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78edf-104">SYNTAX</span></span>

### <span data-ttu-id="78edf-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="78edf-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78edf-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78edf-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78edf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78edf-107">DESCRIPTION</span></span>
<span data-ttu-id="78edf-108">관리 노드 형식 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="78edf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="78edf-109">EXAMPLES</span></span>

### <span data-ttu-id="78edf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="78edf-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="78edf-111">노드 형식 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-111">Get node type details.</span></span>

### <span data-ttu-id="78edf-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="78edf-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="78edf-113">지정 된 클러스터 아래에 있는 노드 형식 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="78edf-114">변수</span><span class="sxs-lookup"><span data-stu-id="78edf-114">PARAMETERS</span></span>

### <span data-ttu-id="78edf-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="78edf-115">-ClusterName</span></span>
<span data-ttu-id="78edf-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="78edf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78edf-117">-DefaultProfile</span></span>
<span data-ttu-id="78edf-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78edf-119">-이름</span><span class="sxs-lookup"><span data-stu-id="78edf-119">-Name</span></span>
<span data-ttu-id="78edf-120">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="78edf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78edf-121">-ResourceGroupName</span></span>
<span data-ttu-id="78edf-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="78edf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78edf-123">CommonParameters</span></span>
<span data-ttu-id="78edf-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78edf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78edf-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78edf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78edf-126">입력</span><span class="sxs-lookup"><span data-stu-id="78edf-126">INPUTS</span></span>

### <span data-ttu-id="78edf-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78edf-127">System.String</span></span>

## <span data-ttu-id="78edf-128">출력</span><span class="sxs-lookup"><span data-stu-id="78edf-128">OUTPUTS</span></span>

### <span data-ttu-id="78edf-129">ServiceFabric. a i m.</span><span class="sxs-lookup"><span data-stu-id="78edf-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="78edf-130">상속자</span><span class="sxs-lookup"><span data-stu-id="78edf-130">NOTES</span></span>

## <span data-ttu-id="78edf-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78edf-131">RELATED LINKS</span></span>
