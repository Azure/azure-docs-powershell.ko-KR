---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: c282ea9e902f26d010c2421339de68bc670e2f35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204319"
---
# <span data-ttu-id="20c09-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="20c09-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="20c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c09-102">SYNOPSIS</span></span>
<span data-ttu-id="20c09-103">서비스 패브릭 응용 프로그램 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="20c09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20c09-104">SYNTAX</span></span>

### <span data-ttu-id="20c09-105">ByResourceGroupAndCluster (기본값)</span><span class="sxs-lookup"><span data-stu-id="20c09-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c09-106">ByName</span><span class="sxs-lookup"><span data-stu-id="20c09-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c09-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="20c09-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20c09-108">설명은</span><span class="sxs-lookup"><span data-stu-id="20c09-108">DESCRIPTION</span></span>
<span data-ttu-id="20c09-109">이 cmdlet은 지정 된 리소스 그룹 및 클러스터의 응용 프로그램 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="20c09-110">예제의</span><span class="sxs-lookup"><span data-stu-id="20c09-110">EXAMPLES</span></span>

### <span data-ttu-id="20c09-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="20c09-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="20c09-112">이 예제에서는 "testApp" 응용 프로그램에 대 한 응용 프로그램 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="20c09-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="20c09-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="20c09-114">이 예제에서는 "testCluster" 클러스터 아래에 있는 응용 프로그램의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="20c09-115">변수</span><span class="sxs-lookup"><span data-stu-id="20c09-115">PARAMETERS</span></span>

### <span data-ttu-id="20c09-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="20c09-116">-ClusterName</span></span>
<span data-ttu-id="20c09-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="20c09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c09-118">-DefaultProfile</span></span>
<span data-ttu-id="20c09-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c09-120">-이름</span><span class="sxs-lookup"><span data-stu-id="20c09-120">-Name</span></span>
<span data-ttu-id="20c09-121">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="20c09-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c09-122">-ResourceGroupName</span></span>
<span data-ttu-id="20c09-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="20c09-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20c09-124">-ResourceId</span></span>
<span data-ttu-id="20c09-125">응용 프로그램의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="20c09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c09-126">CommonParameters</span></span>
<span data-ttu-id="20c09-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20c09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c09-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20c09-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c09-129">입력</span><span class="sxs-lookup"><span data-stu-id="20c09-129">INPUTS</span></span>

### <span data-ttu-id="20c09-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20c09-130">System.String</span></span>

## <span data-ttu-id="20c09-131">출력</span><span class="sxs-lookup"><span data-stu-id="20c09-131">OUTPUTS</span></span>

### <span data-ttu-id="20c09-132">ServiceFabric 응용 프로그램의 경우</span><span class="sxs-lookup"><span data-stu-id="20c09-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="20c09-133">상속자</span><span class="sxs-lookup"><span data-stu-id="20c09-133">NOTES</span></span>

## <span data-ttu-id="20c09-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20c09-134">RELATED LINKS</span></span>
