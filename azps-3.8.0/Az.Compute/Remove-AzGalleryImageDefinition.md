---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879881"
---
# <span data-ttu-id="4f18c-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4f18c-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="4f18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f18c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f18c-103">갤러리 이미지 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="4f18c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f18c-104">SYNTAX</span></span>

### <span data-ttu-id="4f18c-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="4f18c-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f18c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4f18c-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f18c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4f18c-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f18c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4f18c-108">DESCRIPTION</span></span>
<span data-ttu-id="4f18c-109">갤러리 이미지 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="4f18c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4f18c-110">EXAMPLES</span></span>

### <span data-ttu-id="4f18c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f18c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="4f18c-112">갤러리 이미지 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="4f18c-113">변수</span><span class="sxs-lookup"><span data-stu-id="4f18c-113">PARAMETERS</span></span>

### <span data-ttu-id="4f18c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f18c-114">-AsJob</span></span>
<span data-ttu-id="4f18c-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4f18c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f18c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f18c-116">-DefaultProfile</span></span>
<span data-ttu-id="4f18c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f18c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4f18c-118">-Force</span></span>
<span data-ttu-id="4f18c-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f18c-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="4f18c-120">-GalleryName</span></span>
<span data-ttu-id="4f18c-121">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="4f18c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f18c-122">-InputObject</span></span>
<span data-ttu-id="4f18c-123">PS 갤러리 이미지 정의 개체</span><span class="sxs-lookup"><span data-stu-id="4f18c-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="4f18c-124">-이름</span><span class="sxs-lookup"><span data-stu-id="4f18c-124">-Name</span></span>
<span data-ttu-id="4f18c-125">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="4f18c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f18c-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f18c-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4f18c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f18c-128">-ResourceId</span></span>
<span data-ttu-id="4f18c-129">갤러리 이미지 정의의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4f18c-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="4f18c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="4f18c-130">-Confirm</span></span>
<span data-ttu-id="4f18c-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f18c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f18c-132">-WhatIf</span></span>
<span data-ttu-id="4f18c-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f18c-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f18c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f18c-135">CommonParameters</span></span>
<span data-ttu-id="4f18c-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f18c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f18c-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f18c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f18c-138">입력</span><span class="sxs-lookup"><span data-stu-id="4f18c-138">INPUTS</span></span>

### <span data-ttu-id="4f18c-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f18c-139">System.String</span></span>

### <span data-ttu-id="4f18c-140">PSGalleryImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="4f18c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4f18c-141">출력</span><span class="sxs-lookup"><span data-stu-id="4f18c-141">OUTPUTS</span></span>

### <span data-ttu-id="4f18c-142">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="4f18c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4f18c-143">상속자</span><span class="sxs-lookup"><span data-stu-id="4f18c-143">NOTES</span></span>

## <span data-ttu-id="4f18c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f18c-144">RELATED LINKS</span></span>
