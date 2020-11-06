---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523703"
---
# <span data-ttu-id="ad42e-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="ad42e-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="ad42e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad42e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad42e-103">위치에 있는 모든 저장소 볼륨의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="ad42e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad42e-104">SYNTAX</span></span>

### <span data-ttu-id="ad42e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad42e-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ad42e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="ad42e-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ad42e-107">리소스</span><span class="sxs-lookup"><span data-stu-id="ad42e-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad42e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ad42e-108">DESCRIPTION</span></span>
<span data-ttu-id="ad42e-109">위치에 있는 모든 저장소 볼륨의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="ad42e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ad42e-110">EXAMPLES</span></span>

### <span data-ttu-id="ad42e-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad42e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="ad42e-112">지정 된 위치에 있는 모든 저장소 볼륨의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="ad42e-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad42e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="ad42e-114">지정 된 위치에서 이름으로 저장소 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="ad42e-115">변수</span><span class="sxs-lookup"><span data-stu-id="ad42e-115">PARAMETERS</span></span>

### <span data-ttu-id="ad42e-116">-필터</span><span class="sxs-lookup"><span data-stu-id="ad42e-116">-Filter</span></span>
<span data-ttu-id="ad42e-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="ad42e-118">-위치</span><span class="sxs-lookup"><span data-stu-id="ad42e-118">-Location</span></span>
<span data-ttu-id="ad42e-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ad42e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ad42e-120">-Name</span></span>
<span data-ttu-id="ad42e-121">저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="ad42e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad42e-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad42e-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ad42e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad42e-124">-ResourceId</span></span>
<span data-ttu-id="ad42e-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-125">The resource id.</span></span>

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

### <span data-ttu-id="ad42e-126">-생략</span><span class="sxs-lookup"><span data-stu-id="ad42e-126">-Skip</span></span>
<span data-ttu-id="ad42e-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ad42e-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="ad42e-128">-StoragePool</span></span>
<span data-ttu-id="ad42e-129">저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-129">Storage pool name.</span></span>

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

### <span data-ttu-id="ad42e-130">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="ad42e-130">-StorageSystem</span></span>
<span data-ttu-id="ad42e-131">인프라 볼륨이 있는 저장소 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="ad42e-132">-위쪽</span><span class="sxs-lookup"><span data-stu-id="ad42e-132">-Top</span></span>
<span data-ttu-id="ad42e-133">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ad42e-134">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ad42e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad42e-135">CommonParameters</span></span>
<span data-ttu-id="ad42e-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad42e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad42e-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad42e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad42e-138">입력</span><span class="sxs-lookup"><span data-stu-id="ad42e-138">INPUTS</span></span>

## <span data-ttu-id="ad42e-139">출력</span><span class="sxs-lookup"><span data-stu-id="ad42e-139">OUTPUTS</span></span>

### <span data-ttu-id="ad42e-140">Microsoft AzureStack. 관리. m. 관리자. 볼륨</span><span class="sxs-lookup"><span data-stu-id="ad42e-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="ad42e-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ad42e-141">NOTES</span></span>

## <span data-ttu-id="ad42e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad42e-142">RELATED LINKS</span></span>

