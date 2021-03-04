---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: cb1f9ca5354810f6459a8d0a0e3ea1a53ad6cf78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958912"
---
# <span data-ttu-id="5679f-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5679f-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="5679f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5679f-102">SYNOPSIS</span></span>
<span data-ttu-id="5679f-103">갤러리 이미지 버전을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="5679f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5679f-104">SYNTAX</span></span>

### <span data-ttu-id="5679f-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="5679f-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5679f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5679f-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5679f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="5679f-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5679f-108">설명</span><span class="sxs-lookup"><span data-stu-id="5679f-108">DESCRIPTION</span></span>
<span data-ttu-id="5679f-109">갤러리 이미지 버전을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="5679f-110">예제</span><span class="sxs-lookup"><span data-stu-id="5679f-110">EXAMPLES</span></span>

### <span data-ttu-id="5679f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5679f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="5679f-112">주어진 갤러리 이미지 버전을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="5679f-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5679f-113">PARAMETERS</span></span>

### <span data-ttu-id="5679f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5679f-114">-AsJob</span></span>
<span data-ttu-id="5679f-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5679f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5679f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5679f-116">-DefaultProfile</span></span>
<span data-ttu-id="5679f-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5679f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5679f-118">-Force</span></span>
<span data-ttu-id="5679f-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5679f-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5679f-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="5679f-121">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5679f-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="5679f-122">-GalleryName</span></span>
<span data-ttu-id="5679f-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="5679f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5679f-124">-InputObject</span></span>
<span data-ttu-id="5679f-125">PS 갤러리 이미지 버전 개체</span><span class="sxs-lookup"><span data-stu-id="5679f-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5679f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5679f-126">-Name</span></span>
<span data-ttu-id="5679f-127">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5679f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5679f-128">-ResourceGroupName</span></span>
<span data-ttu-id="5679f-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="5679f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5679f-130">-ResourceId</span></span>
<span data-ttu-id="5679f-131">갤러리 이미지 버전에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5679f-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="5679f-132">-확인</span><span class="sxs-lookup"><span data-stu-id="5679f-132">-Confirm</span></span>
<span data-ttu-id="5679f-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5679f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5679f-134">-WhatIf</span></span>
<span data-ttu-id="5679f-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5679f-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5679f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5679f-137">CommonParameters</span></span>
<span data-ttu-id="5679f-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5679f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5679f-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5679f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5679f-140">입력</span><span class="sxs-lookup"><span data-stu-id="5679f-140">INPUTS</span></span>

### <span data-ttu-id="5679f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5679f-141">System.String</span></span>

### <span data-ttu-id="5679f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5679f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="5679f-143">출력</span><span class="sxs-lookup"><span data-stu-id="5679f-143">OUTPUTS</span></span>

### <span data-ttu-id="5679f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5679f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5679f-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5679f-145">NOTES</span></span>

## <span data-ttu-id="5679f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5679f-146">RELATED LINKS</span></span>
