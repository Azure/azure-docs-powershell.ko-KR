---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: e525580d7384eef6b7fa7518fc6ddc5707a010ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530761"
---
# <span data-ttu-id="d49bb-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d49bb-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="d49bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d49bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d49bb-103">경로 테이블의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d49bb-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d49bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d49bb-105">DESCRIPTION</span></span>
<span data-ttu-id="d49bb-106">**Set-AzureRmRouteTable** Cmdlet은 Azure 경로 테이블에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="d49bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d49bb-107">EXAMPLES</span></span>

### <span data-ttu-id="d49bb-108">예제 1: 경로를 추가한 다음 경로 테이블의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="d49bb-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="d49bb-109">이 명령은 Get-AzureRmRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="d49bb-110">이 명령은 파이프라인 연산자를 사용 하 여 Add-AzureRmRouteConfig cmdlet에 해당 테이블을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d49bb-111">**Add-AzureRmRouteConfig** 는 Route07 이라는 경로를 추가한 다음 결과를 현재 cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="d49bb-112">변수</span><span class="sxs-lookup"><span data-stu-id="d49bb-112">PARAMETERS</span></span>

### <span data-ttu-id="d49bb-113">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d49bb-113">-RouteTable</span></span>
<span data-ttu-id="d49bb-114">이 cmdlet이 경로 테이블을 설정 하는 목표 상태를 나타내는 경로 테이블 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-114">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d49bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49bb-115">-DefaultProfile</span></span>
<span data-ttu-id="d49bb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d49bb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49bb-117">CommonParameters</span></span>
<span data-ttu-id="d49bb-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49bb-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49bb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49bb-120">입력</span><span class="sxs-lookup"><span data-stu-id="d49bb-120">INPUTS</span></span>

### <span data-ttu-id="d49bb-121">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d49bb-121">PSRouteTable</span></span>
<span data-ttu-id="d49bb-122">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d49bb-122">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="d49bb-123">출력</span><span class="sxs-lookup"><span data-stu-id="d49bb-123">OUTPUTS</span></span>

### <span data-ttu-id="d49bb-124">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d49bb-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d49bb-125">상속자</span><span class="sxs-lookup"><span data-stu-id="d49bb-125">NOTES</span></span>

## <span data-ttu-id="d49bb-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d49bb-126">RELATED LINKS</span></span>

[<span data-ttu-id="d49bb-127">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d49bb-127">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="d49bb-128">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d49bb-128">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="d49bb-129">새로운 AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d49bb-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="d49bb-130">제거-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d49bb-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


