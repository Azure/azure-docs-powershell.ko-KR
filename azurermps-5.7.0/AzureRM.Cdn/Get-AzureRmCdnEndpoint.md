---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527032"
---
# <span data-ttu-id="3163b-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3163b-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="3163b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3163b-102">SYNOPSIS</span></span>
<span data-ttu-id="3163b-103">CDN 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3163b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3163b-104">SYNTAX</span></span>

### <span data-ttu-id="3163b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3163b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3163b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3163b-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3163b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3163b-107">DESCRIPTION</span></span>
<span data-ttu-id="3163b-108">**AzureRMCdnEndpoint** CMDLET은 CDN (Azure Content Delivery Network) 끝점 및 연결 된 구성 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="3163b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3163b-109">EXAMPLES</span></span>

## <span data-ttu-id="3163b-110">변수</span><span class="sxs-lookup"><span data-stu-id="3163b-110">PARAMETERS</span></span>

### <span data-ttu-id="3163b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="3163b-111">-CdnProfile</span></span>
<span data-ttu-id="3163b-112">끝점이 속한 CDN 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3163b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3163b-113">-DefaultProfile</span></span>
<span data-ttu-id="3163b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3163b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3163b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3163b-115">-EndpointName</span></span>
<span data-ttu-id="3163b-116">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="3163b-117">끝점의 이름이 끝점의 호스트 이름이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="3163b-118">-/Profile</span><span class="sxs-lookup"><span data-stu-id="3163b-118">-ProfileName</span></span>
<span data-ttu-id="3163b-119">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3163b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3163b-120">-ResourceGroupName</span></span>
<span data-ttu-id="3163b-121">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3163b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3163b-122">CommonParameters</span></span>
<span data-ttu-id="3163b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3163b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3163b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3163b-125">입력</span><span class="sxs-lookup"><span data-stu-id="3163b-125">INPUTS</span></span>

### <span data-ttu-id="3163b-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="3163b-126">PSProfile</span></span>
<span data-ttu-id="3163b-127">' CdnProfile ' 매개 변수는 파이프라인에서 ' PSProfile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="3163b-128">출력</span><span class="sxs-lookup"><span data-stu-id="3163b-128">OUTPUTS</span></span>

###  
<span data-ttu-id="3163b-129">이 cmdlet은 endpoint 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3163b-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="3163b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="3163b-130">NOTES</span></span>

## <span data-ttu-id="3163b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3163b-131">RELATED LINKS</span></span>

[<span data-ttu-id="3163b-132">새로운 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3163b-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3163b-133">제거-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3163b-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3163b-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3163b-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3163b-135">시작-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3163b-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="3163b-136">중지-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3163b-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


