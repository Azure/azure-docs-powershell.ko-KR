---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 7c62860f3829c07621c951175b00a4be4960c95f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697324"
---
# <span data-ttu-id="b9078-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b9078-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="b9078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9078-102">SYNOPSIS</span></span>
<span data-ttu-id="b9078-103">갤러리 이미지 버전을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="b9078-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9078-104">SYNTAX</span></span>

### <span data-ttu-id="b9078-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9078-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9078-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b9078-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9078-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b9078-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9078-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b9078-108">DESCRIPTION</span></span>
<span data-ttu-id="b9078-109">갤러리 이미지 버전을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="b9078-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b9078-110">EXAMPLES</span></span>

### <span data-ttu-id="b9078-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9078-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="b9078-112">지정 된 갤러리 이미지 버전을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="b9078-113">변수</span><span class="sxs-lookup"><span data-stu-id="b9078-113">PARAMETERS</span></span>

### <span data-ttu-id="b9078-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9078-114">-AsJob</span></span>
<span data-ttu-id="b9078-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b9078-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9078-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9078-116">-DefaultProfile</span></span>
<span data-ttu-id="b9078-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9078-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b9078-118">-Force</span></span>
<span data-ttu-id="b9078-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9078-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b9078-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="b9078-121">갤러리 이미지 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b9078-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b9078-122">-GalleryName</span></span>
<span data-ttu-id="b9078-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="b9078-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9078-124">-InputObject</span></span>
<span data-ttu-id="b9078-125">PS 갤러리 이미지 버전 개체</span><span class="sxs-lookup"><span data-stu-id="b9078-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="b9078-126">-이름</span><span class="sxs-lookup"><span data-stu-id="b9078-126">-Name</span></span>
<span data-ttu-id="b9078-127">갤러리 이미지 버전의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="b9078-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9078-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9078-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9078-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9078-130">-ResourceId</span></span>
<span data-ttu-id="b9078-131">갤러리 이미지 버전에 대 한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b9078-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="b9078-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b9078-132">-Confirm</span></span>
<span data-ttu-id="b9078-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9078-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9078-134">-WhatIf</span></span>
<span data-ttu-id="b9078-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9078-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9078-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9078-137">CommonParameters</span></span>
<span data-ttu-id="b9078-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9078-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9078-139">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9078-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9078-140">입력</span><span class="sxs-lookup"><span data-stu-id="b9078-140">INPUTS</span></span>

### <span data-ttu-id="b9078-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b9078-141">System.String</span></span>

### <span data-ttu-id="b9078-142">PSGalleryImageVersion의. m a.</span><span class="sxs-lookup"><span data-stu-id="b9078-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="b9078-143">출력</span><span class="sxs-lookup"><span data-stu-id="b9078-143">OUTPUTS</span></span>

### <span data-ttu-id="b9078-144">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="b9078-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b9078-145">상속자</span><span class="sxs-lookup"><span data-stu-id="b9078-145">NOTES</span></span>

## <span data-ttu-id="b9078-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9078-146">RELATED LINKS</span></span>
