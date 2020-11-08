---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046913"
---
# <span data-ttu-id="3989e-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="3989e-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="3989e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3989e-102">SYNOPSIS</span></span>
<span data-ttu-id="3989e-103">저장소 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3989e-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3989e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3989e-104">SYNTAX</span></span>

### <span data-ttu-id="3989e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3989e-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3989e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="3989e-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3989e-107">리소스</span><span class="sxs-lookup"><span data-stu-id="3989e-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3989e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3989e-108">DESCRIPTION</span></span>
<span data-ttu-id="3989e-109">저장소 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3989e-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3989e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3989e-110">EXAMPLES</span></span>

### <span data-ttu-id="3989e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3989e-111">EXAMPLE 1</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="3989e-112">저장소 공유 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3989e-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="3989e-113">변수</span><span class="sxs-lookup"><span data-stu-id="3989e-113">PARAMETERS</span></span>

### <span data-ttu-id="3989e-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="3989e-114">-FarmName</span></span>
<span data-ttu-id="3989e-115">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3989e-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3989e-116">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3989e-116">-ShareName</span></span>
<span data-ttu-id="3989e-117">공유 이름.</span><span class="sxs-lookup"><span data-stu-id="3989e-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3989e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3989e-118">-ResourceGroupName</span></span>
<span data-ttu-id="3989e-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3989e-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3989e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3989e-120">-ResourceId</span></span>
<span data-ttu-id="3989e-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3989e-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3989e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3989e-122">CommonParameters</span></span>
<span data-ttu-id="3989e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3989e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3989e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3989e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3989e-125">입력</span><span class="sxs-lookup"><span data-stu-id="3989e-125">INPUTS</span></span>

## <span data-ttu-id="3989e-126">출력</span><span class="sxs-lookup"><span data-stu-id="3989e-126">OUTPUTS</span></span>

### <span data-ttu-id="3989e-127">Microsoft AzureStack. 관리. 모델 공유</span><span class="sxs-lookup"><span data-stu-id="3989e-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="3989e-128">상속자</span><span class="sxs-lookup"><span data-stu-id="3989e-128">NOTES</span></span>

## <span data-ttu-id="3989e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3989e-129">RELATED LINKS</span></span>
