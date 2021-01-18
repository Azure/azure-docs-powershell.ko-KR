---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492506"
---
# <span data-ttu-id="4cd4c-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4cd4c-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4cd4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cd4c-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd4c-103">인터넷 교환 경로 서버 형식 피어링에 등록된 ASN을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="4cd4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4cd4c-104">SYNTAX</span></span>

### <span data-ttu-id="4cd4c-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4cd4c-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cd4c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4cd4c-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cd4c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cd4c-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cd4c-108">설명</span><span class="sxs-lookup"><span data-stu-id="4cd4c-108">DESCRIPTION</span></span>
<span data-ttu-id="4cd4c-109">등록된 ASN을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="4cd4c-110">예제</span><span class="sxs-lookup"><span data-stu-id="4cd4c-110">EXAMPLES</span></span>

### <span data-ttu-id="4cd4c-111">피어링을 위해 등록된 ASNS 나열</span><span class="sxs-lookup"><span data-stu-id="4cd4c-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="4cd4c-112">등록된 asn을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-112">Lists registered asn.</span></span>

### <span data-ttu-id="4cd4c-113">이름에 의해 피어링을 위해 등록된 ASN을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="4cd4c-114">등록된 피어링 asn을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="4cd4c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cd4c-115">PARAMETERS</span></span>

### <span data-ttu-id="4cd4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd4c-116">-DefaultProfile</span></span>
<span data-ttu-id="4cd4c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cd4c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cd4c-118">-InputObject</span></span>
<span data-ttu-id="4cd4c-119">다음 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="4cd4c-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="4cd4c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4cd4c-120">-Name</span></span>
<span data-ttu-id="4cd4c-121">등록된 ASN의 이름</span><span class="sxs-lookup"><span data-stu-id="4cd4c-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="4cd4c-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="4cd4c-122">-PeeringName</span></span>
<span data-ttu-id="4cd4c-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="4cd4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4cd4c-125">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="4cd4c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cd4c-126">-ResourceId</span></span>
<span data-ttu-id="4cd4c-127">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-127">The resource id string name.</span></span>

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

### <span data-ttu-id="4cd4c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd4c-128">CommonParameters</span></span>
<span data-ttu-id="4cd4c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd4c-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd4c-131">입력</span><span class="sxs-lookup"><span data-stu-id="4cd4c-131">INPUTS</span></span>

### <span data-ttu-id="4cd4c-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="4cd4c-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="4cd4c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4cd4c-133">System.String</span></span>

## <span data-ttu-id="4cd4c-134">출력</span><span class="sxs-lookup"><span data-stu-id="4cd4c-134">OUTPUTS</span></span>

### <span data-ttu-id="4cd4c-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="4cd4c-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="4cd4c-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4cd4c-136">NOTES</span></span>

## <span data-ttu-id="4cd4c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cd4c-137">RELATED LINKS</span></span>
