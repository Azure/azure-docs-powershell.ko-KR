---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342153"
---
# <span data-ttu-id="deb75-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="deb75-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="deb75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deb75-102">SYNOPSIS</span></span>
<span data-ttu-id="deb75-103">갤러리 이미지 정의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="deb75-104">구문</span><span class="sxs-lookup"><span data-stu-id="deb75-104">SYNTAX</span></span>

### <span data-ttu-id="deb75-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="deb75-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deb75-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="deb75-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deb75-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="deb75-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb75-108">설명</span><span class="sxs-lookup"><span data-stu-id="deb75-108">DESCRIPTION</span></span>
<span data-ttu-id="deb75-109">갤러리 이미지 정의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="deb75-110">예제</span><span class="sxs-lookup"><span data-stu-id="deb75-110">EXAMPLES</span></span>

### <span data-ttu-id="deb75-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="deb75-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="deb75-112">갤러리 이미지 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="deb75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deb75-113">PARAMETERS</span></span>

### <span data-ttu-id="deb75-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="deb75-114">-AsJob</span></span>
<span data-ttu-id="deb75-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="deb75-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="deb75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb75-116">-DefaultProfile</span></span>
<span data-ttu-id="deb75-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb75-118">-Force</span><span class="sxs-lookup"><span data-stu-id="deb75-118">-Force</span></span>
<span data-ttu-id="deb75-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="deb75-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="deb75-120">-GalleryName</span></span>
<span data-ttu-id="deb75-121">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="deb75-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deb75-122">-InputObject</span></span>
<span data-ttu-id="deb75-123">PS 갤러리 이미지 정의 개체</span><span class="sxs-lookup"><span data-stu-id="deb75-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="deb75-124">-Name</span><span class="sxs-lookup"><span data-stu-id="deb75-124">-Name</span></span>
<span data-ttu-id="deb75-125">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="deb75-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb75-126">-ResourceGroupName</span></span>
<span data-ttu-id="deb75-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="deb75-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deb75-128">-ResourceId</span></span>
<span data-ttu-id="deb75-129">갤러리 이미지 정의에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="deb75-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="deb75-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="deb75-130">-Confirm</span></span>
<span data-ttu-id="deb75-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb75-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb75-132">-WhatIf</span></span>
<span data-ttu-id="deb75-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="deb75-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb75-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb75-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb75-135">CommonParameters</span></span>
<span data-ttu-id="deb75-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="deb75-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb75-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="deb75-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb75-138">입력</span><span class="sxs-lookup"><span data-stu-id="deb75-138">INPUTS</span></span>

### <span data-ttu-id="deb75-139">System.String</span><span class="sxs-lookup"><span data-stu-id="deb75-139">System.String</span></span>

### <span data-ttu-id="deb75-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="deb75-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="deb75-141">출력</span><span class="sxs-lookup"><span data-stu-id="deb75-141">OUTPUTS</span></span>

### <span data-ttu-id="deb75-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="deb75-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="deb75-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="deb75-143">NOTES</span></span>

## <span data-ttu-id="deb75-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="deb75-144">RELATED LINKS</span></span>
