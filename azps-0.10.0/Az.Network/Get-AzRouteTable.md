---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: a881e438166729aea8956dc633b7a635499d3752
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875522"
---
# <span data-ttu-id="a2c16-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2c16-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="a2c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c16-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c16-103">경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-103">Gets route tables.</span></span>

## <span data-ttu-id="a2c16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2c16-104">SYNTAX</span></span>

### <span data-ttu-id="a2c16-105">확장</span><span class="sxs-lookup"><span data-stu-id="a2c16-105">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c16-106">NoExpand</span><span class="sxs-lookup"><span data-stu-id="a2c16-106">NoExpand</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2c16-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a2c16-107">DESCRIPTION</span></span>
<span data-ttu-id="a2c16-108">**Get-AzRouteTable** Cmdlet은 Azure 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="a2c16-109">단일 경로 테이블을 가져오거나 리소스 그룹 또는 구독에서 모든 경로 테이블을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="a2c16-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a2c16-110">EXAMPLES</span></span>

### <span data-ttu-id="a2c16-111">예제 1: 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="a2c16-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="a2c16-112">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a2c16-113">변수</span><span class="sxs-lookup"><span data-stu-id="a2c16-113">PARAMETERS</span></span>

### <span data-ttu-id="a2c16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c16-114">-DefaultProfile</span></span>
<span data-ttu-id="a2c16-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c16-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a2c16-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c16-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a2c16-117">-Name</span></span>
<span data-ttu-id="a2c16-118">이 cmdlet이 가져오는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c16-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2c16-120">이 cmdlet이 가져오는 경로 테이블을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c16-121">CommonParameters</span></span>
<span data-ttu-id="a2c16-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c16-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c16-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c16-124">입력</span><span class="sxs-lookup"><span data-stu-id="a2c16-124">INPUTS</span></span>

## <span data-ttu-id="a2c16-125">출력</span><span class="sxs-lookup"><span data-stu-id="a2c16-125">OUTPUTS</span></span>

### <span data-ttu-id="a2c16-126">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a2c16-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a2c16-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a2c16-127">NOTES</span></span>

## <span data-ttu-id="a2c16-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2c16-128">RELATED LINKS</span></span>

[<span data-ttu-id="a2c16-129">새로운 AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2c16-129">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="a2c16-130">제거-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2c16-130">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="a2c16-131">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a2c16-131">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


