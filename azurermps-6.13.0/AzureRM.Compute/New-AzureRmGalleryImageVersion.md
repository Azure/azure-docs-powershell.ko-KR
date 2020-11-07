---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
ms.openlocfilehash: f27c861386e7a570fe72a5266362bee7fed39e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711404"
---
# <span data-ttu-id="5d3cd-101">New-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5d3cd-101">New-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="5d3cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d3cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3cd-103">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-103">Create a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d3cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d3cd-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3cd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d3cd-105">DESCRIPTION</span></span>
<span data-ttu-id="5d3cd-106">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-106">Create a gallery image version.</span></span>

## <span data-ttu-id="5d3cd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5d3cd-107">EXAMPLES</span></span>

### <span data-ttu-id="5d3cd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d3cd-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="5d3cd-109">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-109">Create a gallery image version.</span></span>

## <span data-ttu-id="5d3cd-110">변수</span><span class="sxs-lookup"><span data-stu-id="5d3cd-110">PARAMETERS</span></span>

### <span data-ttu-id="5d3cd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d3cd-111">-AsJob</span></span>
<span data-ttu-id="5d3cd-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5d3cd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d3cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3cd-113">-DefaultProfile</span></span>
<span data-ttu-id="5d3cd-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3cd-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5d3cd-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="5d3cd-116">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="5d3cd-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="5d3cd-117">-GalleryName</span></span>
<span data-ttu-id="5d3cd-118">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="5d3cd-119">-위치</span><span class="sxs-lookup"><span data-stu-id="5d3cd-119">-Location</span></span>
<span data-ttu-id="5d3cd-120">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="5d3cd-120">Resource location</span></span>

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

### <span data-ttu-id="5d3cd-121">-이름</span><span class="sxs-lookup"><span data-stu-id="5d3cd-121">-Name</span></span>
<span data-ttu-id="5d3cd-122">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="5d3cd-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="5d3cd-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="5d3cd-124">갤러리 이미지 버전의 기간 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="5d3cd-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="5d3cd-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="5d3cd-126">설정 된 경우 최신 버전의 이미지 정의에서 배포 된 가상 컴퓨터는이 이미지 버전을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="5d3cd-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5d3cd-127">-ReplicaCount</span></span>
<span data-ttu-id="5d3cd-128">지역별로 만들 이미지 버전의 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="5d3cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="5d3cd-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d3cd-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="5d3cd-131">-SourceImageId</span></span>
<span data-ttu-id="5d3cd-132">이미지 버전을 만들 원본 이미지의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="5d3cd-133">태그</span><span class="sxs-lookup"><span data-stu-id="5d3cd-133">-Tag</span></span>
<span data-ttu-id="5d3cd-134">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="5d3cd-134">Resource tags</span></span>

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

### <span data-ttu-id="5d3cd-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="5d3cd-135">-TargetRegion</span></span>
<span data-ttu-id="5d3cd-136">이미지 버전이 복제 될 대상 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="5d3cd-137">-확인</span><span class="sxs-lookup"><span data-stu-id="5d3cd-137">-Confirm</span></span>
<span data-ttu-id="5d3cd-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d3cd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d3cd-139">-WhatIf</span></span>
<span data-ttu-id="5d3cd-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d3cd-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d3cd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3cd-142">CommonParameters</span></span>
<span data-ttu-id="5d3cd-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3cd-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d3cd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3cd-145">입력</span><span class="sxs-lookup"><span data-stu-id="5d3cd-145">INPUTS</span></span>

### <span data-ttu-id="5d3cd-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d3cd-146">System.String</span></span>

### <span data-ttu-id="5d3cd-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="5d3cd-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5d3cd-148">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-148">System.Int32</span></span>

### <span data-ttu-id="5d3cd-149">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d3cd-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5d3cd-150">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="5d3cd-150">System.DateTime</span></span>

### <span data-ttu-id="5d3cd-151">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="5d3cd-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="5d3cd-152">출력</span><span class="sxs-lookup"><span data-stu-id="5d3cd-152">OUTPUTS</span></span>

### <span data-ttu-id="5d3cd-153">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="5d3cd-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="5d3cd-154">상속자</span><span class="sxs-lookup"><span data-stu-id="5d3cd-154">NOTES</span></span>

## <span data-ttu-id="5d3cd-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d3cd-155">RELATED LINKS</span></span>
