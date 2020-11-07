---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874356"
---
# <span data-ttu-id="291dd-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="291dd-101">Get-AzsDrive</span></span>

## <span data-ttu-id="291dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="291dd-102">SYNOPSIS</span></span>
<span data-ttu-id="291dd-103">지정 된 클러스터에 대 한 모든 저장소 드라이브의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="291dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="291dd-104">SYNTAX</span></span>

### <span data-ttu-id="291dd-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="291dd-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="291dd-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="291dd-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="291dd-107">리소스</span><span class="sxs-lookup"><span data-stu-id="291dd-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="291dd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="291dd-108">DESCRIPTION</span></span>
<span data-ttu-id="291dd-109">지정 된 클러스터에 대 한 모든 저장소 드라이브의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="291dd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="291dd-110">EXAMPLES</span></span>

### <span data-ttu-id="291dd-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="291dd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="291dd-112">지정 된 클러스터에 대 한 모든 저장소 드라이브의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="291dd-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="291dd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="291dd-114">주어진 클러스터에 대 한 이름으로 저장소 드라이브를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="291dd-115">변수</span><span class="sxs-lookup"><span data-stu-id="291dd-115">PARAMETERS</span></span>

### <span data-ttu-id="291dd-116">-필터</span><span class="sxs-lookup"><span data-stu-id="291dd-116">-Filter</span></span>
<span data-ttu-id="291dd-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="291dd-118">-위치</span><span class="sxs-lookup"><span data-stu-id="291dd-118">-Location</span></span>
<span data-ttu-id="291dd-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-119">Location of the resource.</span></span>

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

### <span data-ttu-id="291dd-120">-이름</span><span class="sxs-lookup"><span data-stu-id="291dd-120">-Name</span></span>
<span data-ttu-id="291dd-121">저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="291dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="291dd-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="291dd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="291dd-124">-ResourceId</span></span>
<span data-ttu-id="291dd-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-125">The resource id.</span></span>

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

### <span data-ttu-id="291dd-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="291dd-126">-ScaleUnit</span></span>
<span data-ttu-id="291dd-127">배율 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="291dd-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="291dd-128">-StorageSubSystem</span></span>
<span data-ttu-id="291dd-129">드라이브가 있는 저장소 하위 시스템.</span><span class="sxs-lookup"><span data-stu-id="291dd-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="291dd-130">-위쪽</span><span class="sxs-lookup"><span data-stu-id="291dd-130">-Top</span></span>
<span data-ttu-id="291dd-131">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="291dd-132">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="291dd-133">-생략</span><span class="sxs-lookup"><span data-stu-id="291dd-133">-Skip</span></span>
<span data-ttu-id="291dd-134">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="291dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291dd-135">CommonParameters</span></span>
<span data-ttu-id="291dd-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="291dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291dd-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="291dd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291dd-138">입력</span><span class="sxs-lookup"><span data-stu-id="291dd-138">INPUTS</span></span>

## <span data-ttu-id="291dd-139">출력</span><span class="sxs-lookup"><span data-stu-id="291dd-139">OUTPUTS</span></span>

### <span data-ttu-id="291dd-140">Microsoft AzureStack. 관리. 드라이브</span><span class="sxs-lookup"><span data-stu-id="291dd-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="291dd-141">상속자</span><span class="sxs-lookup"><span data-stu-id="291dd-141">NOTES</span></span>

## <span data-ttu-id="291dd-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="291dd-142">RELATED LINKS</span></span>
