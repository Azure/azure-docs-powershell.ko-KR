---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875048"
---
# <span data-ttu-id="051ce-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="051ce-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="051ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="051ce-102">SYNOPSIS</span></span>
<span data-ttu-id="051ce-103">관리 되는 디스크 마이그레이션 작업의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="051ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="051ce-104">SYNTAX</span></span>

### <span data-ttu-id="051ce-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="051ce-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="051ce-106">리소스</span><span class="sxs-lookup"><span data-stu-id="051ce-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="051ce-107">가져오기</span><span class="sxs-lookup"><span data-stu-id="051ce-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="051ce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="051ce-108">DESCRIPTION</span></span>
<span data-ttu-id="051ce-109">디스크 마이그레이션 작업 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="051ce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="051ce-110">EXAMPLES</span></span>

### <span data-ttu-id="051ce-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="051ce-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="051ce-112">특정 관리 디스크 마이그레이션 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="051ce-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="051ce-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="051ce-114">로컬 위치에서 관리 되는 디스크 마이그레이션 작업의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="051ce-115">변수</span><span class="sxs-lookup"><span data-stu-id="051ce-115">PARAMETERS</span></span>

### <span data-ttu-id="051ce-116">-위치</span><span class="sxs-lookup"><span data-stu-id="051ce-116">-Location</span></span>
<span data-ttu-id="051ce-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-117">Location of the resource.</span></span>

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

### <span data-ttu-id="051ce-118">-이름</span><span class="sxs-lookup"><span data-stu-id="051ce-118">-Name</span></span>
<span data-ttu-id="051ce-119">마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ce-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="051ce-120">-ResourceId</span></span>
<span data-ttu-id="051ce-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051ce-122">-상태</span><span class="sxs-lookup"><span data-stu-id="051ce-122">-Status</span></span>
<span data-ttu-id="051ce-123">디스크 마이그레이션 작업 상태의 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="051ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051ce-124">CommonParameters</span></span>
<span data-ttu-id="051ce-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="051ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051ce-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="051ce-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051ce-127">입력</span><span class="sxs-lookup"><span data-stu-id="051ce-127">INPUTS</span></span>

## <span data-ttu-id="051ce-128">출력</span><span class="sxs-lookup"><span data-stu-id="051ce-128">OUTPUTS</span></span>

### <span data-ttu-id="051ce-129">DiskMigrationJob의. 관리자. 관리.</span><span class="sxs-lookup"><span data-stu-id="051ce-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="051ce-130">상속자</span><span class="sxs-lookup"><span data-stu-id="051ce-130">NOTES</span></span>

## <span data-ttu-id="051ce-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="051ce-131">RELATED LINKS</span></span>

