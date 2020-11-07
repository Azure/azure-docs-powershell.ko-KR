---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 80536a8bfce32d713649f3feab4d77b1662206b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697377"
---
# <span data-ttu-id="b7f3a-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b7f3a-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="b7f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f3a-103">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-103">Create a gallery image version.</span></span>

## <span data-ttu-id="b7f3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7f3a-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-StorageAccountType <String>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b7f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f3a-106">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-106">Create a gallery image version.</span></span>

## <span data-ttu-id="b7f3a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b7f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="b7f3a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7f3a-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="b7f3a-109">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-109">Create a gallery image version.</span></span>

## <span data-ttu-id="b7f3a-110">변수</span><span class="sxs-lookup"><span data-stu-id="b7f3a-110">PARAMETERS</span></span>

### <span data-ttu-id="b7f3a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7f3a-111">-AsJob</span></span>
<span data-ttu-id="b7f3a-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b7f3a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7f3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f3a-113">-DefaultProfile</span></span>
<span data-ttu-id="b7f3a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f3a-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b7f3a-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="b7f3a-116">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="b7f3a-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b7f3a-117">-GalleryName</span></span>
<span data-ttu-id="b7f3a-118">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="b7f3a-119">-위치</span><span class="sxs-lookup"><span data-stu-id="b7f3a-119">-Location</span></span>
<span data-ttu-id="b7f3a-120">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="b7f3a-120">Resource location</span></span>

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

### <span data-ttu-id="b7f3a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b7f3a-121">-Name</span></span>
<span data-ttu-id="b7f3a-122">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="b7f3a-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="b7f3a-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="b7f3a-124">갤러리 이미지 버전의 기간 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="b7f3a-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="b7f3a-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="b7f3a-126">설정 된 경우 최신 버전의 이미지 정의에서 배포 된 가상 컴퓨터는이 이미지 버전을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="b7f3a-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b7f3a-127">-ReplicaCount</span></span>
<span data-ttu-id="b7f3a-128">지역별로 만들 이미지 버전의 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="b7f3a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f3a-129">-ResourceGroupName</span></span>
<span data-ttu-id="b7f3a-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7f3a-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="b7f3a-131">-SourceImageId</span></span>
<span data-ttu-id="b7f3a-132">이미지 버전을 만들 원본 이미지의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="b7f3a-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b7f3a-133">-StorageAccountType</span></span>
<span data-ttu-id="b7f3a-134">이미지를 저장 하는 데 사용할 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-134">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="b7f3a-135">이 속성은 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-135">This property is not updatable.</span></span> <span data-ttu-id="b7f3a-136">사용할 수 있는 값은 Standard_LRS 및 Standard_ZRS입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-136">Available values are Standard_LRS and Standard_ZRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f3a-137">태그</span><span class="sxs-lookup"><span data-stu-id="b7f3a-137">-Tag</span></span>
<span data-ttu-id="b7f3a-138">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="b7f3a-138">Resource tags</span></span>

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

### <span data-ttu-id="b7f3a-139">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="b7f3a-139">-TargetRegion</span></span>
<span data-ttu-id="b7f3a-140">이미지 버전이 복제 될 대상 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-140">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="b7f3a-141">-확인</span><span class="sxs-lookup"><span data-stu-id="b7f3a-141">-Confirm</span></span>
<span data-ttu-id="b7f3a-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f3a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f3a-143">-WhatIf</span></span>
<span data-ttu-id="b7f3a-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7f3a-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f3a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f3a-146">CommonParameters</span></span>
<span data-ttu-id="b7f3a-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f3a-148">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f3a-149">입력</span><span class="sxs-lookup"><span data-stu-id="b7f3a-149">INPUTS</span></span>

### <span data-ttu-id="b7f3a-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b7f3a-150">System.String</span></span>

### <span data-ttu-id="b7f3a-151">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="b7f3a-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b7f3a-152">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-152">System.Int32</span></span>

### <span data-ttu-id="b7f3a-153">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7f3a-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b7f3a-154">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="b7f3a-154">System.DateTime</span></span>

### <span data-ttu-id="b7f3a-155">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="b7f3a-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="b7f3a-156">출력</span><span class="sxs-lookup"><span data-stu-id="b7f3a-156">OUTPUTS</span></span>

### <span data-ttu-id="b7f3a-157">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="b7f3a-158">상속자</span><span class="sxs-lookup"><span data-stu-id="b7f3a-158">NOTES</span></span>

## <span data-ttu-id="b7f3a-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7f3a-159">RELATED LINKS</span></span>
