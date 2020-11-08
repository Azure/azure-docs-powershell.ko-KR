---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204501"
---
# <span data-ttu-id="211d6-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="211d6-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="211d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="211d6-102">SYNOPSIS</span></span>
<span data-ttu-id="211d6-103">위치에 사용할 수 있는 끝점 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="211d6-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="211d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="211d6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="211d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="211d6-105">DESCRIPTION</span></span>
<span data-ttu-id="211d6-106">Get-AzVirtualNetworkAvailableEndpointService는 지정 된 위치에서 사용할 수 있는 끝점 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="211d6-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="211d6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="211d6-107">EXAMPLES</span></span>

### <span data-ttu-id="211d6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="211d6-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="211d6-109">Westus 지역에서 사용할 수 있는 끝점 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="211d6-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="211d6-110">변수</span><span class="sxs-lookup"><span data-stu-id="211d6-110">PARAMETERS</span></span>

### <span data-ttu-id="211d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211d6-111">-DefaultProfile</span></span>
<span data-ttu-id="211d6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="211d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="211d6-113">-위치</span><span class="sxs-lookup"><span data-stu-id="211d6-113">-Location</span></span>
<span data-ttu-id="211d6-114">끝점 서비스를 검색할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="211d6-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="211d6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211d6-115">CommonParameters</span></span>
<span data-ttu-id="211d6-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="211d6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211d6-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="211d6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211d6-118">입력</span><span class="sxs-lookup"><span data-stu-id="211d6-118">INPUTS</span></span>

### <span data-ttu-id="211d6-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="211d6-119">System.String</span></span>

## <span data-ttu-id="211d6-120">출력</span><span class="sxs-lookup"><span data-stu-id="211d6-120">OUTPUTS</span></span>

### <span data-ttu-id="211d6-121">PSEndpointServiceResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="211d6-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="211d6-122">상속자</span><span class="sxs-lookup"><span data-stu-id="211d6-122">NOTES</span></span>

## <span data-ttu-id="211d6-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="211d6-123">RELATED LINKS</span></span>
