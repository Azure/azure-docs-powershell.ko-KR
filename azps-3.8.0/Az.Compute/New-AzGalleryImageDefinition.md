---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034026"
---
# <span data-ttu-id="ae82a-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ae82a-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="ae82a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae82a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae82a-103">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="ae82a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae82a-104">SYNTAX</span></span>

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

## <span data-ttu-id="ae82a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae82a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae82a-106">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="ae82a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ae82a-107">EXAMPLES</span></span>

### <span data-ttu-id="ae82a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae82a-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="ae82a-109">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="ae82a-110">변수</span><span class="sxs-lookup"><span data-stu-id="ae82a-110">PARAMETERS</span></span>

### <span data-ttu-id="ae82a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae82a-111">-AsJob</span></span>
<span data-ttu-id="ae82a-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ae82a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae82a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae82a-113">-DefaultProfile</span></span>
<span data-ttu-id="ae82a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae82a-115">-설명</span><span class="sxs-lookup"><span data-stu-id="ae82a-115">-Description</span></span>
<span data-ttu-id="ae82a-116">갤러리 이미지 정의 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="ae82a-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="ae82a-117">-DisallowedDiskType</span></span>
<span data-ttu-id="ae82a-118">허용 되지 않는 디스크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="ae82a-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="ae82a-119">-EndOfLifeDate</span></span>
<span data-ttu-id="ae82a-120">갤러리 이미지 정의의 기간 종료 날짜</span><span class="sxs-lookup"><span data-stu-id="ae82a-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="ae82a-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="ae82a-121">-Eula</span></span>
<span data-ttu-id="ae82a-122">갤러리 이미지 정의에 대 한 Eula 계약입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="ae82a-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="ae82a-123">-GalleryName</span></span>
<span data-ttu-id="ae82a-124">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="ae82a-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="ae82a-125">-HyperVGeneration</span></span>
<span data-ttu-id="ae82a-126">가상 컴퓨터의 하이퍼바이저 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="ae82a-127">OS 디스크에만 적용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="ae82a-128">허용 되는 값은 V1 및 V2입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="ae82a-129">-위치</span><span class="sxs-lookup"><span data-stu-id="ae82a-129">-Location</span></span>
<span data-ttu-id="ae82a-130">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="ae82a-130">Resource location</span></span>

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

### <span data-ttu-id="ae82a-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="ae82a-131">-MaximumMemory</span></span>
<span data-ttu-id="ae82a-132">권장 되는 메모리의 최대 개수</span><span class="sxs-lookup"><span data-stu-id="ae82a-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="ae82a-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="ae82a-133">-MaximumVCPU</span></span>
<span data-ttu-id="ae82a-134">권장 되는 CPU 코어의 최대</span><span class="sxs-lookup"><span data-stu-id="ae82a-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ae82a-135">-가을 메모리</span><span class="sxs-lookup"><span data-stu-id="ae82a-135">-MinimumMemory</span></span>
<span data-ttu-id="ae82a-136">권장 되는 메모리의 최소 개수</span><span class="sxs-lookup"><span data-stu-id="ae82a-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="ae82a-137">-없음 Vcpu</span><span class="sxs-lookup"><span data-stu-id="ae82a-137">-MinimumVCPU</span></span>
<span data-ttu-id="ae82a-138">권장 되는 CPU 코어의 최소</span><span class="sxs-lookup"><span data-stu-id="ae82a-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ae82a-139">-이름</span><span class="sxs-lookup"><span data-stu-id="ae82a-139">-Name</span></span>
<span data-ttu-id="ae82a-140">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="ae82a-141">-제공</span><span class="sxs-lookup"><span data-stu-id="ae82a-141">-Offer</span></span>
<span data-ttu-id="ae82a-142">갤러리 이미지 정의 제공의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="ae82a-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="ae82a-143">-OsState</span></span>
<span data-ttu-id="ae82a-144">OS의 상태</span><span class="sxs-lookup"><span data-stu-id="ae82a-144">The state of OS</span></span>

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

### <span data-ttu-id="ae82a-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="ae82a-145">-OsType</span></span>
<span data-ttu-id="ae82a-146">OS 유형</span><span class="sxs-lookup"><span data-stu-id="ae82a-146">The type of OS</span></span>

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

### <span data-ttu-id="ae82a-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="ae82a-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="ae82a-148">개인 정보 취급 방침 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="ae82a-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ae82a-149">-Publisher</span></span>
<span data-ttu-id="ae82a-150">갤러리 이미지 정의 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="ae82a-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="ae82a-151">-PurchasePlanName</span></span>
<span data-ttu-id="ae82a-152">구매 계획의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ae82a-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="ae82a-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="ae82a-154">구매 플랜의 제품 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ae82a-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ae82a-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="ae82a-156">구매 계획의 게시자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ae82a-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="ae82a-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="ae82a-158">릴리스 노트 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-158">The release note uri.</span></span>

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

### <span data-ttu-id="ae82a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae82a-159">-ResourceGroupName</span></span>
<span data-ttu-id="ae82a-160">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae82a-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="ae82a-161">-Sku</span></span>
<span data-ttu-id="ae82a-162">갤러리 이미지 정의 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="ae82a-163">태그</span><span class="sxs-lookup"><span data-stu-id="ae82a-163">-Tag</span></span>
<span data-ttu-id="ae82a-164">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="ae82a-164">Resource tags</span></span>

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

### <span data-ttu-id="ae82a-165">-확인</span><span class="sxs-lookup"><span data-stu-id="ae82a-165">-Confirm</span></span>
<span data-ttu-id="ae82a-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae82a-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae82a-167">-WhatIf</span></span>
<span data-ttu-id="ae82a-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae82a-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae82a-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae82a-170">CommonParameters</span></span>
<span data-ttu-id="ae82a-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae82a-172">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae82a-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae82a-173">입력</span><span class="sxs-lookup"><span data-stu-id="ae82a-173">INPUTS</span></span>

### <span data-ttu-id="ae82a-174">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae82a-174">System.String</span></span>

### <span data-ttu-id="ae82a-175">OperatingSystemStateTypes를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="ae82a-176">OperatingSystemTypes를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae82a-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="ae82a-177">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="ae82a-177">System.DateTime</span></span>

### <span data-ttu-id="ae82a-178">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ae82a-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ae82a-179">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ae82a-179">System.Int32</span></span>

### <span data-ttu-id="ae82a-180">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="ae82a-180">System.String[]</span></span>

## <span data-ttu-id="ae82a-181">출력</span><span class="sxs-lookup"><span data-stu-id="ae82a-181">OUTPUTS</span></span>

### <span data-ttu-id="ae82a-182">PSGalleryImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="ae82a-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="ae82a-183">상속자</span><span class="sxs-lookup"><span data-stu-id="ae82a-183">NOTES</span></span>

## <span data-ttu-id="ae82a-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae82a-184">RELATED LINKS</span></span>
