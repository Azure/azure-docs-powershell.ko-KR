---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181532"
---
# <span data-ttu-id="b105d-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b105d-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="b105d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b105d-102">SYNOPSIS</span></span>
<span data-ttu-id="b105d-103">갤러리 이미지 버전을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-103">Update a gallery image version.</span></span>

## <span data-ttu-id="b105d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b105d-104">SYNTAX</span></span>

### <span data-ttu-id="b105d-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="b105d-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b105d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b105d-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b105d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b105d-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b105d-108">설명</span><span class="sxs-lookup"><span data-stu-id="b105d-108">DESCRIPTION</span></span>
<span data-ttu-id="b105d-109">갤러리 이미지 버전을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-109">Update a gallery image version.</span></span>

## <span data-ttu-id="b105d-110">예제</span><span class="sxs-lookup"><span data-stu-id="b105d-110">EXAMPLES</span></span>

### <span data-ttu-id="b105d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b105d-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="b105d-112">갤러리 이미지 버전을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-112">Update a gallery image version.</span></span>

## <span data-ttu-id="b105d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b105d-113">PARAMETERS</span></span>

### <span data-ttu-id="b105d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b105d-114">-AsJob</span></span>
<span data-ttu-id="b105d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b105d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b105d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b105d-116">-DefaultProfile</span></span>
<span data-ttu-id="b105d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b105d-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b105d-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="b105d-119">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b105d-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b105d-120">-GalleryName</span></span>
<span data-ttu-id="b105d-121">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b105d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b105d-122">-InputObject</span></span>
<span data-ttu-id="b105d-123">PS 갤러리 이미지 버전 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b105d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b105d-124">-Name</span></span>
<span data-ttu-id="b105d-125">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b105d-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="b105d-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="b105d-127">갤러리 이미지 버전의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="b105d-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="b105d-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="b105d-129">설정되어 있는 경우 최신 버전의 이미지 정의에서 배포된 Virtual Machines는 이 이미지 버전을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="b105d-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b105d-130">-ReplicaCount</span></span>
<span data-ttu-id="b105d-131">지역당 만들 이미지 버전의 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="b105d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b105d-132">-ResourceGroupName</span></span>
<span data-ttu-id="b105d-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b105d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b105d-134">-ResourceId</span></span>
<span data-ttu-id="b105d-135">갤러리 이미지 버전에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b105d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="b105d-136">-Tag</span></span>
<span data-ttu-id="b105d-137">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="b105d-137">Resource tags</span></span>

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

### <span data-ttu-id="b105d-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="b105d-138">-TargetRegion</span></span>
<span data-ttu-id="b105d-139">이미지 버전을 복제할 대상 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="b105d-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b105d-140">-Confirm</span></span>
<span data-ttu-id="b105d-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b105d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b105d-142">-WhatIf</span></span>
<span data-ttu-id="b105d-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b105d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b105d-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b105d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b105d-145">CommonParameters</span></span>
<span data-ttu-id="b105d-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b105d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b105d-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b105d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b105d-148">입력</span><span class="sxs-lookup"><span data-stu-id="b105d-148">INPUTS</span></span>

### <span data-ttu-id="b105d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b105d-149">System.String</span></span>

### <span data-ttu-id="b105d-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b105d-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="b105d-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b105d-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b105d-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b105d-152">System.Int32</span></span>

### <span data-ttu-id="b105d-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b105d-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b105d-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="b105d-154">System.DateTime</span></span>

### <span data-ttu-id="b105d-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="b105d-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="b105d-156">출력</span><span class="sxs-lookup"><span data-stu-id="b105d-156">OUTPUTS</span></span>

### <span data-ttu-id="b105d-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b105d-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="b105d-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b105d-158">NOTES</span></span>

## <span data-ttu-id="b105d-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b105d-159">RELATED LINKS</span></span>
