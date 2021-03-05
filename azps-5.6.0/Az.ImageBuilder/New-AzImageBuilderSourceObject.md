---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013040"
---
# <span data-ttu-id="b2683-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="b2683-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="b2683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2683-102">SYNOPSIS</span></span>
<span data-ttu-id="b2683-103">구축, 사용자 지정 및 배포를 위한 가상 머신 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="b2683-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2683-104">SYNTAX</span></span>

### <span data-ttu-id="b2683-105">ManagedImage(기본값)</span><span class="sxs-lookup"><span data-stu-id="b2683-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2683-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="b2683-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2683-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="b2683-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2683-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="b2683-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="b2683-109">설명</span><span class="sxs-lookup"><span data-stu-id="b2683-109">DESCRIPTION</span></span>
<span data-ttu-id="b2683-110">구축, 사용자 지정 및 배포를 위한 가상 머신 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="b2683-111">예제</span><span class="sxs-lookup"><span data-stu-id="b2683-111">EXAMPLES</span></span>

### <span data-ttu-id="b2683-112">예제 1: 관리되는 이미지 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="b2683-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="b2683-113">이 명령은 관리되는 이미지 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="b2683-114">예제 2: 공유 이미지 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="b2683-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="b2683-115">이 명령은 공유 이미지 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="b2683-116">예제 3: platfrom 이미지 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="b2683-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="b2683-117">이 명령은 platfrom 이미지 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="b2683-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2683-118">PARAMETERS</span></span>

### <span data-ttu-id="b2683-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="b2683-119">-ImageId</span></span>
<span data-ttu-id="b2683-120">ARM 관리되는 이미지의 리소스 ID를 고객 구독에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="b2683-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="b2683-121">-ImageVersionId</span></span>
<span data-ttu-id="b2683-122">ARM 이미지 버전의 리소스 ID를 공유 이미지 갤러리에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="b2683-123">-제품</span><span class="sxs-lookup"><span data-stu-id="b2683-123">-Offer</span></span>
<span data-ttu-id="b2683-124">Azure 갤러리 이미지의 [이미지 제공.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b2683-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b2683-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b2683-125">-PlanName</span></span>
<span data-ttu-id="b2683-126">구매 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="b2683-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b2683-127">-PlanProduct</span></span>
<span data-ttu-id="b2683-128">구매 계획의 제품입니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="b2683-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b2683-129">-PlanPublisher</span></span>
<span data-ttu-id="b2683-130">구매 계획의 게시자입니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="b2683-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b2683-131">-Publisher</span></span>
<span data-ttu-id="b2683-132">Azure 갤러리 [이미지의 이미지 게시자.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b2683-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b2683-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="b2683-133">-Sku</span></span>
<span data-ttu-id="b2683-134">Azure 갤러리 이미지의 [이미지 sku입니다.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b2683-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b2683-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="b2683-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="b2683-136">고객 구독에서 관리되는 이미지인 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="b2683-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="b2683-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="b2683-138">Azure 갤러리 이미지의 [이미지 원본을 설명합니다.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b2683-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b2683-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="b2683-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="b2683-140">공유 이미지 갤러리의 이미지 버전인 이미지 원본을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="b2683-141">-Version</span><span class="sxs-lookup"><span data-stu-id="b2683-141">-Version</span></span>
<span data-ttu-id="b2683-142">Azure 갤러리 이미지의 [이미지 버전입니다.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="b2683-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="b2683-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2683-143">CommonParameters</span></span>
<span data-ttu-id="b2683-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2683-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2683-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2683-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2683-146">입력</span><span class="sxs-lookup"><span data-stu-id="b2683-146">INPUTS</span></span>

## <span data-ttu-id="b2683-147">출력</span><span class="sxs-lookup"><span data-stu-id="b2683-147">OUTPUTS</span></span>

### <span data-ttu-id="b2683-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="b2683-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="b2683-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2683-149">NOTES</span></span>

<span data-ttu-id="b2683-150">별칭</span><span class="sxs-lookup"><span data-stu-id="b2683-150">ALIASES</span></span>

## <span data-ttu-id="b2683-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2683-151">RELATED LINKS</span></span>

