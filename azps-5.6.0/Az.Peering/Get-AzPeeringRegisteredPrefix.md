---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 4eb704682885e5040913e08c5242d4142a387ef7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989506"
---
# <span data-ttu-id="bea07-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="bea07-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="bea07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea07-102">SYNOPSIS</span></span>
<span data-ttu-id="bea07-103">피어링에 대한 등록된 도두를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="bea07-104">구문</span><span class="sxs-lookup"><span data-stu-id="bea07-104">SYNTAX</span></span>

### <span data-ttu-id="bea07-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bea07-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea07-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bea07-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea07-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bea07-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bea07-108">설명</span><span class="sxs-lookup"><span data-stu-id="bea07-108">DESCRIPTION</span></span>
<span data-ttu-id="bea07-109">피어링에 대한 등록된 도두를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="bea07-110">예제</span><span class="sxs-lookup"><span data-stu-id="bea07-110">EXAMPLES</span></span>

### <span data-ttu-id="bea07-111">피어링을 위해 등록된 ASNS 나열</span><span class="sxs-lookup"><span data-stu-id="bea07-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="bea07-112">등록된 asn을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-112">Lists registered asn.</span></span>

### <span data-ttu-id="bea07-113">이름으로 피어링을 위해 등록된 ASN을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="bea07-114">등록된 피어링 asn을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-114">Gets registered peering asn.</span></span>

<span data-ttu-id="bea07-115">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="bea07-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="bea07-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bea07-116">PARAMETERS</span></span>

### <span data-ttu-id="bea07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea07-117">-DefaultProfile</span></span>
<span data-ttu-id="bea07-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea07-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bea07-119">-InputObject</span></span>
<span data-ttu-id="bea07-120">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="bea07-120">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bea07-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bea07-121">-Name</span></span>
<span data-ttu-id="bea07-122">도두사 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-122">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea07-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="bea07-123">-PeeringName</span></span>
<span data-ttu-id="bea07-124">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea07-125">-ResourceGroupName</span></span>
<span data-ttu-id="bea07-126">기존 리소스 그룹 이름을 만들거나 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="bea07-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bea07-127">-ResourceId</span></span>
<span data-ttu-id="bea07-128">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-128">The resource id string name.</span></span>

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

### <span data-ttu-id="bea07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea07-129">CommonParameters</span></span>
<span data-ttu-id="bea07-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bea07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea07-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bea07-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea07-132">입력</span><span class="sxs-lookup"><span data-stu-id="bea07-132">INPUTS</span></span>

### <span data-ttu-id="bea07-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="bea07-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="bea07-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bea07-134">System.String</span></span>

## <span data-ttu-id="bea07-135">출력</span><span class="sxs-lookup"><span data-stu-id="bea07-135">OUTPUTS</span></span>

### <span data-ttu-id="bea07-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="bea07-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="bea07-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bea07-137">NOTES</span></span>

## <span data-ttu-id="bea07-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bea07-138">RELATED LINKS</span></span>
