---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 346664d4714836b9965088d946262257e76747e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963616"
---
# <span data-ttu-id="17da4-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="17da4-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="17da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17da4-102">SYNOPSIS</span></span>
<span data-ttu-id="17da4-103">Service Fabric 애플리케이션 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-103">Get Service Fabric application details.</span></span> <span data-ttu-id="17da4-104">배포된 애플리케이션만 ARM 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="17da4-105">구문</span><span class="sxs-lookup"><span data-stu-id="17da4-105">SYNTAX</span></span>

### <span data-ttu-id="17da4-106">ByResourceGroupAndCluster(기본값)</span><span class="sxs-lookup"><span data-stu-id="17da4-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17da4-107">ByName</span><span class="sxs-lookup"><span data-stu-id="17da4-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17da4-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17da4-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17da4-109">설명</span><span class="sxs-lookup"><span data-stu-id="17da4-109">DESCRIPTION</span></span>
<span data-ttu-id="17da4-110">이 cmdlet은 지정된 리소스 그룹 및 클러스터에서 애플리케이션 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="17da4-111">예제</span><span class="sxs-lookup"><span data-stu-id="17da4-111">EXAMPLES</span></span>

### <span data-ttu-id="17da4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="17da4-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="17da4-113">이 예제에서는 애플리케이션 "testApp"에 대한 애플리케이션 리소스 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="17da4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="17da4-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="17da4-115">이 예제에서는 클러스터 "testCluster"에서 애플리케이션 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="17da4-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="17da4-116">PARAMETERS</span></span>

### <span data-ttu-id="17da4-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="17da4-117">-ClusterName</span></span>
<span data-ttu-id="17da4-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17da4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17da4-119">-DefaultProfile</span></span>
<span data-ttu-id="17da4-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17da4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="17da4-121">-Name</span></span>
<span data-ttu-id="17da4-122">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17da4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17da4-123">-ResourceGroupName</span></span>
<span data-ttu-id="17da4-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17da4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17da4-125">-ResourceId</span></span>
<span data-ttu-id="17da4-126">애플리케이션의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-126">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17da4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17da4-127">CommonParameters</span></span>
<span data-ttu-id="17da4-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17da4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17da4-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17da4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17da4-130">입력</span><span class="sxs-lookup"><span data-stu-id="17da4-130">INPUTS</span></span>

### <span data-ttu-id="17da4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="17da4-131">System.String</span></span>

## <span data-ttu-id="17da4-132">출력</span><span class="sxs-lookup"><span data-stu-id="17da4-132">OUTPUTS</span></span>

### <span data-ttu-id="17da4-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="17da4-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="17da4-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17da4-134">NOTES</span></span>

## <span data-ttu-id="17da4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17da4-135">RELATED LINKS</span></span>
