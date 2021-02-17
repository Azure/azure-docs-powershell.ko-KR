---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: bd419d3b6ec55af885a0f05b7be5c5de269fccdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193345"
---
# <span data-ttu-id="5b549-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b549-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="5b549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b549-102">SYNOPSIS</span></span>
<span data-ttu-id="5b549-103">경로 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-103">Updates a route table.</span></span>

## <span data-ttu-id="5b549-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b549-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b549-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b549-105">DESCRIPTION</span></span>
<span data-ttu-id="5b549-106">**Set-AzRouteTable** cmdlet은 경로 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="5b549-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b549-107">EXAMPLES</span></span>

### <span data-ttu-id="5b549-108">예제 1: 경로 구성을 추가하여 경로 테이블 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b549-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
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

<span data-ttu-id="5b549-109">이 명령은 Get-AzRouteTable cmdlet을 사용하여 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="5b549-110">이 명령은 파이프라인 연산자를 사용하여 Add-AzRouteConfig cmdlet에 테이블을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b549-111">**Add-AzRouteConfig는** Route07이라는 경로를 추가한 다음 결과를 현재 cmdlet에 전달하여 변경 내용을 반영하기 위해 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="5b549-112">예제 2: 경로 테이블 수정</span><span class="sxs-lookup"><span data-stu-id="5b549-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="5b549-113">첫 번째 명령은 rtName이라는 경로 테이블을 사용하여 $rt 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="5b549-114">두 번째 명령은 DisableBgpRoutePropagation의 값을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="5b549-115">세 번째 명령은 DisableBgpRoutePropagation의 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="5b549-116">네 번째 명령은 서버의 경로 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="5b549-117">다섯 번째 명령은 업데이트된 경로 테이블을 다운로드하여 $rt 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="5b549-118">여섯 번째 명령은 DisableBgpRoutePropagation의 값을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="5b549-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b549-119">PARAMETERS</span></span>

### <span data-ttu-id="5b549-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b549-120">-AsJob</span></span>
<span data-ttu-id="5b549-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b549-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b549-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b549-122">-DefaultProfile</span></span>
<span data-ttu-id="5b549-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b549-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5b549-124">-RouteTable</span></span>
<span data-ttu-id="5b549-125">경로 테이블을 설정해야 하는 상태를 나타내는 경로 테이블 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

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

### <span data-ttu-id="5b549-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b549-126">-Confirm</span></span>
<span data-ttu-id="5b549-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b549-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b549-128">-WhatIf</span></span>
<span data-ttu-id="5b549-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b549-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b549-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b549-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b549-131">CommonParameters</span></span>
<span data-ttu-id="5b549-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b549-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b549-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b549-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b549-134">입력</span><span class="sxs-lookup"><span data-stu-id="5b549-134">INPUTS</span></span>

### <span data-ttu-id="5b549-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b549-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5b549-136">출력</span><span class="sxs-lookup"><span data-stu-id="5b549-136">OUTPUTS</span></span>

### <span data-ttu-id="5b549-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b549-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5b549-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b549-138">NOTES</span></span>

## <span data-ttu-id="5b549-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b549-139">RELATED LINKS</span></span>

[<span data-ttu-id="5b549-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5b549-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="5b549-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b549-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="5b549-142">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b549-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="5b549-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b549-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


