---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492905"
---
# <span data-ttu-id="fb093-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="fb093-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="fb093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb093-102">SYNOPSIS</span></span>
<span data-ttu-id="fb093-103">일반 배포 개체</span><span class="sxs-lookup"><span data-stu-id="fb093-103">Generic distribution object</span></span>

## <span data-ttu-id="fb093-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb093-104">SYNTAX</span></span>

### <span data-ttu-id="fb093-105">ManagedImageDistributor(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb093-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="fb093-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="fb093-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="fb093-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="fb093-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="fb093-108">설명</span><span class="sxs-lookup"><span data-stu-id="fb093-108">DESCRIPTION</span></span>
<span data-ttu-id="fb093-109">일반 배포 개체</span><span class="sxs-lookup"><span data-stu-id="fb093-109">Generic distribution object</span></span>

## <span data-ttu-id="fb093-110">예제</span><span class="sxs-lookup"><span data-stu-id="fb093-110">EXAMPLES</span></span>

### <span data-ttu-id="fb093-111">예제 1: 관리되는 이미지 배포자 만들기</span><span class="sxs-lookup"><span data-stu-id="fb093-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="fb093-112">이 명령은 관리되는 이미지 배포자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="fb093-113">예제 2: VHD 배포자 만들기</span><span class="sxs-lookup"><span data-stu-id="fb093-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="fb093-114">이 명령은 VHD 배포자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="fb093-115">예제 3: 공유 이미지 배포자 만들기</span><span class="sxs-lookup"><span data-stu-id="fb093-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="fb093-116">이 명령은 공유 이미지 배포자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="fb093-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb093-117">PARAMETERS</span></span>

### <span data-ttu-id="fb093-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="fb093-118">-ArtifactTag</span></span>
<span data-ttu-id="fb093-119">배포자가 아티팩트를 생성/업데이트한 후 아티팩트에 적용할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="fb093-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="fb093-121">만든 이미지 버전을 최신에서 제외해야 하는지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="fb093-122">기본값(false)을 사용하기 위해 생략합니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="fb093-123">-GalleryImageId</span></span>
<span data-ttu-id="fb093-124">공유 이미지 갤러리 이미지의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="fb093-125">-ImageId</span></span>
<span data-ttu-id="fb093-126">Managed Disk 이미지의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-127">-Location</span><span class="sxs-lookup"><span data-stu-id="fb093-127">-Location</span></span>
<span data-ttu-id="fb093-128">이미지에 대한 Azure 위치는 이미지가 이미 있는 경우 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="fb093-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="fb093-130">Managed Disk 이미지로 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="fb093-131">-ReplicationRegion</span></span>
<span data-ttu-id="fb093-132">이미지가 복제될 지역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="fb093-133">-RunOutputName</span></span>
<span data-ttu-id="fb093-134">연결된 RunOutput에 사용할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="fb093-135">-SharedImageDistributor</span></span>
<span data-ttu-id="fb093-136">공유 이미지 갤러리를 통해 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fb093-137">-StorageAccountType</span></span>
<span data-ttu-id="fb093-138">공유 이미지를 저장하는 데 사용할 저장소 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="fb093-139">기본값(Standard_LRS) 사용은 생략합니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="fb093-140">-VhdDistributor</span></span>
<span data-ttu-id="fb093-141">저장소 계정의 VHD를 통해 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb093-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb093-142">CommonParameters</span></span>
<span data-ttu-id="fb093-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb093-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb093-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb093-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb093-145">입력</span><span class="sxs-lookup"><span data-stu-id="fb093-145">INPUTS</span></span>

## <span data-ttu-id="fb093-146">출력</span><span class="sxs-lookup"><span data-stu-id="fb093-146">OUTPUTS</span></span>

### <span data-ttu-id="fb093-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="fb093-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="fb093-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb093-148">NOTES</span></span>

<span data-ttu-id="fb093-149">별칭</span><span class="sxs-lookup"><span data-stu-id="fb093-149">ALIASES</span></span>

## <span data-ttu-id="fb093-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb093-150">RELATED LINKS</span></span>

