---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: fbfb0a10016d81edcffeb62580b1ca0ff9b5b341
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957568"
---
# <span data-ttu-id="2f7be-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="2f7be-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="2f7be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f7be-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7be-103">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="2f7be-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f7be-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f7be-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f7be-105">DESCRIPTION</span></span>
<span data-ttu-id="2f7be-106">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="2f7be-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f7be-107">EXAMPLES</span></span>

### <span data-ttu-id="2f7be-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f7be-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="2f7be-109">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="2f7be-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f7be-110">PARAMETERS</span></span>

### <span data-ttu-id="2f7be-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f7be-111">-AsJob</span></span>
<span data-ttu-id="2f7be-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2f7be-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f7be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7be-113">-DefaultProfile</span></span>
<span data-ttu-id="2f7be-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f7be-115">-Description</span><span class="sxs-lookup"><span data-stu-id="2f7be-115">-Description</span></span>
<span data-ttu-id="2f7be-116">갤러리 이미지 정의 리소스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="2f7be-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="2f7be-117">-DisallowedDiskType</span></span>
<span data-ttu-id="2f7be-118">사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-118">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7be-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="2f7be-119">-EndOfLifeDate</span></span>
<span data-ttu-id="2f7be-120">갤러리 이미지 정의의 수명 종료 날짜</span><span class="sxs-lookup"><span data-stu-id="2f7be-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="2f7be-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="2f7be-121">-Eula</span></span>
<span data-ttu-id="2f7be-122">갤러리 이미지 정의에 대한 Eula 계약입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="2f7be-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="2f7be-123">-GalleryName</span></span>
<span data-ttu-id="2f7be-124">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="2f7be-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="2f7be-125">-HyperVGeneration</span></span>
<span data-ttu-id="2f7be-126">Virtual Machine의 하이퍼바이서 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="2f7be-127">OS 디스크에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="2f7be-128">허용되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="2f7be-129">-Location</span><span class="sxs-lookup"><span data-stu-id="2f7be-129">-Location</span></span>
<span data-ttu-id="2f7be-130">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="2f7be-130">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7be-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="2f7be-131">-MaximumMemory</span></span>
<span data-ttu-id="2f7be-132">권장되는 메모리의 최대값</span><span class="sxs-lookup"><span data-stu-id="2f7be-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="2f7be-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="2f7be-133">-MaximumVCPU</span></span>
<span data-ttu-id="2f7be-134">권장되는 CPU 코어의 최대값</span><span class="sxs-lookup"><span data-stu-id="2f7be-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="2f7be-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="2f7be-135">-MinimumMemory</span></span>
<span data-ttu-id="2f7be-136">권장되는 메모리의 최소값</span><span class="sxs-lookup"><span data-stu-id="2f7be-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="2f7be-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="2f7be-137">-MinimumVCPU</span></span>
<span data-ttu-id="2f7be-138">권장되는 CPU 코어의 최소값</span><span class="sxs-lookup"><span data-stu-id="2f7be-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="2f7be-139">-Name</span><span class="sxs-lookup"><span data-stu-id="2f7be-139">-Name</span></span>
<span data-ttu-id="2f7be-140">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-140">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7be-141">-제품</span><span class="sxs-lookup"><span data-stu-id="2f7be-141">-Offer</span></span>
<span data-ttu-id="2f7be-142">갤러리 이미지 정의 제품 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="2f7be-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="2f7be-143">-OsState</span></span>
<span data-ttu-id="2f7be-144">OS 상태</span><span class="sxs-lookup"><span data-stu-id="2f7be-144">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7be-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="2f7be-145">-OsType</span></span>
<span data-ttu-id="2f7be-146">OS 유형</span><span class="sxs-lookup"><span data-stu-id="2f7be-146">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7be-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="2f7be-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="2f7be-148">개인 정보 취급 방침 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="2f7be-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2f7be-149">-Publisher</span></span>
<span data-ttu-id="2f7be-150">갤러리 이미지 정의 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="2f7be-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="2f7be-151">-PurchasePlanName</span></span>
<span data-ttu-id="2f7be-152">구매 계획의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="2f7be-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="2f7be-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="2f7be-154">구매 계획의 제품 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="2f7be-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="2f7be-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="2f7be-156">구매 계획의 게시자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="2f7be-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="2f7be-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="2f7be-158">릴리스 참고 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-158">The release note uri.</span></span>

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

### <span data-ttu-id="2f7be-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f7be-159">-ResourceGroupName</span></span>
<span data-ttu-id="2f7be-160">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f7be-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="2f7be-161">-Sku</span></span>
<span data-ttu-id="2f7be-162">갤러리 이미지 정의 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="2f7be-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f7be-163">-Tag</span></span>
<span data-ttu-id="2f7be-164">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="2f7be-164">Resource tags</span></span>

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

### <span data-ttu-id="2f7be-165">-확인</span><span class="sxs-lookup"><span data-stu-id="2f7be-165">-Confirm</span></span>
<span data-ttu-id="2f7be-166">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f7be-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f7be-167">-WhatIf</span></span>
<span data-ttu-id="2f7be-168">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f7be-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f7be-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7be-170">CommonParameters</span></span>
<span data-ttu-id="2f7be-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f7be-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7be-172">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f7be-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7be-173">입력</span><span class="sxs-lookup"><span data-stu-id="2f7be-173">INPUTS</span></span>

### <span data-ttu-id="2f7be-174">System.String</span><span class="sxs-lookup"><span data-stu-id="2f7be-174">System.String</span></span>

### <span data-ttu-id="2f7be-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="2f7be-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="2f7be-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="2f7be-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="2f7be-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="2f7be-177">System.DateTime</span></span>

### <span data-ttu-id="2f7be-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f7be-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2f7be-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2f7be-179">System.Int32</span></span>

### <span data-ttu-id="2f7be-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2f7be-180">System.String[]</span></span>

## <span data-ttu-id="2f7be-181">출력</span><span class="sxs-lookup"><span data-stu-id="2f7be-181">OUTPUTS</span></span>

### <span data-ttu-id="2f7be-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="2f7be-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="2f7be-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f7be-183">NOTES</span></span>

## <span data-ttu-id="2f7be-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f7be-184">RELATED LINKS</span></span>
