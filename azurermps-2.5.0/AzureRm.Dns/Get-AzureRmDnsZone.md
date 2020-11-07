---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882254"
---
# <span data-ttu-id="02253-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="02253-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="02253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02253-102">SYNOPSIS</span></span>
<span data-ttu-id="02253-103">DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02253-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02253-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02253-104">SYNTAX</span></span>

### <span data-ttu-id="02253-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="02253-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="02253-106">리소스</span><span class="sxs-lookup"><span data-stu-id="02253-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="02253-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02253-107">DESCRIPTION</span></span>
<span data-ttu-id="02253-108">**AzureRmDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Domain Name System) 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02253-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="02253-109">*Name* 매개 변수를 지정 하면 단일 **DnsZone** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02253-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="02253-110">*Name* 매개 변수를 지정 하지 않으면 지정 된 리소스 그룹의 모든 영역이 포함 된 배열이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02253-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="02253-111">**DnsZone** 개체를 사용 하 여 영역을 업데이트할 수 있습니다 (예: **레코드 집합** 개체를 추가할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="02253-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="02253-112">예제의</span><span class="sxs-lookup"><span data-stu-id="02253-112">EXAMPLES</span></span>

### <span data-ttu-id="02253-113">예제 1: 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="02253-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="02253-114">이 예제에서는 지정 된 리소스 그룹에서 myzone.com 이라는 DNS 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="02253-115">예제 2: 리소스 그룹의 모든 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="02253-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="02253-116">이 예제에서는 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="02253-117">예제 3: 구독에 있는 모든 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="02253-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="02253-118">이 예제에서는 현재 Azure 구독에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="02253-119">변수</span><span class="sxs-lookup"><span data-stu-id="02253-119">PARAMETERS</span></span>

### <span data-ttu-id="02253-120">-이름</span><span class="sxs-lookup"><span data-stu-id="02253-120">-Name</span></span>
<span data-ttu-id="02253-121">가져올 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="02253-122">*Name* 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02253-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="02253-123">*ResourceGroupName* 매개 변수를 생략 해도이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02253-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02253-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02253-124">-ResourceGroupName</span></span>
<span data-ttu-id="02253-125">가져올 DNS 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="02253-126">*ResourceGroupName* 를 지정 하지 않은 경우에는 *Name* 매개 변수도 생략 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="02253-127">이 경우이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02253-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02253-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02253-128">CommonParameters</span></span>
<span data-ttu-id="02253-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02253-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02253-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02253-131">입력</span><span class="sxs-lookup"><span data-stu-id="02253-131">INPUTS</span></span>

### <span data-ttu-id="02253-132">않아야</span><span class="sxs-lookup"><span data-stu-id="02253-132">None</span></span>
<span data-ttu-id="02253-133">이 cmdlet은 사용자가 파이프를 입력할 수 있도록 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02253-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="02253-134">출력</span><span class="sxs-lookup"><span data-stu-id="02253-134">OUTPUTS</span></span>

### <span data-ttu-id="02253-135">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="02253-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="02253-136">이 cmdlet은 DNS 영역을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02253-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="02253-137">영역 이름을 지정 하지 않으면 영역 개체의 배열이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02253-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="02253-138">상속자</span><span class="sxs-lookup"><span data-stu-id="02253-138">NOTES</span></span>

## <span data-ttu-id="02253-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02253-139">RELATED LINKS</span></span>

[<span data-ttu-id="02253-140">새로운 AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="02253-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="02253-141">제거-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="02253-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="02253-142">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="02253-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
