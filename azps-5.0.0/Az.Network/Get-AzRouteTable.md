---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226409"
---
# <span data-ttu-id="a9e8d-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a9e8d-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="a9e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e8d-103">경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-103">Gets route tables.</span></span>

## <span data-ttu-id="a9e8d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9e8d-104">SYNTAX</span></span>

### <span data-ttu-id="a9e8d-105">NoExpand (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9e8d-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9e8d-106">확장</span><span class="sxs-lookup"><span data-stu-id="a9e8d-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9e8d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a9e8d-107">DESCRIPTION</span></span>
<span data-ttu-id="a9e8d-108">**Get-AzRouteTable** Cmdlet은 Azure 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="a9e8d-109">단일 경로 테이블을 가져오거나 리소스 그룹 또는 구독에서 모든 경로 테이블을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="a9e8d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a9e8d-110">EXAMPLES</span></span>

### <span data-ttu-id="a9e8d-111">예제 1: 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="a9e8d-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="a9e8d-112">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="a9e8d-113">예제 2: 필터링을 사용 하 여 경로 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="a9e8d-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="a9e8d-114">이 명령은 이름이 "RouteTable"로 시작 하는 모든 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="a9e8d-115">변수</span><span class="sxs-lookup"><span data-stu-id="a9e8d-115">PARAMETERS</span></span>

### <span data-ttu-id="a9e8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e8d-116">-DefaultProfile</span></span>
<span data-ttu-id="a9e8d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9e8d-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a9e8d-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e8d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a9e8d-119">-Name</span></span>
<span data-ttu-id="a9e8d-120">이 cmdlet이 가져오는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a9e8d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e8d-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9e8d-122">이 cmdlet이 가져오는 경로 테이블을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a9e8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e8d-123">CommonParameters</span></span>
<span data-ttu-id="a9e8d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e8d-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e8d-126">입력</span><span class="sxs-lookup"><span data-stu-id="a9e8d-126">INPUTS</span></span>

### <span data-ttu-id="a9e8d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a9e8d-127">System.String</span></span>

## <span data-ttu-id="a9e8d-128">출력</span><span class="sxs-lookup"><span data-stu-id="a9e8d-128">OUTPUTS</span></span>

### <span data-ttu-id="a9e8d-129">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a9e8d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a9e8d-130">NOTES</span></span>

## <span data-ttu-id="a9e8d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9e8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="a9e8d-132">새로운 AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a9e8d-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="a9e8d-133">제거-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a9e8d-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="a9e8d-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a9e8d-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


