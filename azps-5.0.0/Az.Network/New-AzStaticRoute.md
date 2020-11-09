---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309506"
---
# <span data-ttu-id="effaf-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="effaf-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="effaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="effaf-102">SYNOPSIS</span></span>
<span data-ttu-id="effaf-103">RoutingConfiguration 개체에 추가할 수 있는 StaticRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="effaf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="effaf-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="effaf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="effaf-105">DESCRIPTION</span></span>
<span data-ttu-id="effaf-106">StaticRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="effaf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="effaf-107">EXAMPLES</span></span>

### <span data-ttu-id="effaf-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="effaf-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="effaf-109">위 명령에서는 RoutingConfiguration 개체에 추가할 수 있는 StaticRoute 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="effaf-110">변수</span><span class="sxs-lookup"><span data-stu-id="effaf-110">PARAMETERS</span></span>

### <span data-ttu-id="effaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="effaf-111">-DefaultProfile</span></span>
<span data-ttu-id="effaf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effaf-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="effaf-113">-AddressPrefix</span></span>
<span data-ttu-id="effaf-114">주소 접두사 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effaf-115">-이름</span><span class="sxs-lookup"><span data-stu-id="effaf-115">-Name</span></span>
<span data-ttu-id="effaf-116">경로 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effaf-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="effaf-117">-NextHopIpAddress</span></span>
<span data-ttu-id="effaf-118">다음 홉 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-118">The next hop ip address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effaf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="effaf-119">CommonParameters</span></span>
<span data-ttu-id="effaf-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="effaf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="effaf-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="effaf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="effaf-122">입력</span><span class="sxs-lookup"><span data-stu-id="effaf-122">INPUTS</span></span>

### <span data-ttu-id="effaf-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="effaf-123">System.String</span></span>

## <span data-ttu-id="effaf-124">출력</span><span class="sxs-lookup"><span data-stu-id="effaf-124">OUTPUTS</span></span>

### <span data-ttu-id="effaf-125">Microsoft. 네트워크 모델. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="effaf-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="effaf-126">상속자</span><span class="sxs-lookup"><span data-stu-id="effaf-126">NOTES</span></span>

## <span data-ttu-id="effaf-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="effaf-127">RELATED LINKS</span></span>

[<span data-ttu-id="effaf-128">새로운 AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="effaf-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
