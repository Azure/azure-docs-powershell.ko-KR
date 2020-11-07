---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 04d53c657c4747d0a4057a82e8160598fa57bc9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701288"
---
# <span data-ttu-id="6ca15-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6ca15-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="6ca15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca15-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca15-103">갤러리 이미지 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="6ca15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ca15-104">SYNTAX</span></span>

### <span data-ttu-id="6ca15-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ca15-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca15-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6ca15-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca15-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6ca15-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca15-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ca15-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca15-109">갤러리 이미지 정의를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="6ca15-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ca15-110">EXAMPLES</span></span>

### <span data-ttu-id="6ca15-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ca15-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="6ca15-112">갤러리 이미지 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="6ca15-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ca15-113">PARAMETERS</span></span>

### <span data-ttu-id="6ca15-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ca15-114">-AsJob</span></span>
<span data-ttu-id="6ca15-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6ca15-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ca15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca15-116">-DefaultProfile</span></span>
<span data-ttu-id="6ca15-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca15-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca15-118">-Force</span></span>
<span data-ttu-id="6ca15-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ca15-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6ca15-120">-GalleryName</span></span>
<span data-ttu-id="6ca15-121">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="6ca15-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ca15-122">-InputObject</span></span>
<span data-ttu-id="6ca15-123">PS 갤러리 이미지 정의 개체</span><span class="sxs-lookup"><span data-stu-id="6ca15-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="6ca15-124">-이름</span><span class="sxs-lookup"><span data-stu-id="6ca15-124">-Name</span></span>
<span data-ttu-id="6ca15-125">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="6ca15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca15-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ca15-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ca15-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca15-128">-ResourceId</span></span>
<span data-ttu-id="6ca15-129">갤러리 이미지 정의의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6ca15-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="6ca15-130">-확인</span><span class="sxs-lookup"><span data-stu-id="6ca15-130">-Confirm</span></span>
<span data-ttu-id="6ca15-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca15-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca15-132">-WhatIf</span></span>
<span data-ttu-id="6ca15-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca15-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca15-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca15-135">CommonParameters</span></span>
<span data-ttu-id="6ca15-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca15-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca15-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca15-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca15-138">입력</span><span class="sxs-lookup"><span data-stu-id="6ca15-138">INPUTS</span></span>

### <span data-ttu-id="6ca15-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ca15-139">System.String</span></span>

### <span data-ttu-id="6ca15-140">PSGalleryImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="6ca15-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="6ca15-141">출력</span><span class="sxs-lookup"><span data-stu-id="6ca15-141">OUTPUTS</span></span>

### <span data-ttu-id="6ca15-142">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="6ca15-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6ca15-143">상속자</span><span class="sxs-lookup"><span data-stu-id="6ca15-143">NOTES</span></span>

## <span data-ttu-id="6ca15-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ca15-144">RELATED LINKS</span></span>
