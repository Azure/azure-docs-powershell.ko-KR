---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874554"
---
# <span data-ttu-id="676bd-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="676bd-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="676bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="676bd-102">SYNOPSIS</span></span>
<span data-ttu-id="676bd-103">계산 개체에 대 한 할당량 제한을 지정 하는 할당량을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="676bd-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="676bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="676bd-104">SYNTAX</span></span>

### <span data-ttu-id="676bd-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="676bd-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="676bd-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="676bd-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="676bd-107">리소스</span><span class="sxs-lookup"><span data-stu-id="676bd-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="676bd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="676bd-108">DESCRIPTION</span></span>
<span data-ttu-id="676bd-109">기존 할당량 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="676bd-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="676bd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="676bd-110">EXAMPLES</span></span>

### <span data-ttu-id="676bd-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="676bd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="676bd-112">지정 된 위치에 모든 계산 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="676bd-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="676bd-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="676bd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="676bd-114">특정 계산 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="676bd-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="676bd-115">변수</span><span class="sxs-lookup"><span data-stu-id="676bd-115">PARAMETERS</span></span>

### <span data-ttu-id="676bd-116">-위치</span><span class="sxs-lookup"><span data-stu-id="676bd-116">-Location</span></span>
<span data-ttu-id="676bd-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="676bd-117">Location of the resource.</span></span>

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

### <span data-ttu-id="676bd-118">-이름</span><span class="sxs-lookup"><span data-stu-id="676bd-118">-Name</span></span>
<span data-ttu-id="676bd-119">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="676bd-119">Name of the quota.</span></span>

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

### <span data-ttu-id="676bd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="676bd-120">-ResourceId</span></span>
<span data-ttu-id="676bd-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="676bd-121">The resource id.</span></span>

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

### <span data-ttu-id="676bd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="676bd-122">CommonParameters</span></span>
<span data-ttu-id="676bd-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="676bd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="676bd-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="676bd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="676bd-125">입력</span><span class="sxs-lookup"><span data-stu-id="676bd-125">INPUTS</span></span>

## <span data-ttu-id="676bd-126">출력</span><span class="sxs-lookup"><span data-stu-id="676bd-126">OUTPUTS</span></span>

### <span data-ttu-id="676bd-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="676bd-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="676bd-128">상속자</span><span class="sxs-lookup"><span data-stu-id="676bd-128">NOTES</span></span>

## <span data-ttu-id="676bd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="676bd-129">RELATED LINKS</span></span>

