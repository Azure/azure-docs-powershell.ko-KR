---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874590"
---
# <span data-ttu-id="f2e04-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="f2e04-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="f2e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e04-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e04-103">지정 된 이미지 구성에서 가상 컴퓨터 플랫폼 이미지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="f2e04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2e04-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2e04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2e04-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e04-106">플랫폼 이미지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-106">Add a platform image.</span></span>

## <span data-ttu-id="f2e04-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2e04-107">EXAMPLES</span></span>

### <span data-ttu-id="f2e04-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f2e04-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="f2e04-109">새 플랫폼 이미지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-109">Add a new platform image.</span></span>

## <span data-ttu-id="f2e04-110">변수</span><span class="sxs-lookup"><span data-stu-id="f2e04-110">PARAMETERS</span></span>

### <span data-ttu-id="f2e04-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2e04-111">-AsJob</span></span>
<span data-ttu-id="f2e04-112">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="f2e04-113">-BillingPartNumber</span></span>
<span data-ttu-id="f2e04-114">부품 번호는 소프트웨어 비용을 청구 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-115">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="f2e04-115">-DataDisks</span></span>
<span data-ttu-id="f2e04-116">플랫폼 이미지에 사용 되는 데이터 디스크</span><span class="sxs-lookup"><span data-stu-id="f2e04-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f2e04-117">-Force</span></span>
<span data-ttu-id="f2e04-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-119">-위치</span><span class="sxs-lookup"><span data-stu-id="f2e04-119">-Location</span></span>
<span data-ttu-id="f2e04-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-121">-제공</span><span class="sxs-lookup"><span data-stu-id="f2e04-121">-Offer</span></span>
<span data-ttu-id="f2e04-122">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="f2e04-123">-OsType</span></span>
<span data-ttu-id="f2e04-124">운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="f2e04-125">-OsUri</span></span>
<span data-ttu-id="f2e04-126">디스크의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f2e04-127">-Publisher</span></span>
<span data-ttu-id="f2e04-128">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="f2e04-129">-Sku</span></span>
<span data-ttu-id="f2e04-130">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-131">-버전</span><span class="sxs-lookup"><span data-stu-id="f2e04-131">-Version</span></span>
<span data-ttu-id="f2e04-132">가상 컴퓨터 플랫폼 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f2e04-133">-Confirm</span></span>
<span data-ttu-id="f2e04-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e04-135">-WhatIf</span></span>
<span data-ttu-id="f2e04-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e04-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e04-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e04-138">CommonParameters</span></span>
<span data-ttu-id="f2e04-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e04-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e04-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e04-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e04-141">입력</span><span class="sxs-lookup"><span data-stu-id="f2e04-141">INPUTS</span></span>

## <span data-ttu-id="f2e04-142">출력</span><span class="sxs-lookup"><span data-stu-id="f2e04-142">OUTPUTS</span></span>

### <span data-ttu-id="f2e04-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="f2e04-143">PlatformImageObject</span></span>

## <span data-ttu-id="f2e04-144">상속자</span><span class="sxs-lookup"><span data-stu-id="f2e04-144">NOTES</span></span>

## <span data-ttu-id="f2e04-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2e04-145">RELATED LINKS</span></span>

