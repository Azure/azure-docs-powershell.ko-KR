---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216377"
---
# <span data-ttu-id="86e78-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="86e78-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="86e78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e78-102">SYNOPSIS</span></span>
<span data-ttu-id="86e78-103">단일 개체의 피어 링 서비스 개체 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="86e78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86e78-104">SYNTAX</span></span>

### <span data-ttu-id="86e78-105">ByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="86e78-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86e78-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="86e78-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86e78-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="86e78-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86e78-108">설명은</span><span class="sxs-lookup"><span data-stu-id="86e78-108">DESCRIPTION</span></span>
<span data-ttu-id="86e78-109">구독에 대 한 피어 링 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="86e78-110">예제의</span><span class="sxs-lookup"><span data-stu-id="86e78-110">EXAMPLES</span></span>

### <span data-ttu-id="86e78-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="86e78-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="86e78-112">리소스 그룹에 대 한 피어 링 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="86e78-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="86e78-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="86e78-114">리소스 그룹 및 이름에 대 한 피어 링 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="86e78-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="86e78-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="86e78-116">리소스 id 별 피어 링 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="86e78-117">변수</span><span class="sxs-lookup"><span data-stu-id="86e78-117">PARAMETERS</span></span>

### <span data-ttu-id="86e78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e78-118">-DefaultProfile</span></span>
<span data-ttu-id="86e78-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e78-120">-이름</span><span class="sxs-lookup"><span data-stu-id="86e78-120">-Name</span></span>
<span data-ttu-id="86e78-121">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e78-122">-ResourceGroupName</span></span>
<span data-ttu-id="86e78-123">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86e78-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86e78-124">-ResourceId</span></span>
<span data-ttu-id="86e78-125">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e78-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e78-126">CommonParameters</span></span>
<span data-ttu-id="86e78-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86e78-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e78-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="86e78-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e78-129">입력</span><span class="sxs-lookup"><span data-stu-id="86e78-129">INPUTS</span></span>

### <span data-ttu-id="86e78-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="86e78-130">System.String</span></span>

## <span data-ttu-id="86e78-131">출력</span><span class="sxs-lookup"><span data-stu-id="86e78-131">OUTPUTS</span></span>

### <span data-ttu-id="86e78-132">PSPeeringService (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="86e78-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="86e78-133">상속자</span><span class="sxs-lookup"><span data-stu-id="86e78-133">NOTES</span></span>

## <span data-ttu-id="86e78-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86e78-134">RELATED LINKS</span></span>
