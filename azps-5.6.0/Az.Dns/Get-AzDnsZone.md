---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: a788cf3638d124dac164f19171f1be89afc2e385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984825"
---
# <span data-ttu-id="39826-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="39826-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="39826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39826-102">SYNOPSIS</span></span>
<span data-ttu-id="39826-103">DNS 영역이 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="39826-104">구문</span><span class="sxs-lookup"><span data-stu-id="39826-104">SYNTAX</span></span>

### <span data-ttu-id="39826-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="39826-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39826-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39826-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39826-107">설명</span><span class="sxs-lookup"><span data-stu-id="39826-107">DESCRIPTION</span></span>
<span data-ttu-id="39826-108">**Get-AzDnsZone** cmdlet은 지정된 리소스 그룹에서 DNS(도메인 이름 시스템) 지역을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39826-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="39826-109">이름 매개 *변수를 지정하면* **단일 DnsZone** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="39826-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="39826-110">이름 매개 변수를  지정하지 않으면 지정된 리소스 그룹의 모든 영역이 포함된 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="39826-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="39826-111">**DnsZone** 개체를 사용하여 영역 업데이트(예: **RecordSet** 개체)를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39826-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="39826-112">예제</span><span class="sxs-lookup"><span data-stu-id="39826-112">EXAMPLES</span></span>

### <span data-ttu-id="39826-113">예제 1: 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="39826-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="39826-114">이 예제에서는 지정된 리소스 그룹에서 myzone.com DNS 영역이 지정한 다음, 해당 dns $Zone 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="39826-115">예제 2: 리소스 그룹의 모든 영역 사용</span><span class="sxs-lookup"><span data-stu-id="39826-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="39826-116">이 예제에서는 지정된 리소스 그룹에 있는 모든 DNS $Zones 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="39826-117">예제 3: 구독의 모든 영역 사용</span><span class="sxs-lookup"><span data-stu-id="39826-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="39826-118">이 예제에서는 현재 Azure 구독의 모든 DNS 영역이 도착한 다음, 해당 DNS $Zones 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="39826-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="39826-119">PARAMETERS</span></span>

### <span data-ttu-id="39826-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39826-120">-DefaultProfile</span></span>
<span data-ttu-id="39826-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="39826-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39826-122">-Name</span><span class="sxs-lookup"><span data-stu-id="39826-122">-Name</span></span>
<span data-ttu-id="39826-123">얻을 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="39826-124">이름 매개 변수에 대한  값을 지정하지 않으면 이 cmdlet은 지정된 리소스 그룹의 모든 DNS 영역이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="39826-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="39826-125">*ResourceGroupName* 매개 변수를 생략하는 경우 이 cmdlet은 현재 Azure 구독의 모든 DNS 지역을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39826-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39826-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39826-126">-ResourceGroupName</span></span>
<span data-ttu-id="39826-127">얻을 DNS 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="39826-128">*ResourceGroupName을* 지정하지 않으면 이름 매개 변수도 *생략해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="39826-129">이 경우 이 cmdlet은 현재 Azure 구독의 모든 DNS 지역을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39826-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39826-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39826-130">CommonParameters</span></span>
<span data-ttu-id="39826-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39826-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39826-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="39826-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39826-133">입력</span><span class="sxs-lookup"><span data-stu-id="39826-133">INPUTS</span></span>

### <span data-ttu-id="39826-134">System.String</span><span class="sxs-lookup"><span data-stu-id="39826-134">System.String</span></span>

## <span data-ttu-id="39826-135">출력</span><span class="sxs-lookup"><span data-stu-id="39826-135">OUTPUTS</span></span>

### <span data-ttu-id="39826-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="39826-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="39826-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39826-137">NOTES</span></span>

## <span data-ttu-id="39826-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39826-138">RELATED LINKS</span></span>

[<span data-ttu-id="39826-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="39826-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="39826-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="39826-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="39826-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="39826-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
