---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: b8ace5d38878e9acbdbfaa25e3bfd4ebfc185260
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700126"
---
# <span data-ttu-id="8de01-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8de01-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="8de01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8de01-102">SYNOPSIS</span></span>
<span data-ttu-id="8de01-103">경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="8de01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8de01-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de01-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8de01-105">DESCRIPTION</span></span>
<span data-ttu-id="8de01-106">**AzRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="8de01-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8de01-107">EXAMPLES</span></span>

### <span data-ttu-id="8de01-108">예제 1: 경로 제거</span><span class="sxs-lookup"><span data-stu-id="8de01-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="8de01-109">이 명령은 **AzRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="8de01-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8de01-111">현재 cmdlet은 Route02 이라는 경로를 제거 하 고 해당 결과를 **AzRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 테이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="8de01-112">표에 Route02 이라는 경로가 더 이상 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="8de01-113">변수</span><span class="sxs-lookup"><span data-stu-id="8de01-113">PARAMETERS</span></span>

### <span data-ttu-id="8de01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de01-114">-DefaultProfile</span></span>
<span data-ttu-id="8de01-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8de01-116">-이름</span><span class="sxs-lookup"><span data-stu-id="8de01-116">-Name</span></span>
<span data-ttu-id="8de01-117">이 cmdlet이 제거 하는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8de01-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8de01-118">-RouteTable</span></span>
<span data-ttu-id="8de01-119">이 cmdlet이 삭제 하는 경로를 포함 하는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8de01-120">-확인</span><span class="sxs-lookup"><span data-stu-id="8de01-120">-Confirm</span></span>
<span data-ttu-id="8de01-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de01-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de01-122">-WhatIf</span></span>
<span data-ttu-id="8de01-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8de01-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de01-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de01-125">CommonParameters</span></span>
<span data-ttu-id="8de01-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8de01-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de01-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de01-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de01-128">입력</span><span class="sxs-lookup"><span data-stu-id="8de01-128">INPUTS</span></span>

### <span data-ttu-id="8de01-129">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8de01-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="8de01-130">출력</span><span class="sxs-lookup"><span data-stu-id="8de01-130">OUTPUTS</span></span>

### <span data-ttu-id="8de01-131">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8de01-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="8de01-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8de01-132">NOTES</span></span>

## <span data-ttu-id="8de01-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8de01-133">RELATED LINKS</span></span>

[<span data-ttu-id="8de01-134">추가-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8de01-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="8de01-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8de01-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="8de01-136">새로운 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8de01-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="8de01-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8de01-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


