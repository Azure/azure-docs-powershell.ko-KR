---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711340"
---
# <span data-ttu-id="a7965-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="a7965-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="a7965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7965-102">SYNOPSIS</span></span>
<span data-ttu-id="a7965-103">ExpressRoutePort 리소스를 사용할 수 있는 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7965-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7965-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7965-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7965-105">DESCRIPTION</span></span>
<span data-ttu-id="a7965-106">**AzureRmExpressRoutePortsLocation** Cmdlet은 ExpressRoutePort 리소스를 사용할 수 있는 위치를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="a7965-107">특정 위치를 입력으로 제공 하면 cmdlet은 해당 위치의 세부 정보, 즉 해당 위치의 사용 가능한 대역폭 목록 등을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="a7965-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a7965-108">EXAMPLES</span></span>

### <span data-ttu-id="a7965-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a7965-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="a7965-110">ExpressRoutePort 리소스를 사용할 수 있는 위치를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="a7965-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="a7965-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="a7965-112">$Loc 위치에서 사용할 수 있는 ExpressRoutePort 대역폭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="a7965-113">변수</span><span class="sxs-lookup"><span data-stu-id="a7965-113">PARAMETERS</span></span>

### <span data-ttu-id="a7965-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7965-114">-DefaultProfile</span></span>
<span data-ttu-id="a7965-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7965-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="a7965-116">-LocationName</span></span>
<span data-ttu-id="a7965-117">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7965-118">CommonParameters</span></span>
<span data-ttu-id="a7965-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7965-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7965-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7965-121">입력</span><span class="sxs-lookup"><span data-stu-id="a7965-121">INPUTS</span></span>

### <span data-ttu-id="a7965-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7965-122">System.String</span></span>

## <span data-ttu-id="a7965-123">출력</span><span class="sxs-lookup"><span data-stu-id="a7965-123">OUTPUTS</span></span>

### <span data-ttu-id="a7965-124">PSExpressRoutePortsLocation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a7965-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="a7965-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a7965-125">NOTES</span></span>

## <span data-ttu-id="a7965-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7965-126">RELATED LINKS</span></span>
