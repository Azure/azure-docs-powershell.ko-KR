---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213397"
---
# <span data-ttu-id="fef20-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="fef20-101">Update-AzGallery</span></span>

## <span data-ttu-id="fef20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef20-102">SYNOPSIS</span></span>
<span data-ttu-id="fef20-103">갤러리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-103">Update a gallery.</span></span>

## <span data-ttu-id="fef20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fef20-104">SYNTAX</span></span>

### <span data-ttu-id="fef20-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="fef20-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fef20-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fef20-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fef20-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fef20-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef20-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fef20-108">DESCRIPTION</span></span>
<span data-ttu-id="fef20-109">갤러리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-109">Update a gallery.</span></span>

## <span data-ttu-id="fef20-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fef20-110">EXAMPLES</span></span>

### <span data-ttu-id="fef20-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fef20-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="fef20-112">갤러리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-112">Update a gallery.</span></span>

## <span data-ttu-id="fef20-113">변수</span><span class="sxs-lookup"><span data-stu-id="fef20-113">PARAMETERS</span></span>

### <span data-ttu-id="fef20-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fef20-114">-AsJob</span></span>
<span data-ttu-id="fef20-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fef20-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fef20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef20-116">-DefaultProfile</span></span>
<span data-ttu-id="fef20-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fef20-118">-설명</span><span class="sxs-lookup"><span data-stu-id="fef20-118">-Description</span></span>
<span data-ttu-id="fef20-119">갤러리 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="fef20-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fef20-120">-InputObject</span></span>
<span data-ttu-id="fef20-121">PS 갤러리 개체</span><span class="sxs-lookup"><span data-stu-id="fef20-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="fef20-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fef20-122">-Name</span></span>
<span data-ttu-id="fef20-123">갤러리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="fef20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef20-124">-ResourceGroupName</span></span>
<span data-ttu-id="fef20-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="fef20-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fef20-126">-ResourceId</span></span>
<span data-ttu-id="fef20-127">갤러리의 자원 Id</span><span class="sxs-lookup"><span data-stu-id="fef20-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="fef20-128">태그</span><span class="sxs-lookup"><span data-stu-id="fef20-128">-Tag</span></span>
<span data-ttu-id="fef20-129">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="fef20-129">Resource tags</span></span>

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

### <span data-ttu-id="fef20-130">-확인</span><span class="sxs-lookup"><span data-stu-id="fef20-130">-Confirm</span></span>
<span data-ttu-id="fef20-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fef20-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef20-132">-WhatIf</span></span>
<span data-ttu-id="fef20-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fef20-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fef20-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef20-135">CommonParameters</span></span>
<span data-ttu-id="fef20-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef20-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef20-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fef20-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef20-138">입력</span><span class="sxs-lookup"><span data-stu-id="fef20-138">INPUTS</span></span>

### <span data-ttu-id="fef20-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fef20-139">System.String</span></span>

### <span data-ttu-id="fef20-140">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="fef20-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="fef20-141">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="fef20-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fef20-142">출력</span><span class="sxs-lookup"><span data-stu-id="fef20-142">OUTPUTS</span></span>

### <span data-ttu-id="fef20-143">PSGallery의. m a.</span><span class="sxs-lookup"><span data-stu-id="fef20-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="fef20-144">상속자</span><span class="sxs-lookup"><span data-stu-id="fef20-144">NOTES</span></span>

## <span data-ttu-id="fef20-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fef20-145">RELATED LINKS</span></span>
