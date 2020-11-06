---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523427"
---
# <span data-ttu-id="b8eb6-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="b8eb6-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="b8eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b8eb6-103">위치에 대 한 모든 저장소 풀의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="b8eb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8eb6-104">SYNTAX</span></span>

### <span data-ttu-id="b8eb6-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8eb6-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8eb6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b8eb6-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8eb6-107">리소스</span><span class="sxs-lookup"><span data-stu-id="b8eb6-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b8eb6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b8eb6-108">DESCRIPTION</span></span>
<span data-ttu-id="b8eb6-109">위치에 대 한 모든 저장소 풀의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="b8eb6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b8eb6-110">EXAMPLES</span></span>

### <span data-ttu-id="b8eb6-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8eb6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="b8eb6-112">지정 된 위치에서 모든 저장소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="b8eb6-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8eb6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="b8eb6-114">저장소 풀 이름을 지정 된 위치에서 저장소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="b8eb6-115">변수</span><span class="sxs-lookup"><span data-stu-id="b8eb6-115">PARAMETERS</span></span>

### <span data-ttu-id="b8eb6-116">-필터</span><span class="sxs-lookup"><span data-stu-id="b8eb6-116">-Filter</span></span>
<span data-ttu-id="b8eb6-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b8eb6-118">-위치</span><span class="sxs-lookup"><span data-stu-id="b8eb6-118">-Location</span></span>
<span data-ttu-id="b8eb6-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b8eb6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b8eb6-120">-Name</span></span>
<span data-ttu-id="b8eb6-121">저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-121">Storage pool name.</span></span>

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

### <span data-ttu-id="b8eb6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8eb6-122">-ResourceGroupName</span></span>
<span data-ttu-id="b8eb6-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b8eb6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8eb6-124">-ResourceId</span></span>
<span data-ttu-id="b8eb6-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-125">The resource id.</span></span>

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

### <span data-ttu-id="b8eb6-126">-생략</span><span class="sxs-lookup"><span data-stu-id="b8eb6-126">-Skip</span></span>
<span data-ttu-id="b8eb6-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b8eb6-128">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="b8eb6-128">-StorageSystem</span></span>
<span data-ttu-id="b8eb6-129">저장소 풀이 있는 저장소 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="b8eb6-130">-위쪽</span><span class="sxs-lookup"><span data-stu-id="b8eb6-130">-Top</span></span>
<span data-ttu-id="b8eb6-131">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b8eb6-132">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b8eb6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8eb6-133">CommonParameters</span></span>
<span data-ttu-id="b8eb6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8eb6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8eb6-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8eb6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8eb6-136">입력</span><span class="sxs-lookup"><span data-stu-id="b8eb6-136">INPUTS</span></span>

## <span data-ttu-id="b8eb6-137">출력</span><span class="sxs-lookup"><span data-stu-id="b8eb6-137">OUTPUTS</span></span>

### <span data-ttu-id="b8eb6-138">Microsoft AzureStack. 관리. m. 관리자. 저장소 풀</span><span class="sxs-lookup"><span data-stu-id="b8eb6-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="b8eb6-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b8eb6-139">NOTES</span></span>

## <span data-ttu-id="b8eb6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8eb6-140">RELATED LINKS</span></span>

