---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 04e50033a304918eb37d28c2ef5ea5328d5744c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530203"
---
# <span data-ttu-id="cf598-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cf598-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="cf598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf598-102">SYNOPSIS</span></span>
<span data-ttu-id="cf598-103">경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf598-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf598-104">SYNTAX</span></span>

### <span data-ttu-id="cf598-105">NoExpand (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf598-105">NoExpand (Default)</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf598-106">확장</span><span class="sxs-lookup"><span data-stu-id="cf598-106">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf598-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cf598-107">DESCRIPTION</span></span>
<span data-ttu-id="cf598-108">**Get-AzureRmRouteTable** Cmdlet은 Azure 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="cf598-109">단일 경로 테이블을 가져오거나 리소스 그룹 또는 구독에서 모든 경로 테이블을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="cf598-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cf598-110">EXAMPLES</span></span>

### <span data-ttu-id="cf598-111">예제 1: 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf598-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
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

<span data-ttu-id="cf598-112">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="cf598-113">변수</span><span class="sxs-lookup"><span data-stu-id="cf598-113">PARAMETERS</span></span>

### <span data-ttu-id="cf598-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf598-114">-DefaultProfile</span></span>
<span data-ttu-id="cf598-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf598-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cf598-116">-ExpandResource</span></span>
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

### <span data-ttu-id="cf598-117">-이름</span><span class="sxs-lookup"><span data-stu-id="cf598-117">-Name</span></span>
<span data-ttu-id="cf598-118">이 cmdlet이 가져오는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf598-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf598-119">-ResourceGroupName</span></span>
<span data-ttu-id="cf598-120">이 cmdlet이 가져오는 경로 테이블을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="cf598-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf598-121">CommonParameters</span></span>
<span data-ttu-id="cf598-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf598-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf598-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf598-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf598-124">입력</span><span class="sxs-lookup"><span data-stu-id="cf598-124">INPUTS</span></span>

### <span data-ttu-id="cf598-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf598-125">System.String</span></span>

## <span data-ttu-id="cf598-126">출력</span><span class="sxs-lookup"><span data-stu-id="cf598-126">OUTPUTS</span></span>

### <span data-ttu-id="cf598-127">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cf598-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="cf598-128">상속자</span><span class="sxs-lookup"><span data-stu-id="cf598-128">NOTES</span></span>

## <span data-ttu-id="cf598-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf598-129">RELATED LINKS</span></span>

[<span data-ttu-id="cf598-130">새로운 AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cf598-130">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="cf598-131">제거-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cf598-131">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="cf598-132">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="cf598-132">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


