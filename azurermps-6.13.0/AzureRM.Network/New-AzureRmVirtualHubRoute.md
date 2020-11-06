---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532423"
---
# <span data-ttu-id="97a28-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="97a28-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="97a28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a28-102">SYNOPSIS</span></span>
<span data-ttu-id="97a28-103">Azure 가상 허브 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97a28-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97a28-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="97a28-105">DESCRIPTION</span></span>
<span data-ttu-id="97a28-106">Azure 가상 허브 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97a28-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="97a28-107">예제의</span><span class="sxs-lookup"><span data-stu-id="97a28-107">EXAMPLES</span></span>

### <span data-ttu-id="97a28-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="97a28-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="97a28-109">위의 방법을 통해 가상 허브 경로 테이블에 포함할 수 있는 가상 허브 경로 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97a28-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="97a28-110">가상 허브 경로는 VirtualHubRouteTable 개체를 만드는 데 사용할 수 있는 메모리 내 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="97a28-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="97a28-111">변수</span><span class="sxs-lookup"><span data-stu-id="97a28-111">PARAMETERS</span></span>

### <span data-ttu-id="97a28-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="97a28-112">-AddressPrefix</span></span>
<span data-ttu-id="97a28-113">주소 접두사 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="97a28-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a28-114">-DefaultProfile</span></span>
<span data-ttu-id="97a28-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97a28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a28-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="97a28-116">-NextHopIpAddress</span></span>
<span data-ttu-id="97a28-117">다음 홉 IpAddress.</span><span class="sxs-lookup"><span data-stu-id="97a28-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="97a28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a28-118">CommonParameters</span></span>
<span data-ttu-id="97a28-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97a28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a28-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a28-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a28-121">입력</span><span class="sxs-lookup"><span data-stu-id="97a28-121">INPUTS</span></span>

### <span data-ttu-id="97a28-122">않아야</span><span class="sxs-lookup"><span data-stu-id="97a28-122">None</span></span>

## <span data-ttu-id="97a28-123">출력</span><span class="sxs-lookup"><span data-stu-id="97a28-123">OUTPUTS</span></span>

### <span data-ttu-id="97a28-124">PSVirtualHubRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="97a28-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="97a28-125">상속자</span><span class="sxs-lookup"><span data-stu-id="97a28-125">NOTES</span></span>

## <span data-ttu-id="97a28-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97a28-126">RELATED LINKS</span></span>
