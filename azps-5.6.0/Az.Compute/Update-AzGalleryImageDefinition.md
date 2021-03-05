---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 09871f6d7876b5f197af515f531c85b8bf6a3d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972064"
---
# <span data-ttu-id="ae9e5-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ae9e5-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="ae9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9e5-103">갤러리 이미지 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="ae9e5-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae9e5-104">SYNTAX</span></span>

### <span data-ttu-id="ae9e5-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="ae9e5-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9e5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ae9e5-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae9e5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ae9e5-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae9e5-108">설명</span><span class="sxs-lookup"><span data-stu-id="ae9e5-108">DESCRIPTION</span></span>
<span data-ttu-id="ae9e5-109">갤러리 이미지 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="ae9e5-110">예제</span><span class="sxs-lookup"><span data-stu-id="ae9e5-110">EXAMPLES</span></span>

### <span data-ttu-id="ae9e5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae9e5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="ae9e5-112">갤러리 이미지 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="ae9e5-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae9e5-113">PARAMETERS</span></span>

### <span data-ttu-id="ae9e5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae9e5-114">-AsJob</span></span>
<span data-ttu-id="ae9e5-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ae9e5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae9e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9e5-116">-DefaultProfile</span></span>
<span data-ttu-id="ae9e5-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae9e5-118">-Description</span><span class="sxs-lookup"><span data-stu-id="ae9e5-118">-Description</span></span>
<span data-ttu-id="ae9e5-119">갤러리 이미지 정의 리소스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="ae9e5-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="ae9e5-120">-DisallowedDiskType</span></span>
<span data-ttu-id="ae9e5-121">사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="ae9e5-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="ae9e5-122">-EndOfLifeDate</span></span>
<span data-ttu-id="ae9e5-123">갤러리 이미지 정의의 수명 종료 날짜</span><span class="sxs-lookup"><span data-stu-id="ae9e5-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="ae9e5-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="ae9e5-124">-Eula</span></span>
<span data-ttu-id="ae9e5-125">갤러리 이미지 정의에 대한 Eula 계약입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="ae9e5-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="ae9e5-126">-GalleryName</span></span>
<span data-ttu-id="ae9e5-127">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="ae9e5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae9e5-128">-InputObject</span></span>
<span data-ttu-id="ae9e5-129">PS 갤러리 이미지 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9e5-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="ae9e5-130">-MaximumMemory</span></span>
<span data-ttu-id="ae9e5-131">권장되는 메모리의 최대값</span><span class="sxs-lookup"><span data-stu-id="ae9e5-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="ae9e5-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="ae9e5-132">-MaximumVCPU</span></span>
<span data-ttu-id="ae9e5-133">권장되는 CPU 코어의 최대값</span><span class="sxs-lookup"><span data-stu-id="ae9e5-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ae9e5-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="ae9e5-134">-MinimumMemory</span></span>
<span data-ttu-id="ae9e5-135">권장되는 메모리의 최소값</span><span class="sxs-lookup"><span data-stu-id="ae9e5-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="ae9e5-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="ae9e5-136">-MinimumVCPU</span></span>
<span data-ttu-id="ae9e5-137">권장되는 CPU 코어의 최소값</span><span class="sxs-lookup"><span data-stu-id="ae9e5-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ae9e5-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ae9e5-138">-Name</span></span>
<span data-ttu-id="ae9e5-139">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9e5-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="ae9e5-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="ae9e5-141">개인 정보 취급 방침 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="ae9e5-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="ae9e5-142">-PurchasePlanName</span></span>
<span data-ttu-id="ae9e5-143">구매 계획의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ae9e5-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="ae9e5-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="ae9e5-145">구매 계획의 제품 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ae9e5-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ae9e5-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="ae9e5-147">구매 계획의 게시자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ae9e5-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="ae9e5-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="ae9e5-149">릴리스 참고 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-149">The release note uri.</span></span>

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

### <span data-ttu-id="ae9e5-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae9e5-150">-ResourceGroupName</span></span>
<span data-ttu-id="ae9e5-151">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae9e5-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae9e5-152">-ResourceId</span></span>
<span data-ttu-id="ae9e5-153">이미지 정의에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ae9e5-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="ae9e5-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae9e5-154">-Tag</span></span>
<span data-ttu-id="ae9e5-155">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="ae9e5-155">Resource tags</span></span>

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

### <span data-ttu-id="ae9e5-156">-확인</span><span class="sxs-lookup"><span data-stu-id="ae9e5-156">-Confirm</span></span>
<span data-ttu-id="ae9e5-157">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9e5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9e5-158">-WhatIf</span></span>
<span data-ttu-id="ae9e5-159">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae9e5-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9e5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9e5-161">CommonParameters</span></span>
<span data-ttu-id="ae9e5-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae9e5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9e5-163">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae9e5-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9e5-164">입력</span><span class="sxs-lookup"><span data-stu-id="ae9e5-164">INPUTS</span></span>

### <span data-ttu-id="ae9e5-165">System.String</span><span class="sxs-lookup"><span data-stu-id="ae9e5-165">System.String</span></span>

### <span data-ttu-id="ae9e5-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="ae9e5-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="ae9e5-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="ae9e5-167">System.DateTime</span></span>

### <span data-ttu-id="ae9e5-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae9e5-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ae9e5-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ae9e5-169">System.Int32</span></span>

### <span data-ttu-id="ae9e5-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ae9e5-170">System.String[]</span></span>

## <span data-ttu-id="ae9e5-171">출력</span><span class="sxs-lookup"><span data-stu-id="ae9e5-171">OUTPUTS</span></span>

### <span data-ttu-id="ae9e5-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="ae9e5-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="ae9e5-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae9e5-173">NOTES</span></span>

## <span data-ttu-id="ae9e5-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae9e5-174">RELATED LINKS</span></span>
