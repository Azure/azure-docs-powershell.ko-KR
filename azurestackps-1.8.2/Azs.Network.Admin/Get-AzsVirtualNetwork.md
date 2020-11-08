---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046963"
---
# <span data-ttu-id="cafa9-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cafa9-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="cafa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cafa9-102">SYNOPSIS</span></span>
<span data-ttu-id="cafa9-103">모든 가상 네트워크 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="cafa9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cafa9-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="cafa9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cafa9-105">DESCRIPTION</span></span>
<span data-ttu-id="cafa9-106">모든 가상 네트워크 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="cafa9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cafa9-107">EXAMPLES</span></span>

### <span data-ttu-id="cafa9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cafa9-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="cafa9-109">Azure 스택 스탬프에 대 한 가상 네트워크 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="cafa9-110">변수</span><span class="sxs-lookup"><span data-stu-id="cafa9-110">PARAMETERS</span></span>

### <span data-ttu-id="cafa9-111">-필터</span><span class="sxs-lookup"><span data-stu-id="cafa9-111">-Filter</span></span>
<span data-ttu-id="cafa9-112">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafa9-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="cafa9-113">-OrderBy</span></span>
<span data-ttu-id="cafa9-114">OData orderBy 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="cafa9-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafa9-115">-생략</span><span class="sxs-lookup"><span data-stu-id="cafa9-115">-Skip</span></span>
<span data-ttu-id="cafa9-116">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafa9-117">-위쪽</span><span class="sxs-lookup"><span data-stu-id="cafa9-117">-Top</span></span>
<span data-ttu-id="cafa9-118">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cafa9-119">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafa9-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="cafa9-120">-InlineCount</span></span>
<span data-ttu-id="cafa9-121">OData 인라인 개수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafa9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafa9-122">CommonParameters</span></span>
<span data-ttu-id="cafa9-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cafa9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafa9-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cafa9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafa9-125">입력</span><span class="sxs-lookup"><span data-stu-id="cafa9-125">INPUTS</span></span>

## <span data-ttu-id="cafa9-126">출력</span><span class="sxs-lookup"><span data-stu-id="cafa9-126">OUTPUTS</span></span>

### <span data-ttu-id="cafa9-127">VirtualNetwork. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="cafa9-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="cafa9-128">상속자</span><span class="sxs-lookup"><span data-stu-id="cafa9-128">NOTES</span></span>

## <span data-ttu-id="cafa9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cafa9-129">RELATED LINKS</span></span>
