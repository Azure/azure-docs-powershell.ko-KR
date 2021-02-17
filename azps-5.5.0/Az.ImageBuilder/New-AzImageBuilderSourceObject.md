---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188329"
---
# <span data-ttu-id="be7dc-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="be7dc-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="be7dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="be7dc-103">구축, 사용자 지정 및 배포를 위한 가상 머신 이미지 원본에 대해 설명하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="be7dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="be7dc-104">SYNTAX</span></span>

### <span data-ttu-id="be7dc-105">ManagedImage(기본값)</span><span class="sxs-lookup"><span data-stu-id="be7dc-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="be7dc-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="be7dc-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="be7dc-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="be7dc-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="be7dc-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="be7dc-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="be7dc-109">설명</span><span class="sxs-lookup"><span data-stu-id="be7dc-109">DESCRIPTION</span></span>
<span data-ttu-id="be7dc-110">구축, 사용자 지정 및 배포를 위한 가상 머신 이미지 원본에 대해 설명하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="be7dc-111">예제</span><span class="sxs-lookup"><span data-stu-id="be7dc-111">EXAMPLES</span></span>

### <span data-ttu-id="be7dc-112">예제 1: 관리되는 이미지 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="be7dc-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="be7dc-113">이 명령은 관리되는 이미지 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="be7dc-114">예제 2: 공유 이미지 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="be7dc-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="be7dc-115">이 명령은 공유 이미지 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="be7dc-116">예제 3: platfrom 이미지 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="be7dc-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="be7dc-117">이 명령은 platfrom 이미지 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="be7dc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be7dc-118">PARAMETERS</span></span>

### <span data-ttu-id="be7dc-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="be7dc-119">-ImageId</span></span>
<span data-ttu-id="be7dc-120">ARM 구독에서 관리되는 이미지의 리소스 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="be7dc-121">-ImageVersionId</span></span>
<span data-ttu-id="be7dc-122">ARM 이미지 버전의 리소스 ID를 공유 이미지 갤러리에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="be7dc-123">-Offer</span></span>
<span data-ttu-id="be7dc-124">Azure 갤러리 [이미지의 이미지 제품](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="be7dc-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="be7dc-125">-PlanName</span></span>
<span data-ttu-id="be7dc-126">구매 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="be7dc-127">-PlanProduct</span></span>
<span data-ttu-id="be7dc-128">구매 계획의 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="be7dc-129">-PlanPublisher</span></span>
<span data-ttu-id="be7dc-130">구매 계획의 게시자입니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="be7dc-131">-Publisher</span></span>
<span data-ttu-id="be7dc-132">Azure 갤러리 이미지의 이미지 [게시자](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="be7dc-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="be7dc-133">-Sku</span></span>
<span data-ttu-id="be7dc-134">Azure 갤러리 이미지의 [이미지 SKU입니다.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="be7dc-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="be7dc-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="be7dc-136">고객 구독에서 관리되는 이미지인 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="be7dc-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="be7dc-138">Azure 갤러리 이미지의 [이미지 원본을 설명합니다.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="be7dc-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="be7dc-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="be7dc-140">공유 이미지 갤러리의 이미지 버전인 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-141">-Version</span><span class="sxs-lookup"><span data-stu-id="be7dc-141">-Version</span></span>
<span data-ttu-id="be7dc-142">Azure 갤러리 [이미지의 이미지 버전](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="be7dc-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7dc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7dc-143">CommonParameters</span></span>
<span data-ttu-id="be7dc-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="be7dc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7dc-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be7dc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7dc-146">입력</span><span class="sxs-lookup"><span data-stu-id="be7dc-146">INPUTS</span></span>

## <span data-ttu-id="be7dc-147">출력</span><span class="sxs-lookup"><span data-stu-id="be7dc-147">OUTPUTS</span></span>

### <span data-ttu-id="be7dc-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="be7dc-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="be7dc-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="be7dc-149">NOTES</span></span>

<span data-ttu-id="be7dc-150">별칭</span><span class="sxs-lookup"><span data-stu-id="be7dc-150">ALIASES</span></span>

## <span data-ttu-id="be7dc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be7dc-151">RELATED LINKS</span></span>

