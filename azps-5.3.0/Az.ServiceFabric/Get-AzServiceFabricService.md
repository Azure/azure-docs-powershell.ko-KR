---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494781"
---
# <span data-ttu-id="9be39-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="9be39-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="9be39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9be39-102">SYNOPSIS</span></span>
<span data-ttu-id="9be39-103">지정된 애플리케이션 및 클러스터에서 Service Fabric 서비스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="9be39-104">배포된 ARM 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="9be39-105">구문</span><span class="sxs-lookup"><span data-stu-id="9be39-105">SYNTAX</span></span>

### <span data-ttu-id="9be39-106">ByResourceGroupAndCluster(기본값)</span><span class="sxs-lookup"><span data-stu-id="9be39-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be39-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9be39-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be39-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9be39-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9be39-109">설명</span><span class="sxs-lookup"><span data-stu-id="9be39-109">DESCRIPTION</span></span>
<span data-ttu-id="9be39-110">이 cmdlet은 지정된 애플리케이션 및 클러스터에서 서비스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="9be39-111">예제</span><span class="sxs-lookup"><span data-stu-id="9be39-111">EXAMPLES</span></span>

### <span data-ttu-id="9be39-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9be39-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="9be39-113">이 예제에서는 "testApp~testService" 서비스에 대한 서비스 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="9be39-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9be39-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="9be39-115">이 예제에서는 애플리케이션 "testApp"에서 서비스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="9be39-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9be39-116">PARAMETERS</span></span>

### <span data-ttu-id="9be39-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="9be39-117">-ApplicationName</span></span>
<span data-ttu-id="9be39-118">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-118">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be39-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9be39-119">-ClusterName</span></span>
<span data-ttu-id="9be39-120">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9be39-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be39-121">-DefaultProfile</span></span>
<span data-ttu-id="9be39-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9be39-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9be39-123">-Name</span></span>
<span data-ttu-id="9be39-124">서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-124">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be39-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9be39-125">-ResourceGroupName</span></span>
<span data-ttu-id="9be39-126">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9be39-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9be39-127">-ResourceId</span></span>
<span data-ttu-id="9be39-128">서비스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="9be39-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be39-129">CommonParameters</span></span>
<span data-ttu-id="9be39-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9be39-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be39-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9be39-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be39-132">입력</span><span class="sxs-lookup"><span data-stu-id="9be39-132">INPUTS</span></span>

### <span data-ttu-id="9be39-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9be39-133">System.String</span></span>

## <span data-ttu-id="9be39-134">출력</span><span class="sxs-lookup"><span data-stu-id="9be39-134">OUTPUTS</span></span>

### <span data-ttu-id="9be39-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="9be39-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="9be39-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9be39-136">NOTES</span></span>

## <span data-ttu-id="9be39-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9be39-137">RELATED LINKS</span></span>
