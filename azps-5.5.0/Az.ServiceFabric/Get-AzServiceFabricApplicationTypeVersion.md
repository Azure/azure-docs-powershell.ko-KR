---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208048"
---
# <span data-ttu-id="829ff-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="829ff-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="829ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="829ff-102">SYNOPSIS</span></span>
<span data-ttu-id="829ff-103">Service Fabric 애플리케이션 유형 버전 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="829ff-104">배포된 ARM 버전만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="829ff-105">구문</span><span class="sxs-lookup"><span data-stu-id="829ff-105">SYNTAX</span></span>

### <span data-ttu-id="829ff-106">ByResourceGroupAndCluster(기본값)</span><span class="sxs-lookup"><span data-stu-id="829ff-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="829ff-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="829ff-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="829ff-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="829ff-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="829ff-109">설명</span><span class="sxs-lookup"><span data-stu-id="829ff-109">DESCRIPTION</span></span>
<span data-ttu-id="829ff-110">이 cmdlet을 사용하여 지정된 리소스 그룹 및 클러스터에서 애플리케이션 유형 버전 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="829ff-111">예제</span><span class="sxs-lookup"><span data-stu-id="829ff-111">EXAMPLES</span></span>

### <span data-ttu-id="829ff-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="829ff-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="829ff-113">이 예제에서는 "v1" 버전이 있는 애플리케이션 형식 "testAppType"을 얻습니다. 리소스를 찾지 못하면 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="829ff-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="829ff-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="829ff-115">이 예제에서는 지정된 클러스터 및 형식 아래에 정의된 애플리케이션 유형 버전 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="829ff-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="829ff-116">PARAMETERS</span></span>

### <span data-ttu-id="829ff-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="829ff-117">-ClusterName</span></span>
<span data-ttu-id="829ff-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="829ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829ff-119">-DefaultProfile</span></span>
<span data-ttu-id="829ff-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="829ff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="829ff-121">-Name</span></span>
<span data-ttu-id="829ff-122">애플리케이션 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-122">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="829ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="829ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="829ff-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="829ff-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="829ff-125">-ResourceId</span></span>
<span data-ttu-id="829ff-126">애플리케이션 형식 버전의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="829ff-127">-Version</span><span class="sxs-lookup"><span data-stu-id="829ff-127">-Version</span></span>
<span data-ttu-id="829ff-128">애플리케이션 형식의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-128">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="829ff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829ff-129">CommonParameters</span></span>
<span data-ttu-id="829ff-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="829ff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829ff-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="829ff-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829ff-132">입력</span><span class="sxs-lookup"><span data-stu-id="829ff-132">INPUTS</span></span>

### <span data-ttu-id="829ff-133">System.String</span><span class="sxs-lookup"><span data-stu-id="829ff-133">System.String</span></span>

## <span data-ttu-id="829ff-134">출력</span><span class="sxs-lookup"><span data-stu-id="829ff-134">OUTPUTS</span></span>

### <span data-ttu-id="829ff-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="829ff-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="829ff-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="829ff-136">NOTES</span></span>

## <span data-ttu-id="829ff-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="829ff-137">RELATED LINKS</span></span>
