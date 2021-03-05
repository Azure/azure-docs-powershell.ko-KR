---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: d632f3f9717c706adf2881aa177d9cb7ff2425dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988344"
---
# <span data-ttu-id="d72e7-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="d72e7-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="d72e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d72e7-103">갤러리 이미지 정의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="d72e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="d72e7-104">SYNTAX</span></span>

### <span data-ttu-id="d72e7-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="d72e7-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72e7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d72e7-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72e7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d72e7-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72e7-108">설명</span><span class="sxs-lookup"><span data-stu-id="d72e7-108">DESCRIPTION</span></span>
<span data-ttu-id="d72e7-109">갤러리 이미지 정의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="d72e7-110">예제</span><span class="sxs-lookup"><span data-stu-id="d72e7-110">EXAMPLES</span></span>

### <span data-ttu-id="d72e7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d72e7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="d72e7-112">갤러리 이미지 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="d72e7-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d72e7-113">PARAMETERS</span></span>

### <span data-ttu-id="d72e7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d72e7-114">-AsJob</span></span>
<span data-ttu-id="d72e7-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d72e7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d72e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72e7-116">-DefaultProfile</span></span>
<span data-ttu-id="d72e7-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d72e7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d72e7-118">-Force</span></span>
<span data-ttu-id="d72e7-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d72e7-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="d72e7-120">-GalleryName</span></span>
<span data-ttu-id="d72e7-121">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="d72e7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d72e7-122">-InputObject</span></span>
<span data-ttu-id="d72e7-123">PS 갤러리 이미지 정의 개체</span><span class="sxs-lookup"><span data-stu-id="d72e7-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="d72e7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d72e7-124">-Name</span></span>
<span data-ttu-id="d72e7-125">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="d72e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="d72e7-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d72e7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d72e7-128">-ResourceId</span></span>
<span data-ttu-id="d72e7-129">갤러리 이미지 정의에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d72e7-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="d72e7-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d72e7-130">-Confirm</span></span>
<span data-ttu-id="d72e7-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72e7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72e7-132">-WhatIf</span></span>
<span data-ttu-id="d72e7-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72e7-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72e7-135">CommonParameters</span></span>
<span data-ttu-id="d72e7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d72e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72e7-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d72e7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72e7-138">입력</span><span class="sxs-lookup"><span data-stu-id="d72e7-138">INPUTS</span></span>

### <span data-ttu-id="d72e7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d72e7-139">System.String</span></span>

### <span data-ttu-id="d72e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="d72e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="d72e7-141">출력</span><span class="sxs-lookup"><span data-stu-id="d72e7-141">OUTPUTS</span></span>

### <span data-ttu-id="d72e7-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d72e7-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d72e7-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d72e7-143">NOTES</span></span>

## <span data-ttu-id="d72e7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d72e7-144">RELATED LINKS</span></span>
