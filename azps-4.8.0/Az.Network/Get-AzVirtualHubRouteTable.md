---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204507"
---
# <span data-ttu-id="f85e6-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f85e6-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="f85e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f85e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f85e6-103">가상 허브에서 가상 허브 경로 테이블을 가져오거나 가상 허브의 모든 경로 테이블을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="f85e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f85e6-104">SYNTAX</span></span>

### <span data-ttu-id="f85e6-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f85e6-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f85e6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f85e6-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f85e6-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="f85e6-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f85e6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f85e6-108">DESCRIPTION</span></span>
<span data-ttu-id="f85e6-109">가상 허브에서 가상 허브 경로 테이블을 가져오거나 가상 허브의 모든 경로 테이블을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="f85e6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f85e6-110">EXAMPLES</span></span>

### <span data-ttu-id="f85e6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f85e6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="f85e6-112">이 cmdlet은 리소스 그룹 이름, 허브 이름, 경로 테이블 이름을 사용 하 여 경로 테이블 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="f85e6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f85e6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="f85e6-114">이 cmdlet은 리소스 그룹 이름 및 허브 이름을 사용 하 여 가상 허브에 있는 모든 경로 테이블을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="f85e6-115">변수</span><span class="sxs-lookup"><span data-stu-id="f85e6-115">PARAMETERS</span></span>

### <span data-ttu-id="f85e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85e6-116">-DefaultProfile</span></span>
<span data-ttu-id="f85e6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85e6-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="f85e6-118">-HubName</span></span>
<span data-ttu-id="f85e6-119">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85e6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f85e6-120">-Name</span></span>
<span data-ttu-id="f85e6-121">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85e6-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f85e6-122">-ParentResourceId</span></span>
<span data-ttu-id="f85e6-123">부모 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f85e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="f85e6-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85e6-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f85e6-126">-VirtualHub</span></span>
<span data-ttu-id="f85e6-127">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f85e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85e6-128">CommonParameters</span></span>
<span data-ttu-id="f85e6-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f85e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85e6-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f85e6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85e6-131">입력</span><span class="sxs-lookup"><span data-stu-id="f85e6-131">INPUTS</span></span>

### <span data-ttu-id="f85e6-132">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f85e6-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f85e6-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f85e6-133">System.String</span></span>

## <span data-ttu-id="f85e6-134">출력</span><span class="sxs-lookup"><span data-stu-id="f85e6-134">OUTPUTS</span></span>

### <span data-ttu-id="f85e6-135">PSVirtualHubRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f85e6-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="f85e6-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f85e6-136">NOTES</span></span>

## <span data-ttu-id="f85e6-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f85e6-137">RELATED LINKS</span></span>
