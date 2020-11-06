---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42181271e9295212f256cfc519e8ecc32eeae048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524084"
---
# <span data-ttu-id="76b77-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="76b77-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="76b77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b77-102">SYNOPSIS</span></span>
<span data-ttu-id="76b77-103">새 가상 컴퓨터 확장 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="76b77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76b77-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76b77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="76b77-105">DESCRIPTION</span></span>
<span data-ttu-id="76b77-106">가상 컴퓨터 확장 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="76b77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="76b77-107">EXAMPLES</span></span>

### <span data-ttu-id="76b77-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="76b77-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="76b77-109">새 플랫폼 이미지 확장명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="76b77-110">변수</span><span class="sxs-lookup"><span data-stu-id="76b77-110">PARAMETERS</span></span>

### <span data-ttu-id="76b77-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76b77-111">-AsJob</span></span>
<span data-ttu-id="76b77-112">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="76b77-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="76b77-113">-ComputeRole</span></span>
<span data-ttu-id="76b77-114">이 확장이 지 원하는 역할 유형, IaaS 또는 PaaS입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="76b77-115">-Force</span><span class="sxs-lookup"><span data-stu-id="76b77-115">-Force</span></span>
<span data-ttu-id="76b77-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="76b77-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="76b77-117">-IsSystemExtension</span></span>
<span data-ttu-id="76b77-118">시스템에 대 한 내선 번호 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="76b77-119">-위치</span><span class="sxs-lookup"><span data-stu-id="76b77-119">-Location</span></span>
<span data-ttu-id="76b77-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-120">Location of the resource.</span></span>

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

### <span data-ttu-id="76b77-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="76b77-121">-Publisher</span></span>
<span data-ttu-id="76b77-122">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="76b77-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="76b77-123">-SourceBlob</span></span>
<span data-ttu-id="76b77-124">가상 컴퓨터 확장 패키지의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b77-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="76b77-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="76b77-126">여러 확장명을 지 원하는 경우 True입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="76b77-127">-Type</span><span class="sxs-lookup"><span data-stu-id="76b77-127">-Type</span></span>
<span data-ttu-id="76b77-128">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-128">Type of extension.</span></span>

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

### <span data-ttu-id="76b77-129">-버전</span><span class="sxs-lookup"><span data-stu-id="76b77-129">-Version</span></span>
<span data-ttu-id="76b77-130">Vritual 컴퓨터 이미지 확장명의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="76b77-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="76b77-131">-VmOsType</span></span>
<span data-ttu-id="76b77-132">확장 처리기를 배포 하는 데 필요한 대상 가상 컴퓨터 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="76b77-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="76b77-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="76b77-134">확장을 가상 컴퓨터 확장 집합 지원에 사용할 수 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="76b77-135">-확인</span><span class="sxs-lookup"><span data-stu-id="76b77-135">-Confirm</span></span>
<span data-ttu-id="76b77-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b77-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b77-137">-WhatIf</span></span>
<span data-ttu-id="76b77-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b77-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b77-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b77-140">CommonParameters</span></span>
<span data-ttu-id="76b77-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76b77-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b77-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b77-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b77-143">입력</span><span class="sxs-lookup"><span data-stu-id="76b77-143">INPUTS</span></span>

## <span data-ttu-id="76b77-144">출력</span><span class="sxs-lookup"><span data-stu-id="76b77-144">OUTPUTS</span></span>

### <span data-ttu-id="76b77-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="76b77-145">VmExtensionObject</span></span>

## <span data-ttu-id="76b77-146">상속자</span><span class="sxs-lookup"><span data-stu-id="76b77-146">NOTES</span></span>

## <span data-ttu-id="76b77-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76b77-147">RELATED LINKS</span></span>

