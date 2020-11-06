---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523819"
---
# <span data-ttu-id="daf50-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="daf50-101">Get-AzsVolume</span></span>

## <span data-ttu-id="daf50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daf50-102">SYNOPSIS</span></span>
<span data-ttu-id="daf50-103">위치에 있는 모든 저장소 볼륨의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="daf50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="daf50-104">SYNTAX</span></span>

### <span data-ttu-id="daf50-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="daf50-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="daf50-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="daf50-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="daf50-107">리소스</span><span class="sxs-lookup"><span data-stu-id="daf50-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="daf50-108">설명은</span><span class="sxs-lookup"><span data-stu-id="daf50-108">DESCRIPTION</span></span>
<span data-ttu-id="daf50-109">위치에 있는 모든 저장소 볼륨의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="daf50-110">예제의</span><span class="sxs-lookup"><span data-stu-id="daf50-110">EXAMPLES</span></span>

### <span data-ttu-id="daf50-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="daf50-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="daf50-112">지정 된 위치에 있는 모든 저장소 볼륨의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="daf50-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="daf50-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="daf50-114">지정 된 위치에서 이름으로 저장소 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="daf50-115">변수</span><span class="sxs-lookup"><span data-stu-id="daf50-115">PARAMETERS</span></span>

### <span data-ttu-id="daf50-116">-필터</span><span class="sxs-lookup"><span data-stu-id="daf50-116">-Filter</span></span>
<span data-ttu-id="daf50-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="daf50-118">-위치</span><span class="sxs-lookup"><span data-stu-id="daf50-118">-Location</span></span>
<span data-ttu-id="daf50-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-119">Location of the resource.</span></span>

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

### <span data-ttu-id="daf50-120">-이름</span><span class="sxs-lookup"><span data-stu-id="daf50-120">-Name</span></span>
<span data-ttu-id="daf50-121">저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="daf50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf50-122">-ResourceGroupName</span></span>
<span data-ttu-id="daf50-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="daf50-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daf50-124">-ResourceId</span></span>
<span data-ttu-id="daf50-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-125">The resource id.</span></span>

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

### <span data-ttu-id="daf50-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="daf50-126">-ScaleUnit</span></span>
<span data-ttu-id="daf50-127">배율 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="daf50-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="daf50-128">-StorageSubSystem</span></span>
<span data-ttu-id="daf50-129">볼륨이 위치한 저장소 하위 시스템.</span><span class="sxs-lookup"><span data-stu-id="daf50-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="daf50-130">-위쪽</span><span class="sxs-lookup"><span data-stu-id="daf50-130">-Top</span></span>
<span data-ttu-id="daf50-131">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="daf50-132">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="daf50-133">-생략</span><span class="sxs-lookup"><span data-stu-id="daf50-133">-Skip</span></span>
<span data-ttu-id="daf50-134">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="daf50-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf50-135">CommonParameters</span></span>
<span data-ttu-id="daf50-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf50-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf50-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf50-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf50-138">입력</span><span class="sxs-lookup"><span data-stu-id="daf50-138">INPUTS</span></span>

## <span data-ttu-id="daf50-139">출력</span><span class="sxs-lookup"><span data-stu-id="daf50-139">OUTPUTS</span></span>

### <span data-ttu-id="daf50-140">Microsoft AzureStack. 관리. m. 관리자. 볼륨</span><span class="sxs-lookup"><span data-stu-id="daf50-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="daf50-141">상속자</span><span class="sxs-lookup"><span data-stu-id="daf50-141">NOTES</span></span>

## <span data-ttu-id="daf50-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daf50-142">RELATED LINKS</span></span>
