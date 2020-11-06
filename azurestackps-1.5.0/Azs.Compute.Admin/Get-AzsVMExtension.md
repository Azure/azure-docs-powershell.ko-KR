---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523388"
---
# <span data-ttu-id="99e92-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="99e92-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="99e92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e92-102">SYNOPSIS</span></span>
<span data-ttu-id="99e92-103">현재 사용할 수 있는 가상 컴퓨터 이미지 확장을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="99e92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99e92-104">SYNTAX</span></span>

### <span data-ttu-id="99e92-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="99e92-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="99e92-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="99e92-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="99e92-107">리소스</span><span class="sxs-lookup"><span data-stu-id="99e92-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="99e92-108">설명은</span><span class="sxs-lookup"><span data-stu-id="99e92-108">DESCRIPTION</span></span>
<span data-ttu-id="99e92-109">가상 컴퓨터 이미지 확장을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="99e92-110">예제의</span><span class="sxs-lookup"><span data-stu-id="99e92-110">EXAMPLES</span></span>

### <span data-ttu-id="99e92-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="99e92-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="99e92-112">위치에서 모든 VM 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="99e92-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="99e92-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="99e92-114">특정 VM 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-114">Get specific VM extension.</span></span>

## <span data-ttu-id="99e92-115">변수</span><span class="sxs-lookup"><span data-stu-id="99e92-115">PARAMETERS</span></span>

### <span data-ttu-id="99e92-116">-위치</span><span class="sxs-lookup"><span data-stu-id="99e92-116">-Location</span></span>
<span data-ttu-id="99e92-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-117">Location of the resource.</span></span>

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

### <span data-ttu-id="99e92-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="99e92-118">-Publisher</span></span>
<span data-ttu-id="99e92-119">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="99e92-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99e92-120">-ResourceId</span></span>
<span data-ttu-id="99e92-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-121">The resource id.</span></span>

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

### <span data-ttu-id="99e92-122">-Type</span><span class="sxs-lookup"><span data-stu-id="99e92-122">-Type</span></span>
<span data-ttu-id="99e92-123">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-123">Type of extension.</span></span>

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

### <span data-ttu-id="99e92-124">-버전</span><span class="sxs-lookup"><span data-stu-id="99e92-124">-Version</span></span>
<span data-ttu-id="99e92-125">가상 컴퓨터 이미지 확장 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="99e92-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e92-126">CommonParameters</span></span>
<span data-ttu-id="99e92-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99e92-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e92-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e92-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e92-129">입력</span><span class="sxs-lookup"><span data-stu-id="99e92-129">INPUTS</span></span>

## <span data-ttu-id="99e92-130">출력</span><span class="sxs-lookup"><span data-stu-id="99e92-130">OUTPUTS</span></span>

### <span data-ttu-id="99e92-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="99e92-131">VmExtensionObject</span></span>

## <span data-ttu-id="99e92-132">상속자</span><span class="sxs-lookup"><span data-stu-id="99e92-132">NOTES</span></span>

## <span data-ttu-id="99e92-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99e92-133">RELATED LINKS</span></span>

