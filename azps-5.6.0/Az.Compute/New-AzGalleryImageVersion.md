---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 95622cba86c39b52b850b017ac370ea71dc2f84d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977579"
---
# <span data-ttu-id="5ff66-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5ff66-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="5ff66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ff66-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff66-103">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-103">Create a gallery image version.</span></span>

## <span data-ttu-id="5ff66-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ff66-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff66-105">설명</span><span class="sxs-lookup"><span data-stu-id="5ff66-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff66-106">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-106">Create a gallery image version.</span></span>

## <span data-ttu-id="5ff66-107">예제</span><span class="sxs-lookup"><span data-stu-id="5ff66-107">EXAMPLES</span></span>

### <span data-ttu-id="5ff66-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ff66-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="5ff66-109">갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-109">Create a gallery image version.</span></span>

### <span data-ttu-id="5ff66-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="5ff66-110">Example 2</span></span>
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

<span data-ttu-id="5ff66-111">디스크 이미지 암호화를 사용하여 갤러리 이미지 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="5ff66-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5ff66-112">PARAMETERS</span></span>

### <span data-ttu-id="5ff66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ff66-113">-AsJob</span></span>
<span data-ttu-id="5ff66-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5ff66-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ff66-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="5ff66-115">-DataDiskImage</span></span>
<span data-ttu-id="5ff66-116">데이터 디스크 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-116">Data disk images.</span></span>   <span data-ttu-id="5ff66-117">예: @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="5ff66-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="5ff66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff66-118">-DefaultProfile</span></span>
<span data-ttu-id="5ff66-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff66-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5ff66-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="5ff66-121">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="5ff66-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="5ff66-122">-GalleryName</span></span>
<span data-ttu-id="5ff66-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="5ff66-124">-Location</span><span class="sxs-lookup"><span data-stu-id="5ff66-124">-Location</span></span>
<span data-ttu-id="5ff66-125">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="5ff66-125">Resource location</span></span>

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

### <span data-ttu-id="5ff66-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5ff66-126">-Name</span></span>
<span data-ttu-id="5ff66-127">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="5ff66-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="5ff66-128">-OSDiskImage</span></span>
<span data-ttu-id="5ff66-129">OS 디스크 이미지(예: @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="5ff66-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="5ff66-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="5ff66-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="5ff66-131">갤러리 이미지 버전의 수명이 종료된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="5ff66-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="5ff66-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="5ff66-133">설정되어 있는 경우 최신 버전의 이미지 정의에서 배포된 Virtual Machines는 이 이미지 버전을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="5ff66-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5ff66-134">-ReplicaCount</span></span>
<span data-ttu-id="5ff66-135">지역별로 만들 이미지 버전의 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="5ff66-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff66-136">-ResourceGroupName</span></span>
<span data-ttu-id="5ff66-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ff66-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="5ff66-138">-SourceImageId</span></span>
<span data-ttu-id="5ff66-139">이미지 버전을 만들 원본 이미지의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="5ff66-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5ff66-140">-StorageAccountType</span></span>
<span data-ttu-id="5ff66-141">이미지를 저장하는 데 사용할 저장소 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="5ff66-142">이 속성은 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-142">This property is not updatable.</span></span> <span data-ttu-id="5ff66-143">사용 가능한 값은 Standard_LRS, Standard_ZRS 및 Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="5ff66-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="5ff66-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ff66-144">-Tag</span></span>
<span data-ttu-id="5ff66-145">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="5ff66-145">Resource tags</span></span>

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

### <span data-ttu-id="5ff66-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="5ff66-146">-TargetRegion</span></span>
<span data-ttu-id="5ff66-147">이미지 버전이 복제될 대상 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="5ff66-148">-확인</span><span class="sxs-lookup"><span data-stu-id="5ff66-148">-Confirm</span></span>
<span data-ttu-id="5ff66-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff66-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff66-150">-WhatIf</span></span>
<span data-ttu-id="5ff66-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff66-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff66-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff66-153">CommonParameters</span></span>
<span data-ttu-id="5ff66-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff66-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff66-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ff66-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff66-156">입력</span><span class="sxs-lookup"><span data-stu-id="5ff66-156">INPUTS</span></span>

### <span data-ttu-id="5ff66-157">System.String</span><span class="sxs-lookup"><span data-stu-id="5ff66-157">System.String</span></span>

### <span data-ttu-id="5ff66-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ff66-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ff66-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5ff66-159">System.Int32</span></span>

### <span data-ttu-id="5ff66-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ff66-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5ff66-161">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="5ff66-161">System.DateTime</span></span>

### <span data-ttu-id="5ff66-162">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="5ff66-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="5ff66-163">출력</span><span class="sxs-lookup"><span data-stu-id="5ff66-163">OUTPUTS</span></span>

### <span data-ttu-id="5ff66-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5ff66-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="5ff66-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ff66-165">NOTES</span></span>

## <span data-ttu-id="5ff66-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ff66-166">RELATED LINKS</span></span>
