---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874652"
---
# <span data-ttu-id="edeb7-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="edeb7-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="edeb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="edeb7-103">위치에 대 한 모든 저장소 하위 시스템의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="edeb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="edeb7-104">SYNTAX</span></span>

### <span data-ttu-id="edeb7-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="edeb7-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="edeb7-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="edeb7-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="edeb7-107">리소스</span><span class="sxs-lookup"><span data-stu-id="edeb7-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="edeb7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="edeb7-108">DESCRIPTION</span></span>
<span data-ttu-id="edeb7-109">위치에 대 한 모든 저장소 하위 시스템의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="edeb7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="edeb7-110">EXAMPLES</span></span>

### <span data-ttu-id="edeb7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="edeb7-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="edeb7-112">위치에서 모든 저장소 하위 시스템을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="edeb7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="edeb7-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="edeb7-114">위치 및 이름이 지정 된 저장소 하위 시스템을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="edeb7-115">변수</span><span class="sxs-lookup"><span data-stu-id="edeb7-115">PARAMETERS</span></span>

### <span data-ttu-id="edeb7-116">-이름</span><span class="sxs-lookup"><span data-stu-id="edeb7-116">-Name</span></span>
<span data-ttu-id="edeb7-117">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="edeb7-118">-위치</span><span class="sxs-lookup"><span data-stu-id="edeb7-118">-Location</span></span>
<span data-ttu-id="edeb7-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-119">Location of the resource.</span></span>

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

### <span data-ttu-id="edeb7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edeb7-120">-ResourceGroupName</span></span>
<span data-ttu-id="edeb7-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="edeb7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edeb7-122">-ResourceId</span></span>
<span data-ttu-id="edeb7-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-123">The resource id.</span></span>

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

### <span data-ttu-id="edeb7-124">-필터</span><span class="sxs-lookup"><span data-stu-id="edeb7-124">-Filter</span></span>
<span data-ttu-id="edeb7-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="edeb7-126">-생략</span><span class="sxs-lookup"><span data-stu-id="edeb7-126">-Skip</span></span>
<span data-ttu-id="edeb7-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="edeb7-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="edeb7-128">-Top</span></span>
<span data-ttu-id="edeb7-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="edeb7-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="edeb7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edeb7-131">CommonParameters</span></span>
<span data-ttu-id="edeb7-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="edeb7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edeb7-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edeb7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edeb7-134">입력</span><span class="sxs-lookup"><span data-stu-id="edeb7-134">INPUTS</span></span>

## <span data-ttu-id="edeb7-135">출력</span><span class="sxs-lookup"><span data-stu-id="edeb7-135">OUTPUTS</span></span>

### <span data-ttu-id="edeb7-136">StorageSystem. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="edeb7-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="edeb7-137">상속자</span><span class="sxs-lookup"><span data-stu-id="edeb7-137">NOTES</span></span>

## <span data-ttu-id="edeb7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edeb7-138">RELATED LINKS</span></span>
