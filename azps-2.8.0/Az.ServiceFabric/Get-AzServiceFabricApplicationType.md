---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 78cec82383c257e325c35d0987de73f37aff253d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871538"
---
# <span data-ttu-id="0e596-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0e596-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="0e596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e596-102">SYNOPSIS</span></span>
<span data-ttu-id="0e596-103">서비스 패브릭 응용 프로그램 유형 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="0e596-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e596-104">SYNTAX</span></span>

### <span data-ttu-id="0e596-105">ByResourceGroupAndCluster (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e596-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e596-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0e596-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e596-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e596-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e596-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0e596-108">DESCRIPTION</span></span>
<span data-ttu-id="0e596-109">이 cmdlet을 사용 하 여 지정 된 리소스 그룹 및 클러스터의 응용 프로그램 유형 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="0e596-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0e596-110">EXAMPLES</span></span>

### <span data-ttu-id="0e596-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e596-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="0e596-112">이 예제에서는 해당 리소스를 찾을 수 없는 경우 지정 된 매개 변수를 사용 하 여 응용 프로그램 형식 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="0e596-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0e596-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="0e596-114">이 예제에서는 지정 된 클러스터 아래에 정의 된 응용 프로그램 종류의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="0e596-115">변수</span><span class="sxs-lookup"><span data-stu-id="0e596-115">PARAMETERS</span></span>

### <span data-ttu-id="0e596-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0e596-116">-ClusterName</span></span>
<span data-ttu-id="0e596-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0e596-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e596-118">-DefaultProfile</span></span>
<span data-ttu-id="0e596-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e596-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0e596-120">-Name</span></span>
<span data-ttu-id="0e596-121">응용 프로그램 종류의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="0e596-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="0e596-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e596-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e596-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0e596-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e596-124">-ResourceId</span></span>
<span data-ttu-id="0e596-125">응용 프로그램 종류의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="0e596-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e596-126">CommonParameters</span></span>
<span data-ttu-id="0e596-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e596-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e596-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e596-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e596-129">입력</span><span class="sxs-lookup"><span data-stu-id="0e596-129">INPUTS</span></span>

### <span data-ttu-id="0e596-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e596-130">System.String</span></span>

## <span data-ttu-id="0e596-131">출력</span><span class="sxs-lookup"><span data-stu-id="0e596-131">OUTPUTS</span></span>

### <span data-ttu-id="0e596-132">ServiceFabric. m a m/. m i m m Applicationtype</span><span class="sxs-lookup"><span data-stu-id="0e596-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="0e596-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0e596-133">NOTES</span></span>

## <span data-ttu-id="0e596-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e596-134">RELATED LINKS</span></span>
