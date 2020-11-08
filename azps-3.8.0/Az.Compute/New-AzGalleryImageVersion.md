---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 57520697c0107cdf81bf55e562e78bd991a73fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034924"
---
# <span data-ttu-id="5b6ac-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5b6ac-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="5b6ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6ac-103">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-103">Create a gallery image version.</span></span>

## <span data-ttu-id="5b6ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b6ac-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b6ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b6ac-105">DESCRIPTION</span></span>
<span data-ttu-id="5b6ac-106">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-106">Create a gallery image version.</span></span>

## <span data-ttu-id="5b6ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b6ac-107">EXAMPLES</span></span>

### <span data-ttu-id="5b6ac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b6ac-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="5b6ac-109">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-109">Create a gallery image version.</span></span>

### <span data-ttu-id="5b6ac-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="5b6ac-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="5b6ac-111">디스크 이미지 암호화를 사용 하 여 갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="5b6ac-112">변수</span><span class="sxs-lookup"><span data-stu-id="5b6ac-112">PARAMETERS</span></span>

### <span data-ttu-id="5b6ac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b6ac-113">-AsJob</span></span>
<span data-ttu-id="5b6ac-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b6ac-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b6ac-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="5b6ac-115">-DataDiskImage</span></span>
<span data-ttu-id="5b6ac-116">데이터 디스크 이미지</span><span class="sxs-lookup"><span data-stu-id="5b6ac-116">Data disk images.</span></span>   <span data-ttu-id="5b6ac-117">예: @ {Source = @ {Id =<source_id>}; Lun = 1, SizeInGB = 100, HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="5b6ac-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6ac-118">-DefaultProfile</span></span>
<span data-ttu-id="5b6ac-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b6ac-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5b6ac-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="5b6ac-121">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="5b6ac-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="5b6ac-122">-GalleryName</span></span>
<span data-ttu-id="5b6ac-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="5b6ac-124">-위치</span><span class="sxs-lookup"><span data-stu-id="5b6ac-124">-Location</span></span>
<span data-ttu-id="5b6ac-125">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="5b6ac-125">Resource location</span></span>

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

### <span data-ttu-id="5b6ac-126">-이름</span><span class="sxs-lookup"><span data-stu-id="5b6ac-126">-Name</span></span>
<span data-ttu-id="5b6ac-127">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="5b6ac-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="5b6ac-128">-OSDiskImage</span></span>
<span data-ttu-id="5b6ac-129">OS 디스크 이미지 예: @ {Source = @ {Id =<source_id>}; SizeInGB = 100, HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="5b6ac-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6ac-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="5b6ac-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="5b6ac-131">갤러리 이미지 버전의 기간 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="5b6ac-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="5b6ac-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="5b6ac-133">설정 된 경우 최신 버전의 이미지 정의에서 배포 된 가상 컴퓨터는이 이미지 버전을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="5b6ac-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5b6ac-134">-ReplicaCount</span></span>
<span data-ttu-id="5b6ac-135">지역별로 만들 이미지 버전의 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="5b6ac-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b6ac-136">-ResourceGroupName</span></span>
<span data-ttu-id="5b6ac-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="5b6ac-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="5b6ac-138">-SourceImageId</span></span>
<span data-ttu-id="5b6ac-139">이미지 버전을 만들 원본 이미지의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="5b6ac-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5b6ac-140">-StorageAccountType</span></span>
<span data-ttu-id="5b6ac-141">이미지를 저장 하는 데 사용할 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="5b6ac-142">이 속성은 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-142">This property is not updatable.</span></span> <span data-ttu-id="5b6ac-143">사용할 수 있는 값은 Standard_LRS 및 Standard_ZRS입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-143">Available values are Standard_LRS and Standard_ZRS.</span></span>

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

### <span data-ttu-id="5b6ac-144">태그</span><span class="sxs-lookup"><span data-stu-id="5b6ac-144">-Tag</span></span>
<span data-ttu-id="5b6ac-145">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="5b6ac-145">Resource tags</span></span>

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

### <span data-ttu-id="5b6ac-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="5b6ac-146">-TargetRegion</span></span>
<span data-ttu-id="5b6ac-147">이미지 버전이 복제 될 대상 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="5b6ac-148">-확인</span><span class="sxs-lookup"><span data-stu-id="5b6ac-148">-Confirm</span></span>
<span data-ttu-id="5b6ac-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b6ac-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b6ac-150">-WhatIf</span></span>
<span data-ttu-id="5b6ac-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b6ac-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b6ac-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6ac-153">CommonParameters</span></span>
<span data-ttu-id="5b6ac-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6ac-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6ac-156">입력</span><span class="sxs-lookup"><span data-stu-id="5b6ac-156">INPUTS</span></span>

### <span data-ttu-id="5b6ac-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b6ac-157">System.String</span></span>

### <span data-ttu-id="5b6ac-158">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="5b6ac-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5b6ac-159">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-159">System.Int32</span></span>

### <span data-ttu-id="5b6ac-160">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b6ac-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5b6ac-161">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="5b6ac-161">System.DateTime</span></span>

### <span data-ttu-id="5b6ac-162">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="5b6ac-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="5b6ac-163">출력</span><span class="sxs-lookup"><span data-stu-id="5b6ac-163">OUTPUTS</span></span>

### <span data-ttu-id="5b6ac-164">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="5b6ac-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="5b6ac-165">상속자</span><span class="sxs-lookup"><span data-stu-id="5b6ac-165">NOTES</span></span>

## <span data-ttu-id="5b6ac-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b6ac-166">RELATED LINKS</span></span>
