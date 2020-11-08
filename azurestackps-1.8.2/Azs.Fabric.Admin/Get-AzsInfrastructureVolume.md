---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047130"
---
# <span data-ttu-id="241f2-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="241f2-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="241f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="241f2-102">SYNOPSIS</span></span>
<span data-ttu-id="241f2-103">위치에 있는 모든 저장소 볼륨의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="241f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="241f2-104">SYNTAX</span></span>

### <span data-ttu-id="241f2-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="241f2-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="241f2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="241f2-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="241f2-107">리소스</span><span class="sxs-lookup"><span data-stu-id="241f2-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="241f2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="241f2-108">DESCRIPTION</span></span>
<span data-ttu-id="241f2-109">위치에 있는 모든 저장소 볼륨의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="241f2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="241f2-110">EXAMPLES</span></span>

### <span data-ttu-id="241f2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="241f2-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="241f2-112">지정 된 위치에 있는 모든 저장소 볼륨의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="241f2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="241f2-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="241f2-114">지정 된 위치에서 이름으로 저장소 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="241f2-115">변수</span><span class="sxs-lookup"><span data-stu-id="241f2-115">PARAMETERS</span></span>

### <span data-ttu-id="241f2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="241f2-116">-Name</span></span>
<span data-ttu-id="241f2-117">저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="241f2-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="241f2-118">-StoragePool</span></span>
<span data-ttu-id="241f2-119">저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-119">Storage pool name.</span></span>

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

### <span data-ttu-id="241f2-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="241f2-120">-StorageSystem</span></span>
<span data-ttu-id="241f2-121">저장소 시스템 리소스의 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="241f2-122">-위치</span><span class="sxs-lookup"><span data-stu-id="241f2-122">-Location</span></span>
<span data-ttu-id="241f2-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-123">Location of the resource.</span></span>

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

### <span data-ttu-id="241f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="241f2-125">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="241f2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="241f2-126">-ResourceId</span></span>
<span data-ttu-id="241f2-127">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-127">The resource id.</span></span>

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

### <span data-ttu-id="241f2-128">-필터</span><span class="sxs-lookup"><span data-stu-id="241f2-128">-Filter</span></span>
<span data-ttu-id="241f2-129">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="241f2-130">-생략</span><span class="sxs-lookup"><span data-stu-id="241f2-130">-Skip</span></span>
<span data-ttu-id="241f2-131">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="241f2-132">-위쪽</span><span class="sxs-lookup"><span data-stu-id="241f2-132">-Top</span></span>
<span data-ttu-id="241f2-133">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="241f2-134">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="241f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241f2-135">CommonParameters</span></span>
<span data-ttu-id="241f2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="241f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241f2-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241f2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241f2-138">입력</span><span class="sxs-lookup"><span data-stu-id="241f2-138">INPUTS</span></span>

## <span data-ttu-id="241f2-139">출력</span><span class="sxs-lookup"><span data-stu-id="241f2-139">OUTPUTS</span></span>

### <span data-ttu-id="241f2-140">Microsoft AzureStack. 관리. m. 관리자. 볼륨</span><span class="sxs-lookup"><span data-stu-id="241f2-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="241f2-141">상속자</span><span class="sxs-lookup"><span data-stu-id="241f2-141">NOTES</span></span>

## <span data-ttu-id="241f2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="241f2-142">RELATED LINKS</span></span>
