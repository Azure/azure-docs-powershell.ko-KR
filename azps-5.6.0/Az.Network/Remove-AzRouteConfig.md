---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: e48da3a5f300d39051a9d1b07e9789855ed7dca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996123"
---
# <span data-ttu-id="ad999-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ad999-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="ad999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad999-102">SYNOPSIS</span></span>
<span data-ttu-id="ad999-103">경로 테이블에서 경로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="ad999-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad999-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad999-105">설명</span><span class="sxs-lookup"><span data-stu-id="ad999-105">DESCRIPTION</span></span>
<span data-ttu-id="ad999-106">**Remove-AzRouteConfig** cmdlet은 Azure 경로 테이블에서 경로를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="ad999-107">예제</span><span class="sxs-lookup"><span data-stu-id="ad999-107">EXAMPLES</span></span>

### <span data-ttu-id="ad999-108">예제 1: 경로 제거</span><span class="sxs-lookup"><span data-stu-id="ad999-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="ad999-109">이 명령은 **Get-AzRouteTable** cmdlet을 사용하여 RouteTable01이라는 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="ad999-110">명령은 파이프라인 연산자를 사용하여 현재 cmdlet에 테이블을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ad999-111">현재 cmdlet은 Route02라는 경로를 제거하고 결과를 **Set-AzRouteTable** cmdlet에 전달하여 변경 내용을 반영하기 위해 표를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="ad999-112">테이블에 Route02라는 경로가 더 이상 포함되어 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="ad999-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ad999-113">PARAMETERS</span></span>

### <span data-ttu-id="ad999-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad999-114">-DefaultProfile</span></span>
<span data-ttu-id="ad999-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad999-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ad999-116">-Name</span></span>
<span data-ttu-id="ad999-117">이 cmdlet이 제거하는 경로의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad999-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ad999-118">-RouteTable</span></span>
<span data-ttu-id="ad999-119">이 cmdlet이 삭제하는 경로를 포함하는 경로 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ad999-120">-확인</span><span class="sxs-lookup"><span data-stu-id="ad999-120">-Confirm</span></span>
<span data-ttu-id="ad999-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad999-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad999-122">-WhatIf</span></span>
<span data-ttu-id="ad999-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad999-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad999-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad999-125">CommonParameters</span></span>
<span data-ttu-id="ad999-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad999-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad999-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ad999-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad999-128">입력</span><span class="sxs-lookup"><span data-stu-id="ad999-128">INPUTS</span></span>

### <span data-ttu-id="ad999-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad999-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ad999-130">출력</span><span class="sxs-lookup"><span data-stu-id="ad999-130">OUTPUTS</span></span>

### <span data-ttu-id="ad999-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad999-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ad999-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad999-132">NOTES</span></span>

## <span data-ttu-id="ad999-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad999-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad999-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ad999-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="ad999-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ad999-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="ad999-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ad999-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="ad999-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ad999-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


