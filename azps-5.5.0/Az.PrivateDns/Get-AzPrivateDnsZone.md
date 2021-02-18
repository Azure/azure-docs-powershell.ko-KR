---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202124"
---
# <span data-ttu-id="88fb1-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88fb1-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="88fb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="88fb1-103">사설 DNS 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="88fb1-104">구문</span><span class="sxs-lookup"><span data-stu-id="88fb1-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88fb1-105">설명</span><span class="sxs-lookup"><span data-stu-id="88fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="88fb1-106">**Get-AzPrivateDnsZone** cmdlet은 지정된 리소스 그룹에서 DNS(개인 도메인 이름 시스템) 지역을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="88fb1-107">Name 매개 *변수를 지정하면* 단일 **PrivateDnsZone** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="88fb1-108">Name 매개 변수를 *지정하지* 않으면 지정된 리소스 그룹의 모든 영역이 포함된 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="88fb1-109">**PrivateDnsZone** 개체를 사용하여 영역 업데이트를 할 수 있습니다. 예를 들어 **RecordSet** 개체를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="88fb1-110">예제</span><span class="sxs-lookup"><span data-stu-id="88fb1-110">EXAMPLES</span></span>

### <span data-ttu-id="88fb1-111">예제 1: 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="88fb1-111">Example 1: Get a zone</span></span>
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

### <span data-ttu-id="88fb1-112">예제 2: 리소스 그룹의 모든 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="88fb1-112">Example 2: Get all of the zones in a resource group</span></span>
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

<span data-ttu-id="88fb1-113">이 예제에서는 지정된 리소스 그룹에 있는 모든 사설 DNS 영역이 있는 경우 해당 $Zones 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="88fb1-114">예제 3: 구독의 모든 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="88fb1-114">Example 3: Get all of the zones in a subscription</span></span>
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

<span data-ttu-id="88fb1-115">이 예제에서는 현재 Azure 구독의 모든 사설 DNS 영역이 있는 경우 해당 도메인을 $Zones 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="88fb1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88fb1-116">PARAMETERS</span></span>

### <span data-ttu-id="88fb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fb1-117">-DefaultProfile</span></span>
<span data-ttu-id="88fb1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88fb1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88fb1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="88fb1-119">-Name</span></span>
<span data-ttu-id="88fb1-120">얻을 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="88fb1-121">Name 매개 변수에 대한  값을 지정하지 않으면 이 cmdlet은 지정된 리소스 그룹의 모든 개인 DNS 영역이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="88fb1-122">*ResourceGroupName* 매개 변수도 생략하면 이 cmdlet은 현재 Azure 구독의 모든 사설 DNS 지역을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="88fb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88fb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="88fb1-124">얻을 개인 DNS 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="88fb1-125">*ResourceGroupName을* 지정하지 않으면 이름 매개 변수도 *생략해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-125">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="88fb1-126">이 경우 이 cmdlet은 현재 Azure 구독의 모든 사설 DNS 지역을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="88fb1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fb1-127">CommonParameters</span></span>
<span data-ttu-id="88fb1-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88fb1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fb1-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="88fb1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fb1-130">입력</span><span class="sxs-lookup"><span data-stu-id="88fb1-130">INPUTS</span></span>

### <span data-ttu-id="88fb1-131">없음</span><span class="sxs-lookup"><span data-stu-id="88fb1-131">None</span></span>

## <span data-ttu-id="88fb1-132">출력</span><span class="sxs-lookup"><span data-stu-id="88fb1-132">OUTPUTS</span></span>

### <span data-ttu-id="88fb1-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88fb1-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="88fb1-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88fb1-134">NOTES</span></span>

## <span data-ttu-id="88fb1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88fb1-135">RELATED LINKS</span></span>

[<span data-ttu-id="88fb1-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88fb1-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="88fb1-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88fb1-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="88fb1-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="88fb1-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
