---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045204"
---
# <span data-ttu-id="a8e0c-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="a8e0c-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="a8e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e0c-103">공용 ip 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-103">List of public ip addresses.</span></span>

## <span data-ttu-id="a8e0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8e0c-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a8e0c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a8e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e0c-106">공용 ip 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-106">List of public ip addresses.</span></span>

## <span data-ttu-id="a8e0c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a8e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="a8e0c-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8e0c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="a8e0c-109">할당 되거나 할당 되지 않은 공용 ip 주소 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="a8e0c-110">변수</span><span class="sxs-lookup"><span data-stu-id="a8e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="a8e0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e0c-111">-DefaultProfile</span></span>
<span data-ttu-id="a8e0c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8e0c-113">-필터</span><span class="sxs-lookup"><span data-stu-id="a8e0c-113">-Filter</span></span>
<span data-ttu-id="a8e0c-114">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-114">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8e0c-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="a8e0c-115">-InlineCount</span></span>
<span data-ttu-id="a8e0c-116">OData 인라인 개수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-116">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8e0c-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="a8e0c-117">-OrderBy</span></span>
<span data-ttu-id="a8e0c-118">OData orderBy 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-118">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8e0c-119">-생략</span><span class="sxs-lookup"><span data-stu-id="a8e0c-119">-Skip</span></span>
<span data-ttu-id="a8e0c-120">OData skip 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-120">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8e0c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8e0c-121">-SubscriptionId</span></span>
<span data-ttu-id="a8e0c-122">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a8e0c-123">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8e0c-124">-위쪽</span><span class="sxs-lookup"><span data-stu-id="a8e0c-124">-Top</span></span>
<span data-ttu-id="a8e0c-125">OData top 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-125">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a8e0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e0c-126">CommonParameters</span></span>
<span data-ttu-id="a8e0c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e0c-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e0c-129">입력</span><span class="sxs-lookup"><span data-stu-id="a8e0c-129">INPUTS</span></span>

## <span data-ttu-id="a8e0c-130">출력</span><span class="sxs-lookup"><span data-stu-id="a8e0c-130">OUTPUTS</span></span>

### <span data-ttu-id="a8e0c-131">Api20150615. IPublicIPAddress에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="a8e0c-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="a8e0c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a8e0c-132">NOTES</span></span>

## <span data-ttu-id="a8e0c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8e0c-133">RELATED LINKS</span></span>

