---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216381"
---
# <span data-ttu-id="a8857-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a8857-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a8857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8857-102">SYNOPSIS</span></span>
<span data-ttu-id="a8857-103">인터넷 교환 라우팅 서버 유형 peerings의 등록 된 ASN을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="a8857-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8857-104">SYNTAX</span></span>

### <span data-ttu-id="a8857-105">ByResourceGroupAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8857-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8857-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8857-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8857-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8857-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8857-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a8857-108">DESCRIPTION</span></span>
<span data-ttu-id="a8857-109">등록 된 ASN을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="a8857-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a8857-110">EXAMPLES</span></span>

### <span data-ttu-id="a8857-111">피어 링 용 등록 된 ASNs 목록</span><span class="sxs-lookup"><span data-stu-id="a8857-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="a8857-112">등록 된 asn을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-112">Lists registered asn.</span></span>

### <span data-ttu-id="a8857-113">이름으로 피어 링에 등록 된 ASN을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="a8857-114">등록 된 피어 링 asn을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="a8857-115">변수</span><span class="sxs-lookup"><span data-stu-id="a8857-115">PARAMETERS</span></span>

### <span data-ttu-id="a8857-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8857-116">-DefaultProfile</span></span>
<span data-ttu-id="a8857-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8857-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8857-118">-InputObject</span></span>
<span data-ttu-id="a8857-119">Get-AzPeering 사용</span><span class="sxs-lookup"><span data-stu-id="a8857-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="a8857-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a8857-120">-Name</span></span>
<span data-ttu-id="a8857-121">등록 된 ASN의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="a8857-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a8857-122">-PeeringName</span></span>
<span data-ttu-id="a8857-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a8857-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8857-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8857-125">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="a8857-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8857-126">-ResourceId</span></span>
<span data-ttu-id="a8857-127">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-127">The resource id string name.</span></span>

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

### <span data-ttu-id="a8857-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8857-128">CommonParameters</span></span>
<span data-ttu-id="a8857-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8857-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8857-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8857-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8857-131">입력</span><span class="sxs-lookup"><span data-stu-id="a8857-131">INPUTS</span></span>

### <span data-ttu-id="a8857-132">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8857-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a8857-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a8857-133">System.String</span></span>

## <span data-ttu-id="a8857-134">출력</span><span class="sxs-lookup"><span data-stu-id="a8857-134">OUTPUTS</span></span>

### <span data-ttu-id="a8857-135">PSPeeringRegisteredAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8857-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a8857-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a8857-136">NOTES</span></span>

## <span data-ttu-id="a8857-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8857-137">RELATED LINKS</span></span>
