---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: d25cca457adb70398d29b1b2a8044ac14af893db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703282"
---
# <span data-ttu-id="57aab-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57aab-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="57aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57aab-102">SYNOPSIS</span></span>
<span data-ttu-id="57aab-103">DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57aab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57aab-104">SYNTAX</span></span>

### <span data-ttu-id="57aab-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="57aab-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57aab-106">리소스</span><span class="sxs-lookup"><span data-stu-id="57aab-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57aab-107">설명은</span><span class="sxs-lookup"><span data-stu-id="57aab-107">DESCRIPTION</span></span>
<span data-ttu-id="57aab-108">**AzureRmDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Domain Name System) 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="57aab-109">*Name* 매개 변수를 지정 하면 단일 **DnsZone** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="57aab-110">*Name* 매개 변수를 지정 하지 않으면 지정 된 리소스 그룹의 모든 영역이 포함 된 배열이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="57aab-111">**DnsZone** 개체를 사용 하 여 영역을 업데이트할 수 있습니다 (예: **레코드 집합** 개체를 추가할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="57aab-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="57aab-112">예제의</span><span class="sxs-lookup"><span data-stu-id="57aab-112">EXAMPLES</span></span>

### <span data-ttu-id="57aab-113">예제 1: 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="57aab-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="57aab-114">이 예제에서는 지정 된 리소스 그룹에서 myzone.com 이라는 DNS 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="57aab-115">예제 2: 리소스 그룹의 모든 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="57aab-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="57aab-116">이 예제에서는 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="57aab-117">예제 3: 구독에 있는 모든 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="57aab-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="57aab-118">이 예제에서는 현재 Azure 구독에 있는 모든 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="57aab-119">변수</span><span class="sxs-lookup"><span data-stu-id="57aab-119">PARAMETERS</span></span>

### <span data-ttu-id="57aab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57aab-120">-DefaultProfile</span></span>
<span data-ttu-id="57aab-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="57aab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57aab-122">-이름</span><span class="sxs-lookup"><span data-stu-id="57aab-122">-Name</span></span>
<span data-ttu-id="57aab-123">가져올 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-123">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="57aab-124">*Name* 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 지정 된 리소스 그룹에 있는 모든 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="57aab-125">*ResourceGroupName* 매개 변수를 생략 해도이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="57aab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57aab-126">-ResourceGroupName</span></span>
<span data-ttu-id="57aab-127">가져올 DNS 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="57aab-128">*ResourceGroupName* 를 지정 하지 않은 경우에는 *Name* 매개 변수도 생략 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="57aab-129">이 경우이 cmdlet은 현재 Azure 구독에서 모든 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="57aab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57aab-130">CommonParameters</span></span>
<span data-ttu-id="57aab-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57aab-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57aab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57aab-133">입력</span><span class="sxs-lookup"><span data-stu-id="57aab-133">INPUTS</span></span>

### <span data-ttu-id="57aab-134">않아야</span><span class="sxs-lookup"><span data-stu-id="57aab-134">None</span></span>
<span data-ttu-id="57aab-135">이 cmdlet은 사용자가 파이프를 입력할 수 있도록 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="57aab-136">출력</span><span class="sxs-lookup"><span data-stu-id="57aab-136">OUTPUTS</span></span>

### <span data-ttu-id="57aab-137">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="57aab-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="57aab-138">이 cmdlet은 DNS 영역을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="57aab-139">영역 이름을 지정 하지 않으면 영역 개체의 배열이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57aab-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="57aab-140">상속자</span><span class="sxs-lookup"><span data-stu-id="57aab-140">NOTES</span></span>

## <span data-ttu-id="57aab-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57aab-141">RELATED LINKS</span></span>

[<span data-ttu-id="57aab-142">새로운 AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57aab-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="57aab-143">제거-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57aab-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="57aab-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57aab-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
