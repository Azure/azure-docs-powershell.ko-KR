---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184660"
---
# <span data-ttu-id="1ed59-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ed59-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="1ed59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed59-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed59-103">경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-103">Gets route tables.</span></span>

## <span data-ttu-id="1ed59-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ed59-104">SYNTAX</span></span>

### <span data-ttu-id="1ed59-105">NoExpand(기본값)</span><span class="sxs-lookup"><span data-stu-id="1ed59-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ed59-106">확장</span><span class="sxs-lookup"><span data-stu-id="1ed59-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ed59-107">설명</span><span class="sxs-lookup"><span data-stu-id="1ed59-107">DESCRIPTION</span></span>
<span data-ttu-id="1ed59-108">**Get-AzRouteTable** cmdlet은 Azure 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="1ed59-109">단일 경로 테이블을 얻거나 리소스 그룹 또는 구독에서 모든 경로 테이블을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="1ed59-110">예제</span><span class="sxs-lookup"><span data-stu-id="1ed59-110">EXAMPLES</span></span>

### <span data-ttu-id="1ed59-111">예제 1: 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="1ed59-112">이 명령은 ResourceGroup11이라는 리소스 그룹에 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="1ed59-113">예제 2: 필터링을 사용하여 경로 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="1ed59-113">Example 2: List route tables using filtering</span></span>
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

<span data-ttu-id="1ed59-114">이 명령은 이름이 "RouteTable"로 시작하는 모든 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="1ed59-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ed59-115">PARAMETERS</span></span>

### <span data-ttu-id="1ed59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed59-116">-DefaultProfile</span></span>
<span data-ttu-id="1ed59-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed59-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1ed59-118">-ExpandResource</span></span>
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

### <span data-ttu-id="1ed59-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1ed59-119">-Name</span></span>
<span data-ttu-id="1ed59-120">이 cmdlet에서 얻을 경로 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-120">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1ed59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed59-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ed59-122">이 cmdlet에서 얻을 경로 테이블을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1ed59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed59-123">CommonParameters</span></span>
<span data-ttu-id="1ed59-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed59-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ed59-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed59-126">입력</span><span class="sxs-lookup"><span data-stu-id="1ed59-126">INPUTS</span></span>

### <span data-ttu-id="1ed59-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1ed59-127">System.String</span></span>

## <span data-ttu-id="1ed59-128">출력</span><span class="sxs-lookup"><span data-stu-id="1ed59-128">OUTPUTS</span></span>

### <span data-ttu-id="1ed59-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ed59-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1ed59-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ed59-130">NOTES</span></span>

## <span data-ttu-id="1ed59-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ed59-131">RELATED LINKS</span></span>

[<span data-ttu-id="1ed59-132">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ed59-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="1ed59-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ed59-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="1ed59-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ed59-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


