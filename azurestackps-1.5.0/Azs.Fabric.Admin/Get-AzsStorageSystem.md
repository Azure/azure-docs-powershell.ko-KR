---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 362eb6a8d688aab2276fa1166f65474dab488952
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523132"
---
# <span data-ttu-id="5a95f-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="5a95f-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="5a95f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a95f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a95f-103">위치에 대 한 모든 저장소 하위 시스템의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="5a95f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a95f-104">SYNTAX</span></span>

### <span data-ttu-id="5a95f-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a95f-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5a95f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="5a95f-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5a95f-107">리소스</span><span class="sxs-lookup"><span data-stu-id="5a95f-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5a95f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5a95f-108">DESCRIPTION</span></span>
<span data-ttu-id="5a95f-109">위치에 대 한 모든 저장소 하위 시스템의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="5a95f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5a95f-110">EXAMPLES</span></span>

### <span data-ttu-id="5a95f-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a95f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="5a95f-112">위치에서 모든 저장소 하위 시스템을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="5a95f-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a95f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="5a95f-114">위치 및 이름이 지정 된 저장소 하위 시스템을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="5a95f-115">변수</span><span class="sxs-lookup"><span data-stu-id="5a95f-115">PARAMETERS</span></span>

### <span data-ttu-id="5a95f-116">-필터</span><span class="sxs-lookup"><span data-stu-id="5a95f-116">-Filter</span></span>
<span data-ttu-id="5a95f-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="5a95f-118">-위치</span><span class="sxs-lookup"><span data-stu-id="5a95f-118">-Location</span></span>
<span data-ttu-id="5a95f-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5a95f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="5a95f-120">-Name</span></span>
<span data-ttu-id="5a95f-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5a95f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a95f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a95f-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5a95f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a95f-124">-ResourceId</span></span>
<span data-ttu-id="5a95f-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-125">The resource id.</span></span>

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

### <span data-ttu-id="5a95f-126">-생략</span><span class="sxs-lookup"><span data-stu-id="5a95f-126">-Skip</span></span>
<span data-ttu-id="5a95f-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5a95f-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="5a95f-128">-Top</span></span>
<span data-ttu-id="5a95f-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5a95f-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5a95f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a95f-131">CommonParameters</span></span>
<span data-ttu-id="5a95f-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a95f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a95f-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a95f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a95f-134">입력</span><span class="sxs-lookup"><span data-stu-id="5a95f-134">INPUTS</span></span>

## <span data-ttu-id="5a95f-135">출력</span><span class="sxs-lookup"><span data-stu-id="5a95f-135">OUTPUTS</span></span>

### <span data-ttu-id="5a95f-136">StorageSystem. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="5a95f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="5a95f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="5a95f-137">NOTES</span></span>

## <span data-ttu-id="5a95f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a95f-138">RELATED LINKS</span></span>

