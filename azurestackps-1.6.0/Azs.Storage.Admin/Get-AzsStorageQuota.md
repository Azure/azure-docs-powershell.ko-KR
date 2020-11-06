---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524076"
---
# <span data-ttu-id="4a9a9-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="4a9a9-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="4a9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9a9-103">지정 된 위치의 저장소 할당량 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="4a9a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a9a9-104">SYNTAX</span></span>

### <span data-ttu-id="4a9a9-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a9a9-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4a9a9-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4a9a9-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="4a9a9-107">리소스</span><span class="sxs-lookup"><span data-stu-id="4a9a9-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4a9a9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4a9a9-108">DESCRIPTION</span></span>
<span data-ttu-id="4a9a9-109">지정 된 위치의 저장소 할당량 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="4a9a9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4a9a9-110">EXAMPLES</span></span>

### <span data-ttu-id="4a9a9-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4a9a9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="4a9a9-112">저장소 할당량 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="4a9a9-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4a9a9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="4a9a9-114">이름으로 지정 된 저장소 할당량에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="4a9a9-115">변수</span><span class="sxs-lookup"><span data-stu-id="4a9a9-115">PARAMETERS</span></span>

### <span data-ttu-id="4a9a9-116">-위치</span><span class="sxs-lookup"><span data-stu-id="4a9a9-116">-Location</span></span>
<span data-ttu-id="4a9a9-117">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-117">Resource location.</span></span>

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

### <span data-ttu-id="4a9a9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4a9a9-118">-Name</span></span>
<span data-ttu-id="4a9a9-119">저장소 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-119">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9a9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a9a9-120">-ResourceId</span></span>
<span data-ttu-id="4a9a9-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-121">The resource id.</span></span>

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

### <span data-ttu-id="4a9a9-122">-생략</span><span class="sxs-lookup"><span data-stu-id="4a9a9-122">-Skip</span></span>
<span data-ttu-id="4a9a9-123">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9a9-124">-위쪽</span><span class="sxs-lookup"><span data-stu-id="4a9a9-124">-Top</span></span>
<span data-ttu-id="4a9a9-125">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4a9a9-126">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a9a9-127">CommonParameters</span></span>
<span data-ttu-id="4a9a9-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a9a9-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a9a9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a9a9-130">입력</span><span class="sxs-lookup"><span data-stu-id="4a9a9-130">INPUTS</span></span>

## <span data-ttu-id="4a9a9-131">출력</span><span class="sxs-lookup"><span data-stu-id="4a9a9-131">OUTPUTS</span></span>

### <span data-ttu-id="4a9a9-132">StorageQuota. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="4a9a9-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="4a9a9-133">상속자</span><span class="sxs-lookup"><span data-stu-id="4a9a9-133">NOTES</span></span>

## <span data-ttu-id="4a9a9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a9a9-134">RELATED LINKS</span></span>

