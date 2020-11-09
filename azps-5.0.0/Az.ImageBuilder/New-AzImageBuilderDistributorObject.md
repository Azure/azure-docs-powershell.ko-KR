---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304025"
---
# <span data-ttu-id="a520e-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="a520e-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="a520e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a520e-102">SYNOPSIS</span></span>
<span data-ttu-id="a520e-103">일반 배포 개체</span><span class="sxs-lookup"><span data-stu-id="a520e-103">Generic distribution object</span></span>

## <span data-ttu-id="a520e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a520e-104">SYNTAX</span></span>

### <span data-ttu-id="a520e-105">ManagedImageDistributor (기본값)</span><span class="sxs-lookup"><span data-stu-id="a520e-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="a520e-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="a520e-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="a520e-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="a520e-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="a520e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a520e-108">DESCRIPTION</span></span>
<span data-ttu-id="a520e-109">일반 배포 개체</span><span class="sxs-lookup"><span data-stu-id="a520e-109">Generic distribution object</span></span>

## <span data-ttu-id="a520e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a520e-110">EXAMPLES</span></span>

### <span data-ttu-id="a520e-111">예제 1: 관리 되는 이미지 배포자 만들기</span><span class="sxs-lookup"><span data-stu-id="a520e-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="a520e-112">이 명령은 관리 되는 이미지 배포자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="a520e-113">예제 2: VHD 배포자 만들기</span><span class="sxs-lookup"><span data-stu-id="a520e-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="a520e-114">이 명령은 VHD 배포자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="a520e-115">예제 3: 공유 이미지 배포자 만들기</span><span class="sxs-lookup"><span data-stu-id="a520e-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="a520e-116">이 명령은 공유 이미지 배포자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="a520e-117">변수</span><span class="sxs-lookup"><span data-stu-id="a520e-117">PARAMETERS</span></span>

### <span data-ttu-id="a520e-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="a520e-118">-ArtifactTag</span></span>
<span data-ttu-id="a520e-119">배포자에 의해 생성/업데이트 된 후 아티팩트에 적용 되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="a520e-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="a520e-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="a520e-121">생성 된 이미지 버전을 최신에서 제외할지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="a520e-122">Default (false)를 사용 하지 않는 경우 생략 합니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="a520e-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="a520e-123">-GalleryImageId</span></span>
<span data-ttu-id="a520e-124">공유 이미지 갤러리 이미지의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="a520e-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="a520e-125">-ImageId</span></span>
<span data-ttu-id="a520e-126">관리 되는 디스크 이미지의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="a520e-127">-위치</span><span class="sxs-lookup"><span data-stu-id="a520e-127">-Location</span></span>
<span data-ttu-id="a520e-128">이미지가 이미 있는 경우 이미지에 대 한 Azure 위치가 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="a520e-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="a520e-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="a520e-130">관리 되는 디스크 이미지로 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="a520e-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="a520e-131">-ReplicationRegion</span></span>
<span data-ttu-id="a520e-132">이미지가 복제 되는 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="a520e-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="a520e-133">-RunOutputName</span></span>
<span data-ttu-id="a520e-134">연결 된 RunOutput에 사용 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="a520e-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="a520e-135">-SharedImageDistributor</span></span>
<span data-ttu-id="a520e-136">공유 이미지 갤러리를 통해 배포</span><span class="sxs-lookup"><span data-stu-id="a520e-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="a520e-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a520e-137">-StorageAccountType</span></span>
<span data-ttu-id="a520e-138">공유 이미지를 저장 하는 데 사용 되는 저장소 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="a520e-139">Default (Standard_LRS)를 사용 하려면 생략 합니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="a520e-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="a520e-140">-VhdDistributor</span></span>
<span data-ttu-id="a520e-141">저장소 계정에서 VHD를 통해 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="a520e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a520e-142">CommonParameters</span></span>
<span data-ttu-id="a520e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a520e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a520e-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a520e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a520e-145">입력</span><span class="sxs-lookup"><span data-stu-id="a520e-145">INPUTS</span></span>

## <span data-ttu-id="a520e-146">출력</span><span class="sxs-lookup"><span data-stu-id="a520e-146">OUTPUTS</span></span>

### <span data-ttu-id="a520e-147">Api20200214. IImageTemplateDistributor에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a520e-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="a520e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="a520e-148">NOTES</span></span>

<span data-ttu-id="a520e-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="a520e-149">ALIASES</span></span>

## <span data-ttu-id="a520e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a520e-150">RELATED LINKS</span></span>

