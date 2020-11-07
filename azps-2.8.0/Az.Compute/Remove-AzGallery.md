---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: ac098616d2ee92b4d6910034735824289b971f5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697329"
---
# <span data-ttu-id="80056-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="80056-101">Remove-AzGallery</span></span>

## <span data-ttu-id="80056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80056-102">SYNOPSIS</span></span>
<span data-ttu-id="80056-103">갤러리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80056-103">Delete a gallery.</span></span>

## <span data-ttu-id="80056-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80056-104">SYNTAX</span></span>

### <span data-ttu-id="80056-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="80056-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80056-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="80056-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80056-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="80056-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80056-108">설명은</span><span class="sxs-lookup"><span data-stu-id="80056-108">DESCRIPTION</span></span>
<span data-ttu-id="80056-109">갤러리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80056-109">Delete a gallery.</span></span>

## <span data-ttu-id="80056-110">예제의</span><span class="sxs-lookup"><span data-stu-id="80056-110">EXAMPLES</span></span>

### <span data-ttu-id="80056-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="80056-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="80056-112">지정 된 갤러리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="80056-112">Delete the given gallery.</span></span>

## <span data-ttu-id="80056-113">변수</span><span class="sxs-lookup"><span data-stu-id="80056-113">PARAMETERS</span></span>

### <span data-ttu-id="80056-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80056-114">-AsJob</span></span>
<span data-ttu-id="80056-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="80056-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80056-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80056-116">-DefaultProfile</span></span>
<span data-ttu-id="80056-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80056-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80056-118">-Force</span><span class="sxs-lookup"><span data-stu-id="80056-118">-Force</span></span>
<span data-ttu-id="80056-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="80056-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="80056-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80056-120">-InputObject</span></span>
<span data-ttu-id="80056-121">PS 갤러리 개체</span><span class="sxs-lookup"><span data-stu-id="80056-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="80056-122">-이름</span><span class="sxs-lookup"><span data-stu-id="80056-122">-Name</span></span>
<span data-ttu-id="80056-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80056-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="80056-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80056-124">-ResourceGroupName</span></span>
<span data-ttu-id="80056-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80056-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="80056-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80056-126">-ResourceId</span></span>
<span data-ttu-id="80056-127">갤러리의 자원 Id</span><span class="sxs-lookup"><span data-stu-id="80056-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="80056-128">-확인</span><span class="sxs-lookup"><span data-stu-id="80056-128">-Confirm</span></span>
<span data-ttu-id="80056-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80056-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80056-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80056-130">-WhatIf</span></span>
<span data-ttu-id="80056-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80056-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80056-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80056-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80056-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80056-133">CommonParameters</span></span>
<span data-ttu-id="80056-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80056-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80056-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80056-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80056-136">입력</span><span class="sxs-lookup"><span data-stu-id="80056-136">INPUTS</span></span>

### <span data-ttu-id="80056-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="80056-137">System.String</span></span>

### <span data-ttu-id="80056-138">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="80056-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="80056-139">출력</span><span class="sxs-lookup"><span data-stu-id="80056-139">OUTPUTS</span></span>

### <span data-ttu-id="80056-140">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="80056-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="80056-141">상속자</span><span class="sxs-lookup"><span data-stu-id="80056-141">NOTES</span></span>

## <span data-ttu-id="80056-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80056-142">RELATED LINKS</span></span>
