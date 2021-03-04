---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 5a67faaf48d96a93fe1bc3e6380abb4fe6d03d98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955632"
---
# <span data-ttu-id="cb1d7-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cb1d7-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="cb1d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb1d7-102">SYNOPSIS</span></span>
<span data-ttu-id="cb1d7-103">관리되는 클러스터 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="cb1d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb1d7-104">SYNTAX</span></span>

### <span data-ttu-id="cb1d7-105">BySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb1d7-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb1d7-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb1d7-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb1d7-107">ByName</span><span class="sxs-lookup"><span data-stu-id="cb1d7-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb1d7-108">설명</span><span class="sxs-lookup"><span data-stu-id="cb1d7-108">DESCRIPTION</span></span>
<span data-ttu-id="cb1d7-109">관리되는 클러스터 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="cb1d7-110">예제</span><span class="sxs-lookup"><span data-stu-id="cb1d7-110">EXAMPLES</span></span>

### <span data-ttu-id="cb1d7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb1d7-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="cb1d7-112">클러스터 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-112">Get cluster details.</span></span>

### <span data-ttu-id="cb1d7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cb1d7-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="cb1d7-114">지정된 리소스 그룹 아래에서 클러스터 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="cb1d7-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="cb1d7-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="cb1d7-116">현재 구독 아래에서 클러스터 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="cb1d7-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb1d7-117">PARAMETERS</span></span>

### <span data-ttu-id="cb1d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb1d7-118">-DefaultProfile</span></span>
<span data-ttu-id="cb1d7-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb1d7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cb1d7-120">-Name</span></span>
<span data-ttu-id="cb1d7-121">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb1d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb1d7-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb1d7-124">CommonParameters</span></span>
<span data-ttu-id="cb1d7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb1d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb1d7-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb1d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb1d7-127">입력</span><span class="sxs-lookup"><span data-stu-id="cb1d7-127">INPUTS</span></span>

### <span data-ttu-id="cb1d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cb1d7-128">System.String</span></span>

## <span data-ttu-id="cb1d7-129">출력</span><span class="sxs-lookup"><span data-stu-id="cb1d7-129">OUTPUTS</span></span>

### <span data-ttu-id="cb1d7-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cb1d7-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="cb1d7-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb1d7-131">NOTES</span></span>

## <span data-ttu-id="cb1d7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb1d7-132">RELATED LINKS</span></span>
