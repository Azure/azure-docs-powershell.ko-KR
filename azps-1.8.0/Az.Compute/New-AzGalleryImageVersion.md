---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701313"
---
# <span data-ttu-id="6d3e8-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="6d3e8-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="6d3e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3e8-103">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-103">Create a gallery image version.</span></span>

## <span data-ttu-id="6d3e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d3e8-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d3e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d3e8-105">DESCRIPTION</span></span>
<span data-ttu-id="6d3e8-106">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-106">Create a gallery image version.</span></span>

## <span data-ttu-id="6d3e8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6d3e8-107">EXAMPLES</span></span>

### <span data-ttu-id="6d3e8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d3e8-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="6d3e8-109">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-109">Create a gallery image version.</span></span>

## <span data-ttu-id="6d3e8-110">변수</span><span class="sxs-lookup"><span data-stu-id="6d3e8-110">PARAMETERS</span></span>

### <span data-ttu-id="6d3e8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d3e8-111">-AsJob</span></span>
<span data-ttu-id="6d3e8-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6d3e8-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3e8-113">-DefaultProfile</span></span>
<span data-ttu-id="6d3e8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6d3e8-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="6d3e8-116">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6d3e8-117">-GalleryName</span></span>
<span data-ttu-id="6d3e8-118">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-118">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6d3e8-119">-Location</span></span>
<span data-ttu-id="6d3e8-120">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="6d3e8-120">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6d3e8-121">-Name</span></span>
<span data-ttu-id="6d3e8-122">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="6d3e8-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="6d3e8-124">갤러리 이미지 버전의 기간 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-124">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="6d3e8-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="6d3e8-126">설정 된 경우 최신 버전의 이미지 정의에서 배포 된 가상 컴퓨터는이 이미지 버전을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="6d3e8-127">-ReplicaCount</span></span>
<span data-ttu-id="6d3e8-128">지역별로 만들 이미지 버전의 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-128">The number of replicas of the Image Version to be created per region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d3e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d3e8-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="6d3e8-131">-SourceImageId</span></span>
<span data-ttu-id="6d3e8-132">이미지 버전을 만들 원본 이미지의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-132">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-133">태그</span><span class="sxs-lookup"><span data-stu-id="6d3e8-133">-Tag</span></span>
<span data-ttu-id="6d3e8-134">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="6d3e8-134">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="6d3e8-135">-TargetRegion</span></span>
<span data-ttu-id="6d3e8-136">이미지 버전이 복제 될 대상 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-136">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-137">-확인</span><span class="sxs-lookup"><span data-stu-id="6d3e8-137">-Confirm</span></span>
<span data-ttu-id="6d3e8-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3e8-139">-WhatIf</span></span>
<span data-ttu-id="6d3e8-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d3e8-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3e8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3e8-142">CommonParameters</span></span>
<span data-ttu-id="6d3e8-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3e8-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3e8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3e8-145">입력</span><span class="sxs-lookup"><span data-stu-id="6d3e8-145">INPUTS</span></span>

### <span data-ttu-id="6d3e8-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d3e8-146">System.String</span></span>

### <span data-ttu-id="6d3e8-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="6d3e8-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6d3e8-148">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-148">System.Int32</span></span>

### <span data-ttu-id="6d3e8-149">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d3e8-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6d3e8-150">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="6d3e8-150">System.DateTime</span></span>

### <span data-ttu-id="6d3e8-151">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="6d3e8-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="6d3e8-152">출력</span><span class="sxs-lookup"><span data-stu-id="6d3e8-152">OUTPUTS</span></span>

### <span data-ttu-id="6d3e8-153">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="6d3e8-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="6d3e8-154">상속자</span><span class="sxs-lookup"><span data-stu-id="6d3e8-154">NOTES</span></span>

## <span data-ttu-id="6d3e8-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d3e8-155">RELATED LINKS</span></span>
