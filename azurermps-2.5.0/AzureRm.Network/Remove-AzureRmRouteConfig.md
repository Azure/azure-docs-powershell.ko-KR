---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: c5117fc961a93395991055eff2d404b5b8c6c051
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882853"
---
# <span data-ttu-id="1ac17-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac17-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="1ac17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ac17-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac17-103">경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ac17-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac17-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ac17-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac17-106">**AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="1ac17-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1ac17-107">EXAMPLES</span></span>

### <span data-ttu-id="1ac17-108">예제 1: 경로 제거</span><span class="sxs-lookup"><span data-stu-id="1ac17-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
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

<span data-ttu-id="1ac17-109">이 명령은 **AzureRmRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="1ac17-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1ac17-111">현재 cmdlet은 Route02 이라는 경로를 제거 하 고 해당 결과를 **AzureRmRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 테이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="1ac17-112">표에 Route02 이라는 경로가 더 이상 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="1ac17-113">변수</span><span class="sxs-lookup"><span data-stu-id="1ac17-113">PARAMETERS</span></span>

### <span data-ttu-id="1ac17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac17-114">-DefaultProfile</span></span>
<span data-ttu-id="1ac17-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ac17-116">-이름</span><span class="sxs-lookup"><span data-stu-id="1ac17-116">-Name</span></span>
<span data-ttu-id="1ac17-117">이 cmdlet이 제거 하는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-117">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac17-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1ac17-118">-RouteTable</span></span>
<span data-ttu-id="1ac17-119">이 cmdlet이 삭제 하는 경로를 포함 하는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac17-120">-확인</span><span class="sxs-lookup"><span data-stu-id="1ac17-120">-Confirm</span></span>
<span data-ttu-id="1ac17-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac17-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac17-122">-WhatIf</span></span>
<span data-ttu-id="1ac17-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ac17-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac17-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac17-125">CommonParameters</span></span>
<span data-ttu-id="1ac17-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac17-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac17-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac17-128">입력</span><span class="sxs-lookup"><span data-stu-id="1ac17-128">INPUTS</span></span>

### <span data-ttu-id="1ac17-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ac17-129">PSRouteTable</span></span>
<span data-ttu-id="1ac17-130">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac17-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="1ac17-131">출력</span><span class="sxs-lookup"><span data-stu-id="1ac17-131">OUTPUTS</span></span>

### <span data-ttu-id="1ac17-132">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1ac17-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1ac17-133">상속자</span><span class="sxs-lookup"><span data-stu-id="1ac17-133">NOTES</span></span>

## <span data-ttu-id="1ac17-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ac17-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ac17-135">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac17-135">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="1ac17-136">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac17-136">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="1ac17-137">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac17-137">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="1ac17-138">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1ac17-138">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


