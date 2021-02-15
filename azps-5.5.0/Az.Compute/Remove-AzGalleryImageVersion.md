---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177620"
---
# <span data-ttu-id="18c53-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="18c53-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="18c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18c53-102">SYNOPSIS</span></span>
<span data-ttu-id="18c53-103">갤러리 이미지 버전을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="18c53-104">구문</span><span class="sxs-lookup"><span data-stu-id="18c53-104">SYNTAX</span></span>

### <span data-ttu-id="18c53-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="18c53-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18c53-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="18c53-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18c53-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="18c53-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18c53-108">설명</span><span class="sxs-lookup"><span data-stu-id="18c53-108">DESCRIPTION</span></span>
<span data-ttu-id="18c53-109">갤러리 이미지 버전을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="18c53-110">예제</span><span class="sxs-lookup"><span data-stu-id="18c53-110">EXAMPLES</span></span>

### <span data-ttu-id="18c53-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="18c53-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="18c53-112">주어진 갤러리 이미지 버전을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="18c53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18c53-113">PARAMETERS</span></span>

### <span data-ttu-id="18c53-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18c53-114">-AsJob</span></span>
<span data-ttu-id="18c53-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="18c53-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18c53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c53-116">-DefaultProfile</span></span>
<span data-ttu-id="18c53-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c53-118">-Force</span><span class="sxs-lookup"><span data-stu-id="18c53-118">-Force</span></span>
<span data-ttu-id="18c53-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18c53-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="18c53-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="18c53-121">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="18c53-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="18c53-122">-GalleryName</span></span>
<span data-ttu-id="18c53-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="18c53-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18c53-124">-InputObject</span></span>
<span data-ttu-id="18c53-125">PS 갤러리 이미지 버전 개체</span><span class="sxs-lookup"><span data-stu-id="18c53-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="18c53-126">-Name</span><span class="sxs-lookup"><span data-stu-id="18c53-126">-Name</span></span>
<span data-ttu-id="18c53-127">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="18c53-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c53-128">-ResourceGroupName</span></span>
<span data-ttu-id="18c53-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="18c53-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18c53-130">-ResourceId</span></span>
<span data-ttu-id="18c53-131">갤러리 이미지 버전에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="18c53-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="18c53-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18c53-132">-Confirm</span></span>
<span data-ttu-id="18c53-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18c53-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c53-134">-WhatIf</span></span>
<span data-ttu-id="18c53-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="18c53-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c53-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18c53-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c53-137">CommonParameters</span></span>
<span data-ttu-id="18c53-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="18c53-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c53-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18c53-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c53-140">입력</span><span class="sxs-lookup"><span data-stu-id="18c53-140">INPUTS</span></span>

### <span data-ttu-id="18c53-141">System.String</span><span class="sxs-lookup"><span data-stu-id="18c53-141">System.String</span></span>

### <span data-ttu-id="18c53-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="18c53-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="18c53-143">출력</span><span class="sxs-lookup"><span data-stu-id="18c53-143">OUTPUTS</span></span>

### <span data-ttu-id="18c53-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="18c53-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="18c53-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="18c53-145">NOTES</span></span>

## <span data-ttu-id="18c53-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18c53-146">RELATED LINKS</span></span>
