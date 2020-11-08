---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215101"
---
# <span data-ttu-id="4bb04-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4bb04-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="4bb04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb04-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb04-103">갤러리 이미지 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="4bb04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bb04-104">SYNTAX</span></span>

### <span data-ttu-id="4bb04-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="4bb04-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bb04-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4bb04-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bb04-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4bb04-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bb04-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4bb04-108">DESCRIPTION</span></span>
<span data-ttu-id="4bb04-109">갤러리 이미지 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="4bb04-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4bb04-110">EXAMPLES</span></span>

### <span data-ttu-id="4bb04-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bb04-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="4bb04-112">갤러리 이미지 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="4bb04-113">변수</span><span class="sxs-lookup"><span data-stu-id="4bb04-113">PARAMETERS</span></span>

### <span data-ttu-id="4bb04-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bb04-114">-AsJob</span></span>
<span data-ttu-id="4bb04-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4bb04-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bb04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb04-116">-DefaultProfile</span></span>
<span data-ttu-id="4bb04-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb04-118">-설명</span><span class="sxs-lookup"><span data-stu-id="4bb04-118">-Description</span></span>
<span data-ttu-id="4bb04-119">갤러리 이미지 정의 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="4bb04-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="4bb04-120">-DisallowedDiskType</span></span>
<span data-ttu-id="4bb04-121">허용 되지 않는 디스크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="4bb04-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="4bb04-122">-EndOfLifeDate</span></span>
<span data-ttu-id="4bb04-123">갤러리 이미지 정의의 기간 종료 날짜</span><span class="sxs-lookup"><span data-stu-id="4bb04-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="4bb04-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="4bb04-124">-Eula</span></span>
<span data-ttu-id="4bb04-125">갤러리 이미지 정의에 대 한 Eula 계약입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="4bb04-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="4bb04-126">-GalleryName</span></span>
<span data-ttu-id="4bb04-127">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="4bb04-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bb04-128">-InputObject</span></span>
<span data-ttu-id="4bb04-129">PS 갤러리 이미지 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="4bb04-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="4bb04-130">-MaximumMemory</span></span>
<span data-ttu-id="4bb04-131">권장 되는 메모리의 최대 개수</span><span class="sxs-lookup"><span data-stu-id="4bb04-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="4bb04-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="4bb04-132">-MaximumVCPU</span></span>
<span data-ttu-id="4bb04-133">권장 되는 CPU 코어의 최대</span><span class="sxs-lookup"><span data-stu-id="4bb04-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="4bb04-134">-가을 메모리</span><span class="sxs-lookup"><span data-stu-id="4bb04-134">-MinimumMemory</span></span>
<span data-ttu-id="4bb04-135">권장 되는 메모리의 최소 개수</span><span class="sxs-lookup"><span data-stu-id="4bb04-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="4bb04-136">-없음 Vcpu</span><span class="sxs-lookup"><span data-stu-id="4bb04-136">-MinimumVCPU</span></span>
<span data-ttu-id="4bb04-137">권장 되는 CPU 코어의 최소</span><span class="sxs-lookup"><span data-stu-id="4bb04-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="4bb04-138">-이름</span><span class="sxs-lookup"><span data-stu-id="4bb04-138">-Name</span></span>
<span data-ttu-id="4bb04-139">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="4bb04-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="4bb04-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="4bb04-141">개인 정보 취급 방침 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="4bb04-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="4bb04-142">-PurchasePlanName</span></span>
<span data-ttu-id="4bb04-143">구매 계획의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4bb04-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="4bb04-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="4bb04-145">구매 플랜의 제품 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4bb04-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4bb04-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="4bb04-147">구매 계획의 게시자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4bb04-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="4bb04-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="4bb04-149">릴리스 노트 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-149">The release note uri.</span></span>

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

### <span data-ttu-id="4bb04-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb04-150">-ResourceGroupName</span></span>
<span data-ttu-id="4bb04-151">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="4bb04-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bb04-152">-ResourceId</span></span>
<span data-ttu-id="4bb04-153">이미지 정의의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4bb04-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="4bb04-154">태그</span><span class="sxs-lookup"><span data-stu-id="4bb04-154">-Tag</span></span>
<span data-ttu-id="4bb04-155">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="4bb04-155">Resource tags</span></span>

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

### <span data-ttu-id="4bb04-156">-확인</span><span class="sxs-lookup"><span data-stu-id="4bb04-156">-Confirm</span></span>
<span data-ttu-id="4bb04-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb04-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb04-158">-WhatIf</span></span>
<span data-ttu-id="4bb04-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bb04-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb04-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb04-161">CommonParameters</span></span>
<span data-ttu-id="4bb04-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb04-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb04-163">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4bb04-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb04-164">입력</span><span class="sxs-lookup"><span data-stu-id="4bb04-164">INPUTS</span></span>

### <span data-ttu-id="4bb04-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4bb04-165">System.String</span></span>

### <span data-ttu-id="4bb04-166">PSGalleryImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="4bb04-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="4bb04-167">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="4bb04-167">System.DateTime</span></span>

### <span data-ttu-id="4bb04-168">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="4bb04-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4bb04-169">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="4bb04-169">System.Int32</span></span>

### <span data-ttu-id="4bb04-170">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="4bb04-170">System.String[]</span></span>

## <span data-ttu-id="4bb04-171">출력</span><span class="sxs-lookup"><span data-stu-id="4bb04-171">OUTPUTS</span></span>

### <span data-ttu-id="4bb04-172">PSGalleryImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="4bb04-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4bb04-173">상속자</span><span class="sxs-lookup"><span data-stu-id="4bb04-173">NOTES</span></span>

## <span data-ttu-id="4bb04-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bb04-174">RELATED LINKS</span></span>
