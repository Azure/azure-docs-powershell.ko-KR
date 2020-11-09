---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 1dfd9e0aa2bc6b7c5d52ccfed756f2a96a3f307c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307880"
---
# <span data-ttu-id="c2d5c-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c2d5c-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="c2d5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d5c-103">지정 된 응용 프로그램 및 클러스터 아래에서 서비스 패브릭 서비스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="c2d5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2d5c-104">SYNTAX</span></span>

### <span data-ttu-id="c2d5c-105">ByResourceGroupAndCluster (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2d5c-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d5c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c2d5c-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d5c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d5c-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2d5c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2d5c-108">DESCRIPTION</span></span>
<span data-ttu-id="c2d5c-109">이 cmdlet은 지정 된 응용 프로그램 및 클러스터에서 서비스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="c2d5c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2d5c-110">EXAMPLES</span></span>

### <span data-ttu-id="c2d5c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2d5c-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="c2d5c-112">이 예제에서는 "testApp ~ testService" 서비스에 대 한 서비스 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="c2d5c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c2d5c-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="c2d5c-114">이 예제에서는 "testApp" 응용 프로그램 아래에 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="c2d5c-115">변수</span><span class="sxs-lookup"><span data-stu-id="c2d5c-115">PARAMETERS</span></span>

### <span data-ttu-id="c2d5c-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c2d5c-116">-ApplicationName</span></span>
<span data-ttu-id="c2d5c-117">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="c2d5c-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c2d5c-118">-ClusterName</span></span>
<span data-ttu-id="c2d5c-119">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c2d5c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d5c-120">-DefaultProfile</span></span>
<span data-ttu-id="c2d5c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d5c-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c2d5c-122">-Name</span></span>
<span data-ttu-id="c2d5c-123">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="c2d5c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d5c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2d5c-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c2d5c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d5c-126">-ResourceId</span></span>
<span data-ttu-id="c2d5c-127">서비스 팔에 대 한 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="c2d5c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d5c-128">CommonParameters</span></span>
<span data-ttu-id="c2d5c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d5c-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2d5c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d5c-131">입력</span><span class="sxs-lookup"><span data-stu-id="c2d5c-131">INPUTS</span></span>

### <span data-ttu-id="c2d5c-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2d5c-132">System.String</span></span>

## <span data-ttu-id="c2d5c-133">출력</span><span class="sxs-lookup"><span data-stu-id="c2d5c-133">OUTPUTS</span></span>

### <span data-ttu-id="c2d5c-134">ServiceFabric. a i m. PSService</span><span class="sxs-lookup"><span data-stu-id="c2d5c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="c2d5c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c2d5c-135">NOTES</span></span>

## <span data-ttu-id="c2d5c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2d5c-136">RELATED LINKS</span></span>
