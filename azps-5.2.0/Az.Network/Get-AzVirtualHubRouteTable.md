---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357540"
---
# <span data-ttu-id="ec091-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ec091-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="ec091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec091-102">SYNOPSIS</span></span>
<span data-ttu-id="ec091-103">가상 허브에서 가상 허브 경로 테이블을 얻거나 가상 허브의 모든 경로 테이블을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="ec091-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec091-104">SYNTAX</span></span>

### <span data-ttu-id="ec091-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec091-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec091-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ec091-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec091-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ec091-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec091-108">설명</span><span class="sxs-lookup"><span data-stu-id="ec091-108">DESCRIPTION</span></span>
<span data-ttu-id="ec091-109">가상 허브에서 가상 허브 경로 테이블을 얻거나 가상 허브의 모든 경로 테이블을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="ec091-110">예제</span><span class="sxs-lookup"><span data-stu-id="ec091-110">EXAMPLES</span></span>

### <span data-ttu-id="ec091-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec091-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="ec091-112">이 cmdlet은 리소스 그룹 이름, 허브 이름 및 경로 테이블 이름을 사용하여 경로 테이블 리소스를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="ec091-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ec091-113">Example 2</span></span>
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

<span data-ttu-id="ec091-114">이 cmdlet은 리소스 그룹 이름 및 허브 이름을 사용하여 가상 허브에 있는 모든 경로 테이블을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="ec091-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec091-115">PARAMETERS</span></span>

### <span data-ttu-id="ec091-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec091-116">-DefaultProfile</span></span>
<span data-ttu-id="ec091-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec091-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="ec091-118">-HubName</span></span>
<span data-ttu-id="ec091-119">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-119">The parent resource name.</span></span>

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

### <span data-ttu-id="ec091-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ec091-120">-Name</span></span>
<span data-ttu-id="ec091-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-121">The resource name.</span></span>

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

### <span data-ttu-id="ec091-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ec091-122">-ParentResourceId</span></span>
<span data-ttu-id="ec091-123">부모 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-123">The parent resource id.</span></span>

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

### <span data-ttu-id="ec091-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec091-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec091-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-125">The resource group name.</span></span>

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

### <span data-ttu-id="ec091-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="ec091-126">-VirtualHub</span></span>
<span data-ttu-id="ec091-127">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-127">The parent resource.</span></span>

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

### <span data-ttu-id="ec091-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec091-128">CommonParameters</span></span>
<span data-ttu-id="ec091-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec091-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec091-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec091-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec091-131">입력</span><span class="sxs-lookup"><span data-stu-id="ec091-131">INPUTS</span></span>

### <span data-ttu-id="ec091-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ec091-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ec091-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ec091-133">System.String</span></span>

## <span data-ttu-id="ec091-134">출력</span><span class="sxs-lookup"><span data-stu-id="ec091-134">OUTPUTS</span></span>

### <span data-ttu-id="ec091-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ec091-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="ec091-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec091-136">NOTES</span></span>

## <span data-ttu-id="ec091-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec091-137">RELATED LINKS</span></span>
