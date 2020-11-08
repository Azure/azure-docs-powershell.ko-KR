---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216380"
---
# <span data-ttu-id="afccd-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="afccd-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="afccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afccd-102">SYNOPSIS</span></span>
<span data-ttu-id="afccd-103">Peerings의 등록 된 접두사를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="afccd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afccd-104">SYNTAX</span></span>

### <span data-ttu-id="afccd-105">ByResourceGroupAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="afccd-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afccd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="afccd-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afccd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="afccd-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afccd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="afccd-108">DESCRIPTION</span></span>
<span data-ttu-id="afccd-109">Peerings의 등록 된 접두사를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="afccd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="afccd-110">EXAMPLES</span></span>

### <span data-ttu-id="afccd-111">피어 링 용 등록 된 ASNs 목록</span><span class="sxs-lookup"><span data-stu-id="afccd-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="afccd-112">등록 된 asn을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-112">Lists registered asn.</span></span>

### <span data-ttu-id="afccd-113">이름으로 피어 링에 등록 된 ASN을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="afccd-114">등록 된 피어 링 asn을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-114">Gets registered peering asn.</span></span>

<span data-ttu-id="afccd-115">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="afccd-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="afccd-116">변수</span><span class="sxs-lookup"><span data-stu-id="afccd-116">PARAMETERS</span></span>

### <span data-ttu-id="afccd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afccd-117">-DefaultProfile</span></span>
<span data-ttu-id="afccd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afccd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afccd-119">-InputObject</span></span>
<span data-ttu-id="afccd-120">Get-AzPeering 사용</span><span class="sxs-lookup"><span data-stu-id="afccd-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="afccd-121">-이름</span><span class="sxs-lookup"><span data-stu-id="afccd-121">-Name</span></span>
<span data-ttu-id="afccd-122">접두사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-122">The name of prefix.</span></span>

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

### <span data-ttu-id="afccd-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="afccd-123">-PeeringName</span></span>
<span data-ttu-id="afccd-124">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="afccd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afccd-125">-ResourceGroupName</span></span>
<span data-ttu-id="afccd-126">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="afccd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afccd-127">-ResourceId</span></span>
<span data-ttu-id="afccd-128">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-128">The resource id string name.</span></span>

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

### <span data-ttu-id="afccd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afccd-129">CommonParameters</span></span>
<span data-ttu-id="afccd-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afccd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afccd-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="afccd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afccd-132">입력</span><span class="sxs-lookup"><span data-stu-id="afccd-132">INPUTS</span></span>

### <span data-ttu-id="afccd-133">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="afccd-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="afccd-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afccd-134">System.String</span></span>

## <span data-ttu-id="afccd-135">출력</span><span class="sxs-lookup"><span data-stu-id="afccd-135">OUTPUTS</span></span>

### <span data-ttu-id="afccd-136">PSPeeringRegisteredPrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="afccd-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="afccd-137">상속자</span><span class="sxs-lookup"><span data-stu-id="afccd-137">NOTES</span></span>

## <span data-ttu-id="afccd-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afccd-138">RELATED LINKS</span></span>
