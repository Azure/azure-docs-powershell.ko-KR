---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875045"
---
# <span data-ttu-id="bdf7f-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="bdf7f-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="bdf7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdf7f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf7f-103">현재 사용할 수 있는 가상 컴퓨터 이미지 확장을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="bdf7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdf7f-104">SYNTAX</span></span>

### <span data-ttu-id="bdf7f-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bdf7f-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="bdf7f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="bdf7f-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdf7f-107">리소스</span><span class="sxs-lookup"><span data-stu-id="bdf7f-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bdf7f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bdf7f-108">DESCRIPTION</span></span>
<span data-ttu-id="bdf7f-109">가상 컴퓨터 이미지 확장을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="bdf7f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bdf7f-110">EXAMPLES</span></span>

### <span data-ttu-id="bdf7f-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bdf7f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="bdf7f-112">위치에서 모든 VM 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="bdf7f-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bdf7f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="bdf7f-114">특정 VM 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-114">Get specific VM extension.</span></span>

## <span data-ttu-id="bdf7f-115">변수</span><span class="sxs-lookup"><span data-stu-id="bdf7f-115">PARAMETERS</span></span>

### <span data-ttu-id="bdf7f-116">-위치</span><span class="sxs-lookup"><span data-stu-id="bdf7f-116">-Location</span></span>
<span data-ttu-id="bdf7f-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-117">Location of the resource.</span></span>

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

### <span data-ttu-id="bdf7f-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="bdf7f-118">-Publisher</span></span>
<span data-ttu-id="bdf7f-119">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="bdf7f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdf7f-120">-ResourceId</span></span>
<span data-ttu-id="bdf7f-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-121">The resource id.</span></span>

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

### <span data-ttu-id="bdf7f-122">-Type</span><span class="sxs-lookup"><span data-stu-id="bdf7f-122">-Type</span></span>
<span data-ttu-id="bdf7f-123">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-123">Type of extension.</span></span>

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

### <span data-ttu-id="bdf7f-124">-버전</span><span class="sxs-lookup"><span data-stu-id="bdf7f-124">-Version</span></span>
<span data-ttu-id="bdf7f-125">가상 컴퓨터 이미지 확장 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="bdf7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf7f-126">CommonParameters</span></span>
<span data-ttu-id="bdf7f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf7f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf7f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf7f-129">입력</span><span class="sxs-lookup"><span data-stu-id="bdf7f-129">INPUTS</span></span>

## <span data-ttu-id="bdf7f-130">출력</span><span class="sxs-lookup"><span data-stu-id="bdf7f-130">OUTPUTS</span></span>

### <span data-ttu-id="bdf7f-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="bdf7f-131">VmExtensionObject</span></span>

## <span data-ttu-id="bdf7f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="bdf7f-132">NOTES</span></span>

## <span data-ttu-id="bdf7f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdf7f-133">RELATED LINKS</span></span>

