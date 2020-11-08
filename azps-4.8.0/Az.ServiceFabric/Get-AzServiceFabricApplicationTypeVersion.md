---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: ea86fb4a110d355a848b9fe58969d30ccb96e2da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048738"
---
# <span data-ttu-id="29529-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="29529-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="29529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29529-102">SYNOPSIS</span></span>
<span data-ttu-id="29529-103">서비스 패브릭 응용 프로그램 유형 버전 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29529-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="29529-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29529-104">SYNTAX</span></span>

### <span data-ttu-id="29529-105">ByResourceGroupAndCluster (기본값)</span><span class="sxs-lookup"><span data-stu-id="29529-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29529-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="29529-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29529-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="29529-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29529-108">설명은</span><span class="sxs-lookup"><span data-stu-id="29529-108">DESCRIPTION</span></span>
<span data-ttu-id="29529-109">이 cmdlet을 사용 하 여 지정 된 리소스 그룹 및 클러스터의 응용 프로그램 유형 버전 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29529-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="29529-110">예제의</span><span class="sxs-lookup"><span data-stu-id="29529-110">EXAMPLES</span></span>

### <span data-ttu-id="29529-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="29529-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="29529-112">이 예제에서는 "v1" 버전을 사용 하는 응용 프로그램 유형 "testAppType"를 가져오고,이 리소스를 찾을 수 없는 경우 예외를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="29529-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="29529-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="29529-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="29529-114">이 예제에서는 지정 된 클러스터 및 형식에 정의 된 응용 프로그램 유형 버전의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29529-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="29529-115">변수</span><span class="sxs-lookup"><span data-stu-id="29529-115">PARAMETERS</span></span>

### <span data-ttu-id="29529-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="29529-116">-ClusterName</span></span>
<span data-ttu-id="29529-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29529-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="29529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29529-118">-DefaultProfile</span></span>
<span data-ttu-id="29529-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29529-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29529-120">-이름</span><span class="sxs-lookup"><span data-stu-id="29529-120">-Name</span></span>
<span data-ttu-id="29529-121">응용 프로그램 종류의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29529-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="29529-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29529-122">-ResourceGroupName</span></span>
<span data-ttu-id="29529-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29529-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="29529-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29529-124">-ResourceId</span></span>
<span data-ttu-id="29529-125">응용 프로그램 유형 버전의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="29529-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="29529-126">-버전</span><span class="sxs-lookup"><span data-stu-id="29529-126">-Version</span></span>
<span data-ttu-id="29529-127">응용 프로그램 종류의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29529-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="29529-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29529-128">CommonParameters</span></span>
<span data-ttu-id="29529-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29529-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29529-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29529-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29529-131">입력</span><span class="sxs-lookup"><span data-stu-id="29529-131">INPUTS</span></span>

### <span data-ttu-id="29529-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="29529-132">System.String</span></span>

## <span data-ttu-id="29529-133">출력</span><span class="sxs-lookup"><span data-stu-id="29529-133">OUTPUTS</span></span>

### <span data-ttu-id="29529-134">ServiceFabric. m i m a.</span><span class="sxs-lookup"><span data-stu-id="29529-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="29529-135">상속자</span><span class="sxs-lookup"><span data-stu-id="29529-135">NOTES</span></span>

## <span data-ttu-id="29529-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29529-136">RELATED LINKS</span></span>
