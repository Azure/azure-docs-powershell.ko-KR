---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875078"
---
# <span data-ttu-id="9af64-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="9af64-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="9af64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af64-102">SYNOPSIS</span></span>
<span data-ttu-id="9af64-103">사용 가능한 업데이트 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-103">Get the list of available updates.</span></span>

## <span data-ttu-id="9af64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9af64-104">SYNTAX</span></span>

### <span data-ttu-id="9af64-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9af64-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="9af64-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9af64-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9af64-107">리소스</span><span class="sxs-lookup"><span data-stu-id="9af64-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9af64-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9af64-108">DESCRIPTION</span></span>
<span data-ttu-id="9af64-109">사용 가능한 업데이트 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-109">Get the list of available updates.</span></span> <span data-ttu-id="9af64-110">이 모듈에서 반환 된 업데이트는 해당 하는 경우 ' AzsUpdate '로 파이프 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="9af64-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9af64-111">EXAMPLES</span></span>

### <span data-ttu-id="9af64-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9af64-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="9af64-113">사용 가능한 업데이트 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-113">Get the list of available updates.</span></span>

### <span data-ttu-id="9af64-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9af64-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="9af64-115">특정 업데이트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-115">Get the specific update.</span></span>

## <span data-ttu-id="9af64-116">변수</span><span class="sxs-lookup"><span data-stu-id="9af64-116">PARAMETERS</span></span>

### <span data-ttu-id="9af64-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9af64-117">-Name</span></span>
<span data-ttu-id="9af64-118">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af64-119">-위치</span><span class="sxs-lookup"><span data-stu-id="9af64-119">-Location</span></span>
<span data-ttu-id="9af64-120">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-120">The name of the update location.</span></span>

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

### <span data-ttu-id="9af64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af64-121">-ResourceGroupName</span></span>
<span data-ttu-id="9af64-122">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9af64-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9af64-123">-ResourceId</span></span>
<span data-ttu-id="9af64-124">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-124">The resource id.</span></span>

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

### <span data-ttu-id="9af64-125">-생략</span><span class="sxs-lookup"><span data-stu-id="9af64-125">-Skip</span></span>
<span data-ttu-id="9af64-126">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9af64-127">-위쪽</span><span class="sxs-lookup"><span data-stu-id="9af64-127">-Top</span></span>
<span data-ttu-id="9af64-128">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9af64-129">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9af64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af64-130">CommonParameters</span></span>
<span data-ttu-id="9af64-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af64-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af64-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af64-133">입력</span><span class="sxs-lookup"><span data-stu-id="9af64-133">INPUTS</span></span>

## <span data-ttu-id="9af64-134">출력</span><span class="sxs-lookup"><span data-stu-id="9af64-134">OUTPUTS</span></span>

### <span data-ttu-id="9af64-135">Update.exe의 업데이트. 관리자. 업데이트</span><span class="sxs-lookup"><span data-stu-id="9af64-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="9af64-136">상속자</span><span class="sxs-lookup"><span data-stu-id="9af64-136">NOTES</span></span>

## <span data-ttu-id="9af64-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9af64-137">RELATED LINKS</span></span>
