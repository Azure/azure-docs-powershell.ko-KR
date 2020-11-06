---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536271"
---
# <span data-ttu-id="95b09-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b09-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="95b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95b09-102">SYNOPSIS</span></span>
<span data-ttu-id="95b09-103">경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95b09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95b09-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95b09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95b09-105">DESCRIPTION</span></span>
<span data-ttu-id="95b09-106">**AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="95b09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95b09-107">EXAMPLES</span></span>

### <span data-ttu-id="95b09-108">예제 1: 경로 제거</span><span class="sxs-lookup"><span data-stu-id="95b09-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="95b09-109">이 명령은 **AzureRmRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="95b09-110">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95b09-111">현재 cmdlet은 Route02 이라는 경로를 제거 하 고 해당 결과를 **AzureRmRouteTable** cmdlet에 전달 하 여 변경 내용을 반영 하도록 테이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="95b09-112">표에 Route02 이라는 경로가 더 이상 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="95b09-113">변수</span><span class="sxs-lookup"><span data-stu-id="95b09-113">PARAMETERS</span></span>

### <span data-ttu-id="95b09-114">-이름</span><span class="sxs-lookup"><span data-stu-id="95b09-114">-Name</span></span>
<span data-ttu-id="95b09-115">이 cmdlet이 제거 하는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-115">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b09-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="95b09-116">-RouteTable</span></span>
<span data-ttu-id="95b09-117">이 cmdlet이 삭제 하는 경로를 포함 하는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="95b09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b09-118">-DefaultProfile</span></span>
<span data-ttu-id="95b09-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b09-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b09-120">CommonParameters</span></span>
<span data-ttu-id="95b09-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b09-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b09-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b09-123">입력</span><span class="sxs-lookup"><span data-stu-id="95b09-123">INPUTS</span></span>

### <span data-ttu-id="95b09-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="95b09-124">PSRouteTable</span></span>
<span data-ttu-id="95b09-125">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b09-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="95b09-126">출력</span><span class="sxs-lookup"><span data-stu-id="95b09-126">OUTPUTS</span></span>

### <span data-ttu-id="95b09-127">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="95b09-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="95b09-128">상속자</span><span class="sxs-lookup"><span data-stu-id="95b09-128">NOTES</span></span>

## <span data-ttu-id="95b09-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95b09-129">RELATED LINKS</span></span>

[<span data-ttu-id="95b09-130">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b09-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="95b09-131">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b09-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="95b09-132">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b09-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="95b09-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b09-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


