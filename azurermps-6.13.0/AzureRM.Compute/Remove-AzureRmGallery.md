---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGallery.md
ms.openlocfilehash: 2711b5398f3d10f894214473f6ff68045748af22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530406"
---
# <span data-ttu-id="94f7a-101">Remove-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="94f7a-101">Remove-AzureRmGallery</span></span>

## <span data-ttu-id="94f7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="94f7a-103">갤러리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-103">Delete a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94f7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94f7a-104">SYNTAX</span></span>

### <span data-ttu-id="94f7a-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="94f7a-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f7a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="94f7a-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f7a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="94f7a-107">ObjectParameter</span></span>
```
Remove-AzureRmGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f7a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="94f7a-108">DESCRIPTION</span></span>
<span data-ttu-id="94f7a-109">갤러리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-109">Delete a gallery.</span></span>

## <span data-ttu-id="94f7a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="94f7a-110">EXAMPLES</span></span>

### <span data-ttu-id="94f7a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="94f7a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="94f7a-112">지정 된 갤러리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-112">Delete the given gallery.</span></span>

## <span data-ttu-id="94f7a-113">변수</span><span class="sxs-lookup"><span data-stu-id="94f7a-113">PARAMETERS</span></span>

### <span data-ttu-id="94f7a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94f7a-114">-AsJob</span></span>
<span data-ttu-id="94f7a-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="94f7a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f7a-116">-DefaultProfile</span></span>
<span data-ttu-id="94f7a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f7a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="94f7a-118">-Force</span></span>
<span data-ttu-id="94f7a-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94f7a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94f7a-120">-InputObject</span></span>
<span data-ttu-id="94f7a-121">PS 갤러리 개체</span><span class="sxs-lookup"><span data-stu-id="94f7a-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="94f7a-122">-Name</span></span>
<span data-ttu-id="94f7a-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f7a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f7a-124">-ResourceGroupName</span></span>
<span data-ttu-id="94f7a-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="94f7a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94f7a-126">-ResourceId</span></span>
<span data-ttu-id="94f7a-127">갤러리의 자원 Id</span><span class="sxs-lookup"><span data-stu-id="94f7a-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="94f7a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="94f7a-128">-Confirm</span></span>
<span data-ttu-id="94f7a-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f7a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f7a-130">-WhatIf</span></span>
<span data-ttu-id="94f7a-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f7a-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f7a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f7a-133">CommonParameters</span></span>
<span data-ttu-id="94f7a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94f7a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f7a-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f7a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f7a-136">입력</span><span class="sxs-lookup"><span data-stu-id="94f7a-136">INPUTS</span></span>

### <span data-ttu-id="94f7a-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94f7a-137">System.String</span></span>

### <span data-ttu-id="94f7a-138">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="94f7a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="94f7a-139">출력</span><span class="sxs-lookup"><span data-stu-id="94f7a-139">OUTPUTS</span></span>

### <span data-ttu-id="94f7a-140">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="94f7a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="94f7a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="94f7a-141">NOTES</span></span>

## <span data-ttu-id="94f7a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94f7a-142">RELATED LINKS</span></span>
