---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: e94eaeb7c9b4302c0d7e5e1f89496939a612d4d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531974"
---
# <span data-ttu-id="96458-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="96458-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="96458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96458-102">SYNOPSIS</span></span>
<span data-ttu-id="96458-103">경로 테이블의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96458-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96458-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96458-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96458-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96458-105">DESCRIPTION</span></span>
<span data-ttu-id="96458-106">**Set-AzureRmRouteTable** Cmdlet은 Azure 경로 테이블에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96458-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="96458-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96458-107">EXAMPLES</span></span>

### <span data-ttu-id="96458-108">예제 1: 경로를 추가한 다음 경로 테이블의 목표 상태 설정</span><span class="sxs-lookup"><span data-stu-id="96458-108">Example 1: Add a route and then set the goal state of the route table</span></span>
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

<span data-ttu-id="96458-109">이 명령은 Get-AzureRmRouteTable cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="96458-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="96458-110">이 명령은 파이프라인 연산자를 사용 하 여 Add-AzureRmRouteConfig cmdlet에 해당 테이블을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="96458-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="96458-111">**Add-AzureRmRouteConfig** 는 Route07 이라는 경로를 추가한 다음 결과를 현재 cmdlet에 전달 하 여 변경 내용을 반영 하도록 표를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="96458-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="96458-112">변수</span><span class="sxs-lookup"><span data-stu-id="96458-112">PARAMETERS</span></span>

### <span data-ttu-id="96458-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96458-113">-AsJob</span></span>
<span data-ttu-id="96458-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="96458-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96458-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96458-115">-DefaultProfile</span></span>
<span data-ttu-id="96458-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96458-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96458-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="96458-117">-RouteTable</span></span>
<span data-ttu-id="96458-118">이 cmdlet이 경로 테이블을 설정 하는 목표 상태를 나타내는 경로 테이블 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96458-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

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

### <span data-ttu-id="96458-119">-확인</span><span class="sxs-lookup"><span data-stu-id="96458-119">-Confirm</span></span>
<span data-ttu-id="96458-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96458-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96458-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96458-121">-WhatIf</span></span>
<span data-ttu-id="96458-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96458-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96458-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96458-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96458-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96458-124">CommonParameters</span></span>
<span data-ttu-id="96458-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96458-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96458-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96458-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96458-127">입력</span><span class="sxs-lookup"><span data-stu-id="96458-127">INPUTS</span></span>

### <span data-ttu-id="96458-128">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="96458-128">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>
<span data-ttu-id="96458-129">매개 변수: RouteTable (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96458-129">Parameters: RouteTable (ByValue)</span></span>

## <span data-ttu-id="96458-130">출력</span><span class="sxs-lookup"><span data-stu-id="96458-130">OUTPUTS</span></span>

### <span data-ttu-id="96458-131">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="96458-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="96458-132">상속자</span><span class="sxs-lookup"><span data-stu-id="96458-132">NOTES</span></span>

## <span data-ttu-id="96458-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96458-133">RELATED LINKS</span></span>

[<span data-ttu-id="96458-134">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="96458-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="96458-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="96458-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="96458-136">새로운 AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="96458-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="96458-137">제거-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="96458-137">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


