---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875529"
---
# <span data-ttu-id="13a54-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="13a54-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="13a54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a54-102">SYNOPSIS</span></span>
<span data-ttu-id="13a54-103">경로 테이블에서 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="13a54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13a54-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13a54-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13a54-105">DESCRIPTION</span></span>
<span data-ttu-id="13a54-106">**AzRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="13a54-107">이름을 기준으로 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-107">You can specify a route by name.</span></span>

## <span data-ttu-id="13a54-108">예제의</span><span class="sxs-lookup"><span data-stu-id="13a54-108">EXAMPLES</span></span>

### <span data-ttu-id="13a54-109">예제 1: 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="13a54-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="13a54-110">이 명령은 **AzRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="13a54-111">이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13a54-112">현재 cmdlet는 RouteTable01 이라는 경로 테이블에서 Route07 이라는 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="13a54-113">변수</span><span class="sxs-lookup"><span data-stu-id="13a54-113">PARAMETERS</span></span>

### <span data-ttu-id="13a54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a54-114">-DefaultProfile</span></span>
<span data-ttu-id="13a54-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13a54-116">-이름</span><span class="sxs-lookup"><span data-stu-id="13a54-116">-Name</span></span>
<span data-ttu-id="13a54-117">이 cmdlet이 가져오는 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="13a54-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="13a54-118">-RouteTable</span></span>
<span data-ttu-id="13a54-119">이 cmdlet이 경로를 가져오는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="13a54-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a54-120">CommonParameters</span></span>
<span data-ttu-id="13a54-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a54-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a54-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a54-123">입력</span><span class="sxs-lookup"><span data-stu-id="13a54-123">INPUTS</span></span>

### <span data-ttu-id="13a54-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="13a54-124">PSRouteTable</span></span>
<span data-ttu-id="13a54-125">' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a54-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="13a54-126">출력</span><span class="sxs-lookup"><span data-stu-id="13a54-126">OUTPUTS</span></span>

### <span data-ttu-id="13a54-127">Microsoft. 네트워크 모델. PSRoute</span><span class="sxs-lookup"><span data-stu-id="13a54-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="13a54-128">상속자</span><span class="sxs-lookup"><span data-stu-id="13a54-128">NOTES</span></span>

## <span data-ttu-id="13a54-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13a54-129">RELATED LINKS</span></span>

[<span data-ttu-id="13a54-130">추가-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="13a54-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="13a54-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="13a54-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="13a54-132">새로운 AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="13a54-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="13a54-133">제거-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="13a54-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="13a54-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="13a54-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


