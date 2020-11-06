---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2580e2b6de179cdc3a9407b514848cc832e798e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522991"
---
# <span data-ttu-id="1762d-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="1762d-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="1762d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1762d-102">SYNOPSIS</span></span>
<span data-ttu-id="1762d-103">플랫폼 이미지 리포지토리에 로드 된 가상 컴퓨터 이미지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="1762d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1762d-104">SYNTAX</span></span>

### <span data-ttu-id="1762d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1762d-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1762d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1762d-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1762d-107">리소스</span><span class="sxs-lookup"><span data-stu-id="1762d-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1762d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1762d-108">DESCRIPTION</span></span>
<span data-ttu-id="1762d-109">플랫폼 이미지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-109">Returns platform images.</span></span>

## <span data-ttu-id="1762d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1762d-110">EXAMPLES</span></span>

### <span data-ttu-id="1762d-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1762d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="1762d-112">위치 로컬에서 플랫폼 이미지 리포지토리에 로드 된 가상 컴퓨터 이미지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="1762d-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1762d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="1762d-114">특정 플랫폼 이미지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-114">Get a specific platform image.</span></span>

## <span data-ttu-id="1762d-115">변수</span><span class="sxs-lookup"><span data-stu-id="1762d-115">PARAMETERS</span></span>

### <span data-ttu-id="1762d-116">-위치</span><span class="sxs-lookup"><span data-stu-id="1762d-116">-Location</span></span>
<span data-ttu-id="1762d-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-117">Location of the resource.</span></span>

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

### <span data-ttu-id="1762d-118">-제공</span><span class="sxs-lookup"><span data-stu-id="1762d-118">-Offer</span></span>
<span data-ttu-id="1762d-119">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-119">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="1762d-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1762d-120">-Publisher</span></span>
<span data-ttu-id="1762d-121">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-121">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="1762d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1762d-122">-ResourceId</span></span>
<span data-ttu-id="1762d-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1762d-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="1762d-124">-Sku</span></span>
<span data-ttu-id="1762d-125">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-125">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="1762d-126">-버전</span><span class="sxs-lookup"><span data-stu-id="1762d-126">-Version</span></span>
<span data-ttu-id="1762d-127">플랫폼 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="1762d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1762d-128">CommonParameters</span></span>
<span data-ttu-id="1762d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1762d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1762d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1762d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1762d-131">입력</span><span class="sxs-lookup"><span data-stu-id="1762d-131">INPUTS</span></span>

## <span data-ttu-id="1762d-132">출력</span><span class="sxs-lookup"><span data-stu-id="1762d-132">OUTPUTS</span></span>

### <span data-ttu-id="1762d-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="1762d-133">PlatformImageObject</span></span>

## <span data-ttu-id="1762d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="1762d-134">NOTES</span></span>

## <span data-ttu-id="1762d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1762d-135">RELATED LINKS</span></span>

