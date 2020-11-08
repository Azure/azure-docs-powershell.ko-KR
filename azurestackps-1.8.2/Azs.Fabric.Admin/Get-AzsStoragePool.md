---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047015"
---
# <span data-ttu-id="6ea50-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="6ea50-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="6ea50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea50-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea50-103">위치에 대 한 모든 저장소 풀의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="6ea50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ea50-104">SYNTAX</span></span>

### <span data-ttu-id="6ea50-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ea50-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6ea50-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6ea50-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ea50-107">리소스</span><span class="sxs-lookup"><span data-stu-id="6ea50-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6ea50-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ea50-108">DESCRIPTION</span></span>
<span data-ttu-id="6ea50-109">위치에 대 한 모든 저장소 풀의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="6ea50-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ea50-110">EXAMPLES</span></span>

### <span data-ttu-id="6ea50-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ea50-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="6ea50-112">지정 된 위치에서 모든 저장소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="6ea50-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6ea50-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="6ea50-114">저장소 풀 이름을 지정 된 위치에서 저장소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="6ea50-115">변수</span><span class="sxs-lookup"><span data-stu-id="6ea50-115">PARAMETERS</span></span>

### <span data-ttu-id="6ea50-116">-이름</span><span class="sxs-lookup"><span data-stu-id="6ea50-116">-Name</span></span>
<span data-ttu-id="6ea50-117">저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-117">Storage pool name.</span></span>

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

### <span data-ttu-id="6ea50-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="6ea50-118">-StorageSystem</span></span>
<span data-ttu-id="6ea50-119">저장소 하위 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="6ea50-120">-위치</span><span class="sxs-lookup"><span data-stu-id="6ea50-120">-Location</span></span>
<span data-ttu-id="6ea50-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-121">Location of the resource.</span></span>

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

### <span data-ttu-id="6ea50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea50-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ea50-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6ea50-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ea50-124">-ResourceId</span></span>
<span data-ttu-id="6ea50-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-125">The resource id.</span></span>

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

### <span data-ttu-id="6ea50-126">-필터</span><span class="sxs-lookup"><span data-stu-id="6ea50-126">-Filter</span></span>
<span data-ttu-id="6ea50-127">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="6ea50-128">-생략</span><span class="sxs-lookup"><span data-stu-id="6ea50-128">-Skip</span></span>
<span data-ttu-id="6ea50-129">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6ea50-130">-위쪽</span><span class="sxs-lookup"><span data-stu-id="6ea50-130">-Top</span></span>
<span data-ttu-id="6ea50-131">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6ea50-132">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6ea50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea50-133">CommonParameters</span></span>
<span data-ttu-id="6ea50-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea50-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea50-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea50-136">입력</span><span class="sxs-lookup"><span data-stu-id="6ea50-136">INPUTS</span></span>

## <span data-ttu-id="6ea50-137">출력</span><span class="sxs-lookup"><span data-stu-id="6ea50-137">OUTPUTS</span></span>

### <span data-ttu-id="6ea50-138">Microsoft AzureStack. 관리. m. 관리자. 저장소 풀</span><span class="sxs-lookup"><span data-stu-id="6ea50-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="6ea50-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6ea50-139">NOTES</span></span>

## <span data-ttu-id="6ea50-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ea50-140">RELATED LINKS</span></span>
