---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 8dcfe4adedd7da375e888dade108125d7899d7d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536727"
---
# <span data-ttu-id="310f0-101">New-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="310f0-101">New-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="310f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="310f0-102">SYNOPSIS</span></span>
<span data-ttu-id="310f0-103">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-103">Create a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="310f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="310f0-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Location] <String> -Publisher <String> -Offer <String> -Sku <String>
 -OsState <OperatingSystemStateTypes> -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="310f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="310f0-105">DESCRIPTION</span></span>
<span data-ttu-id="310f0-106">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="310f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="310f0-107">EXAMPLES</span></span>

### <span data-ttu-id="310f0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="310f0-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="310f0-109">갤러리 이미지 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="310f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="310f0-110">PARAMETERS</span></span>

### <span data-ttu-id="310f0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="310f0-111">-AsJob</span></span>
<span data-ttu-id="310f0-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="310f0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="310f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310f0-113">-DefaultProfile</span></span>
<span data-ttu-id="310f0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310f0-115">-설명</span><span class="sxs-lookup"><span data-stu-id="310f0-115">-Description</span></span>
<span data-ttu-id="310f0-116">갤러리 이미지 정의 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="310f0-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="310f0-117">-DisallowedDiskType</span></span>
<span data-ttu-id="310f0-118">허용 되지 않는 디스크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="310f0-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="310f0-119">-EndOfLifeDate</span></span>
<span data-ttu-id="310f0-120">갤러리 이미지 정의의 기간 종료 날짜</span><span class="sxs-lookup"><span data-stu-id="310f0-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="310f0-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="310f0-121">-Eula</span></span>
<span data-ttu-id="310f0-122">갤러리 이미지 정의에 대 한 Eula 계약입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="310f0-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="310f0-123">-GalleryName</span></span>
<span data-ttu-id="310f0-124">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="310f0-125">-위치</span><span class="sxs-lookup"><span data-stu-id="310f0-125">-Location</span></span>
<span data-ttu-id="310f0-126">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="310f0-126">Resource location</span></span>

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

### <span data-ttu-id="310f0-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="310f0-127">-MaximumMemory</span></span>
<span data-ttu-id="310f0-128">권장 되는 메모리의 최대 개수</span><span class="sxs-lookup"><span data-stu-id="310f0-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="310f0-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="310f0-129">-MaximumVCPU</span></span>
<span data-ttu-id="310f0-130">권장 되는 CPU 코어의 최대</span><span class="sxs-lookup"><span data-stu-id="310f0-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="310f0-131">-가을 메모리</span><span class="sxs-lookup"><span data-stu-id="310f0-131">-MinimumMemory</span></span>
<span data-ttu-id="310f0-132">권장 되는 메모리의 최소 개수</span><span class="sxs-lookup"><span data-stu-id="310f0-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="310f0-133">-없음 Vcpu</span><span class="sxs-lookup"><span data-stu-id="310f0-133">-MinimumVCPU</span></span>
<span data-ttu-id="310f0-134">권장 되는 CPU 코어의 최소</span><span class="sxs-lookup"><span data-stu-id="310f0-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="310f0-135">-이름</span><span class="sxs-lookup"><span data-stu-id="310f0-135">-Name</span></span>
<span data-ttu-id="310f0-136">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="310f0-137">-제공</span><span class="sxs-lookup"><span data-stu-id="310f0-137">-Offer</span></span>
<span data-ttu-id="310f0-138">갤러리 이미지 정의 제공의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="310f0-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="310f0-139">-OsState</span></span>
<span data-ttu-id="310f0-140">OS의 상태</span><span class="sxs-lookup"><span data-stu-id="310f0-140">The state of OS</span></span>

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

### <span data-ttu-id="310f0-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="310f0-141">-OsType</span></span>
<span data-ttu-id="310f0-142">OS 유형</span><span class="sxs-lookup"><span data-stu-id="310f0-142">The type of OS</span></span>

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

### <span data-ttu-id="310f0-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="310f0-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="310f0-144">개인 정보 취급 방침 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="310f0-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="310f0-145">-Publisher</span></span>
<span data-ttu-id="310f0-146">갤러리 이미지 정의 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="310f0-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="310f0-147">-PurchasePlanName</span></span>
<span data-ttu-id="310f0-148">구매 계획의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="310f0-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="310f0-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="310f0-150">구매 플랜의 제품 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="310f0-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="310f0-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="310f0-152">구매 계획의 게시자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="310f0-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="310f0-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="310f0-154">릴리스 노트 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-154">The release note uri.</span></span>

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

### <span data-ttu-id="310f0-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310f0-155">-ResourceGroupName</span></span>
<span data-ttu-id="310f0-156">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="310f0-157">-Sku</span><span class="sxs-lookup"><span data-stu-id="310f0-157">-Sku</span></span>
<span data-ttu-id="310f0-158">갤러리 이미지 정의 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="310f0-159">태그</span><span class="sxs-lookup"><span data-stu-id="310f0-159">-Tag</span></span>
<span data-ttu-id="310f0-160">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="310f0-160">Resource tags</span></span>

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

### <span data-ttu-id="310f0-161">-확인</span><span class="sxs-lookup"><span data-stu-id="310f0-161">-Confirm</span></span>
<span data-ttu-id="310f0-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310f0-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310f0-163">-WhatIf</span></span>
<span data-ttu-id="310f0-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310f0-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310f0-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310f0-166">CommonParameters</span></span>
<span data-ttu-id="310f0-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310f0-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310f0-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310f0-169">입력</span><span class="sxs-lookup"><span data-stu-id="310f0-169">INPUTS</span></span>

### <span data-ttu-id="310f0-170">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="310f0-170">System.String</span></span>

### <span data-ttu-id="310f0-171">OperatingSystemStateTypes를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="310f0-172">OperatingSystemTypes를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="310f0-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="310f0-173">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="310f0-173">System.DateTime</span></span>

### <span data-ttu-id="310f0-174">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="310f0-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="310f0-175">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="310f0-175">System.Int32</span></span>

### <span data-ttu-id="310f0-176">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="310f0-176">System.String[]</span></span>

## <span data-ttu-id="310f0-177">출력</span><span class="sxs-lookup"><span data-stu-id="310f0-177">OUTPUTS</span></span>

### <span data-ttu-id="310f0-178">PSGalleryImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="310f0-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="310f0-179">상속자</span><span class="sxs-lookup"><span data-stu-id="310f0-179">NOTES</span></span>

## <span data-ttu-id="310f0-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="310f0-180">RELATED LINKS</span></span>
