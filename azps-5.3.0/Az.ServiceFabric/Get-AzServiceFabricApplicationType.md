---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494791"
---
# <span data-ttu-id="30fd5-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="30fd5-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="30fd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="30fd5-103">Service Fabric 애플리케이션 유형 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="30fd5-104">배포된 ARM 유형만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="30fd5-105">구문</span><span class="sxs-lookup"><span data-stu-id="30fd5-105">SYNTAX</span></span>

### <span data-ttu-id="30fd5-106">ByResourceGroupAndCluster(기본값)</span><span class="sxs-lookup"><span data-stu-id="30fd5-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30fd5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="30fd5-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30fd5-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30fd5-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30fd5-109">설명</span><span class="sxs-lookup"><span data-stu-id="30fd5-109">DESCRIPTION</span></span>
<span data-ttu-id="30fd5-110">이 cmdlet을 사용하여 지정된 리소스 그룹 및 클러스터에서 애플리케이션 유형 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="30fd5-111">예제</span><span class="sxs-lookup"><span data-stu-id="30fd5-111">EXAMPLES</span></span>

### <span data-ttu-id="30fd5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="30fd5-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="30fd5-113">이 예제에서는 지정된 매개 변수를 사용하여 애플리케이션 유형 세부 정보를 얻습니다. 리소스를 찾지 못하면 예외가 throw됩니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="30fd5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="30fd5-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="30fd5-115">이 예제에서는 지정된 클러스터 아래에 정의된 애플리케이션 형식의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="30fd5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30fd5-116">PARAMETERS</span></span>

### <span data-ttu-id="30fd5-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30fd5-117">-ClusterName</span></span>
<span data-ttu-id="30fd5-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="30fd5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30fd5-119">-DefaultProfile</span></span>
<span data-ttu-id="30fd5-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30fd5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="30fd5-121">-Name</span></span>
<span data-ttu-id="30fd5-122">애플리케이션 형식의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="30fd5-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30fd5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30fd5-123">-ResourceGroupName</span></span>
<span data-ttu-id="30fd5-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="30fd5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30fd5-125">-ResourceId</span></span>
<span data-ttu-id="30fd5-126">애플리케이션 유형의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="30fd5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30fd5-127">CommonParameters</span></span>
<span data-ttu-id="30fd5-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30fd5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30fd5-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30fd5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30fd5-130">입력</span><span class="sxs-lookup"><span data-stu-id="30fd5-130">INPUTS</span></span>

### <span data-ttu-id="30fd5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="30fd5-131">System.String</span></span>

## <span data-ttu-id="30fd5-132">출력</span><span class="sxs-lookup"><span data-stu-id="30fd5-132">OUTPUTS</span></span>

### <span data-ttu-id="30fd5-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="30fd5-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="30fd5-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30fd5-134">NOTES</span></span>

## <span data-ttu-id="30fd5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30fd5-135">RELATED LINKS</span></span>
