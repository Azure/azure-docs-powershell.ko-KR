---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 659281d1f78ea984a3db30817d15a6e92f31cbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699785"
---
# <span data-ttu-id="3366f-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="3366f-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="3366f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3366f-102">SYNOPSIS</span></span>
<span data-ttu-id="3366f-103">개인 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="3366f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3366f-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3366f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3366f-105">DESCRIPTION</span></span>
<span data-ttu-id="3366f-106">**AzPrivateDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Private Domain Name System) 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="3366f-107">*Name* 매개 변수를 지정 하면 단일 **PrivateDnsZone** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="3366f-108">*Name* 매개 변수를 지정 하지 않으면 지정 된 리소스 그룹의 모든 영역이 포함 된 배열이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="3366f-109">**PrivateDnsZone** 개체를 사용 하 여 영역을 업데이트할 수 있습니다 (예: **레코드 집합** 개체를 추가할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="3366f-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="3366f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3366f-110">EXAMPLES</span></span>

### <span data-ttu-id="3366f-111">예제 1: 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="3366f-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="3366f-112">예제 2: 리소스 그룹의 모든 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="3366f-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="3366f-113">이 예제에서는 지정 된 리소스 그룹에 있는 모든 개인 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="3366f-114">예제 3: 구독에 있는 모든 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="3366f-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="3366f-115">이 예제에서는 현재 Azure 구독에 있는 모든 개인 DNS 영역을 가져온 다음 $Zones 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="3366f-116">변수</span><span class="sxs-lookup"><span data-stu-id="3366f-116">PARAMETERS</span></span>

### <span data-ttu-id="3366f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3366f-117">-DefaultProfile</span></span>
<span data-ttu-id="3366f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3366f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3366f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="3366f-119">-Name</span></span>
<span data-ttu-id="3366f-120">가져올 개인 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="3366f-121">*Name* 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 지정 된 리소스 그룹의 모든 비공개 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="3366f-122">*ResourceGroupName* 매개 변수를 생략 해도이 cmdlet은 현재 Azure 구독에서 모든 개인 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3366f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3366f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3366f-124">가져올 개인 DNS 영역을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="3366f-125">*ResourceGroupName* 를 지정 하지 않은 경우에는 *Name* 매개 변수도 생략 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="3366f-126">이 경우이 cmdlet은 현재 Azure 구독에서 모든 개인 DNS 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3366f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3366f-127">CommonParameters</span></span>
<span data-ttu-id="3366f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3366f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3366f-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3366f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3366f-130">입력</span><span class="sxs-lookup"><span data-stu-id="3366f-130">INPUTS</span></span>

### <span data-ttu-id="3366f-131">않아야</span><span class="sxs-lookup"><span data-stu-id="3366f-131">None</span></span>

## <span data-ttu-id="3366f-132">출력</span><span class="sxs-lookup"><span data-stu-id="3366f-132">OUTPUTS</span></span>

### <span data-ttu-id="3366f-133">PrivateDns. PSPrivateDnsZone/.</span><span class="sxs-lookup"><span data-stu-id="3366f-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="3366f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="3366f-134">NOTES</span></span>

## <span data-ttu-id="3366f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3366f-135">RELATED LINKS</span></span>

[<span data-ttu-id="3366f-136">새로운 AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="3366f-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="3366f-137">제거-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="3366f-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="3366f-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="3366f-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
