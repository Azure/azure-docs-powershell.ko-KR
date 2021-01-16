---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357043"
---
# <span data-ttu-id="6f551-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6f551-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="6f551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f551-102">SYNOPSIS</span></span>
<span data-ttu-id="6f551-103">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="6f551-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f551-104">SYNTAX</span></span>

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

## <span data-ttu-id="6f551-105">설명</span><span class="sxs-lookup"><span data-stu-id="6f551-105">DESCRIPTION</span></span>
<span data-ttu-id="6f551-106">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="6f551-107">예제</span><span class="sxs-lookup"><span data-stu-id="6f551-107">EXAMPLES</span></span>

### <span data-ttu-id="6f551-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f551-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="6f551-109">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="6f551-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f551-110">PARAMETERS</span></span>

### <span data-ttu-id="6f551-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f551-111">-AsJob</span></span>
<span data-ttu-id="6f551-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6f551-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f551-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f551-113">-DefaultProfile</span></span>
<span data-ttu-id="6f551-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f551-115">-Description</span><span class="sxs-lookup"><span data-stu-id="6f551-115">-Description</span></span>
<span data-ttu-id="6f551-116">갤러리 이미지 정의 리소스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="6f551-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="6f551-117">-DisallowedDiskType</span></span>
<span data-ttu-id="6f551-118">사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="6f551-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="6f551-119">-EndOfLifeDate</span></span>
<span data-ttu-id="6f551-120">갤러리 이미지 정의의 종료 날짜</span><span class="sxs-lookup"><span data-stu-id="6f551-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="6f551-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="6f551-121">-Eula</span></span>
<span data-ttu-id="6f551-122">갤러리 이미지 정의에 대한 Eula 규약입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="6f551-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6f551-123">-GalleryName</span></span>
<span data-ttu-id="6f551-124">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="6f551-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="6f551-125">-HyperVGeneration</span></span>
<span data-ttu-id="6f551-126">Virtual Machine의 하이퍼바이서 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="6f551-127">OS 디스크에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="6f551-128">허용되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="6f551-129">-Location</span><span class="sxs-lookup"><span data-stu-id="6f551-129">-Location</span></span>
<span data-ttu-id="6f551-130">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="6f551-130">Resource location</span></span>

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

### <span data-ttu-id="6f551-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="6f551-131">-MaximumMemory</span></span>
<span data-ttu-id="6f551-132">권장되는 메모리의 최대값</span><span class="sxs-lookup"><span data-stu-id="6f551-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="6f551-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="6f551-133">-MaximumVCPU</span></span>
<span data-ttu-id="6f551-134">권장되는 CPU 코어의 최대값</span><span class="sxs-lookup"><span data-stu-id="6f551-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="6f551-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="6f551-135">-MinimumMemory</span></span>
<span data-ttu-id="6f551-136">권장되는 메모리의 최소값</span><span class="sxs-lookup"><span data-stu-id="6f551-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="6f551-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="6f551-137">-MinimumVCPU</span></span>
<span data-ttu-id="6f551-138">권장되는 CPU 코어의 최소값</span><span class="sxs-lookup"><span data-stu-id="6f551-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="6f551-139">-Name</span><span class="sxs-lookup"><span data-stu-id="6f551-139">-Name</span></span>
<span data-ttu-id="6f551-140">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="6f551-141">-Offer</span><span class="sxs-lookup"><span data-stu-id="6f551-141">-Offer</span></span>
<span data-ttu-id="6f551-142">갤러리 이미지 정의 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="6f551-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="6f551-143">-OsState</span></span>
<span data-ttu-id="6f551-144">OS 상태</span><span class="sxs-lookup"><span data-stu-id="6f551-144">The state of OS</span></span>

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

### <span data-ttu-id="6f551-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="6f551-145">-OsType</span></span>
<span data-ttu-id="6f551-146">OS 유형</span><span class="sxs-lookup"><span data-stu-id="6f551-146">The type of OS</span></span>

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

### <span data-ttu-id="6f551-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="6f551-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="6f551-148">개인정보처리방침 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="6f551-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6f551-149">-Publisher</span></span>
<span data-ttu-id="6f551-150">갤러리 이미지 정의 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="6f551-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="6f551-151">-PurchasePlanName</span></span>
<span data-ttu-id="6f551-152">구매 계획의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6f551-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="6f551-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="6f551-154">구매 계획의 제품 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6f551-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6f551-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="6f551-156">구매 계획의 게시자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6f551-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="6f551-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="6f551-158">릴리스 참고 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-158">The release note uri.</span></span>

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

### <span data-ttu-id="6f551-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f551-159">-ResourceGroupName</span></span>
<span data-ttu-id="6f551-160">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="6f551-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="6f551-161">-Sku</span></span>
<span data-ttu-id="6f551-162">갤러리 이미지 정의 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="6f551-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f551-163">-Tag</span></span>
<span data-ttu-id="6f551-164">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="6f551-164">Resource tags</span></span>

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

### <span data-ttu-id="6f551-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f551-165">-Confirm</span></span>
<span data-ttu-id="6f551-166">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f551-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f551-167">-WhatIf</span></span>
<span data-ttu-id="6f551-168">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6f551-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f551-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f551-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f551-170">CommonParameters</span></span>
<span data-ttu-id="6f551-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f551-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f551-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f551-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f551-173">입력</span><span class="sxs-lookup"><span data-stu-id="6f551-173">INPUTS</span></span>

### <span data-ttu-id="6f551-174">System.String</span><span class="sxs-lookup"><span data-stu-id="6f551-174">System.String</span></span>

### <span data-ttu-id="6f551-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="6f551-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="6f551-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="6f551-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="6f551-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="6f551-177">System.DateTime</span></span>

### <span data-ttu-id="6f551-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6f551-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6f551-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6f551-179">System.Int32</span></span>

### <span data-ttu-id="6f551-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6f551-180">System.String[]</span></span>

## <span data-ttu-id="6f551-181">출력</span><span class="sxs-lookup"><span data-stu-id="6f551-181">OUTPUTS</span></span>

### <span data-ttu-id="6f551-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="6f551-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="6f551-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f551-183">NOTES</span></span>

## <span data-ttu-id="6f551-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f551-184">RELATED LINKS</span></span>
