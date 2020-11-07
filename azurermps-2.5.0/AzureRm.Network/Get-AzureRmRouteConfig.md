---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 907ca017518304a38340e9539aa4e8faf4216d59
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882921"
---
# <span data-ttu-id="f45f2-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f45f2-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="f45f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f45f2-103">경로 테이블에서 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f45f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f45f2-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f45f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f45f2-105">DESCRIPTION</span></span>
<span data-ttu-id="f45f2-106">**AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="f45f2-107">이름을 기준으로 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-107">You can specify a route by name.</span></span>

## <span data-ttu-id="f45f2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f45f2-108">EXAMPLES</span></span>

### <span data-ttu-id="f45f2-109">예제 1: 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="f45f2-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="f45f2-110">이 명령은 **AzureRmRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="f45f2-111">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f45f2-112">현재 cmdlet는 RouteTable01 이라는 경로 테이블에서 Route07 이라는 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="f45f2-113">변수</span><span class="sxs-lookup"><span data-stu-id="f45f2-113">PARAMETERS</span></span>

### <span data-ttu-id="f45f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45f2-114">-DefaultProfile</span></span>
<span data-ttu-id="f45f2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f45f2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f45f2-116">-Name</span></span>
<span data-ttu-id="f45f2-117">이 cmdlet이 가져오는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f45f2-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="f45f2-118">-RouteTable</span></span>
<span data-ttu-id="f45f2-119">이 cmdlet이 경로를 가져오는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="f45f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45f2-120">CommonParameters</span></span>
<span data-ttu-id="f45f2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45f2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f45f2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45f2-123">입력</span><span class="sxs-lookup"><span data-stu-id="f45f2-123">INPUTS</span></span>

### <span data-ttu-id="f45f2-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="f45f2-124">PSRouteTable</span></span>
<span data-ttu-id="f45f2-125">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f45f2-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="f45f2-126">출력</span><span class="sxs-lookup"><span data-stu-id="f45f2-126">OUTPUTS</span></span>

### <span data-ttu-id="f45f2-127">Microsoft. 네트워크 모델. PSRoute</span><span class="sxs-lookup"><span data-stu-id="f45f2-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="f45f2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="f45f2-128">NOTES</span></span>

## <span data-ttu-id="f45f2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f45f2-129">RELATED LINKS</span></span>

[<span data-ttu-id="f45f2-130">추가-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f45f2-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="f45f2-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="f45f2-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="f45f2-132">새로운 AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f45f2-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="f45f2-133">제거-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f45f2-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="f45f2-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="f45f2-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


