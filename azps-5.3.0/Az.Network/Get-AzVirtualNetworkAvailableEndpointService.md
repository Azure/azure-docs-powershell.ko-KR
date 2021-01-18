---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495547"
---
# <span data-ttu-id="2250e-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="2250e-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="2250e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2250e-102">SYNOPSIS</span></span>
<span data-ttu-id="2250e-103">위치에 사용 가능한 엔드포인트 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2250e-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="2250e-104">구문</span><span class="sxs-lookup"><span data-stu-id="2250e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2250e-105">설명</span><span class="sxs-lookup"><span data-stu-id="2250e-105">DESCRIPTION</span></span>
<span data-ttu-id="2250e-106">Get-AzVirtualNetworkAvailableEndpointService 지정된 위치에서 사용할 수 있는 엔드포인트 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2250e-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="2250e-107">예제</span><span class="sxs-lookup"><span data-stu-id="2250e-107">EXAMPLES</span></span>

### <span data-ttu-id="2250e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2250e-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="2250e-109">westus 지역에서 사용 가능한 엔드포인트 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2250e-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="2250e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2250e-110">PARAMETERS</span></span>

### <span data-ttu-id="2250e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2250e-111">-DefaultProfile</span></span>
<span data-ttu-id="2250e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2250e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2250e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2250e-113">-Location</span></span>
<span data-ttu-id="2250e-114">엔드포인트 서비스를 검색할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2250e-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="2250e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2250e-115">CommonParameters</span></span>
<span data-ttu-id="2250e-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2250e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2250e-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2250e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2250e-118">입력</span><span class="sxs-lookup"><span data-stu-id="2250e-118">INPUTS</span></span>

### <span data-ttu-id="2250e-119">System.String</span><span class="sxs-lookup"><span data-stu-id="2250e-119">System.String</span></span>

## <span data-ttu-id="2250e-120">출력</span><span class="sxs-lookup"><span data-stu-id="2250e-120">OUTPUTS</span></span>

### <span data-ttu-id="2250e-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="2250e-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="2250e-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2250e-122">NOTES</span></span>

## <span data-ttu-id="2250e-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2250e-123">RELATED LINKS</span></span>
