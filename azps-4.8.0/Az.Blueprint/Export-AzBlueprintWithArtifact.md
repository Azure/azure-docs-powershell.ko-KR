---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048483"
---
# <span data-ttu-id="c9a7f-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="c9a7f-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="c9a7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a7f-103">지정 된 청사진 정의를 JSON 파일로 지정 된 출력 위치에 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="c9a7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9a7f-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9a7f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9a7f-105">DESCRIPTION</span></span>
<span data-ttu-id="c9a7f-106">해당 가공물을 사용 하 여 청사진 정의를 내보내고 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="c9a7f-107">이 cmdlet은 청사진의 최신 버전 (초안 또는 게시)을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="c9a7f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c9a7f-108">EXAMPLES</span></span>

### <span data-ttu-id="c9a7f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9a7f-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="c9a7f-110">해당 가공물을 사용 하 여 청사진 정의를 내보내고 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="c9a7f-111">변수</span><span class="sxs-lookup"><span data-stu-id="c9a7f-111">PARAMETERS</span></span>

### <span data-ttu-id="c9a7f-112">-청사진</span><span class="sxs-lookup"><span data-stu-id="c9a7f-112">-Blueprint</span></span>
<span data-ttu-id="c9a7f-113">내보낼 청사진 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a7f-114">-DefaultProfile</span></span>
<span data-ttu-id="c9a7f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a7f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c9a7f-116">-Force</span></span>
<span data-ttu-id="c9a7f-117">True로 설정 하면 실행 시 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="c9a7f-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c9a7f-118">-OutputPath</span></span>
<span data-ttu-id="c9a7f-119">JSON 형식으로 청사진 정의를 내보낼 디스크의 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9a7f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9a7f-120">-PassThru</span></span>
<span data-ttu-id="c9a7f-121">설정 되 면 cmdlet은 내보낸 청사진 정의를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="c9a7f-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c9a7f-123">-버전</span><span class="sxs-lookup"><span data-stu-id="c9a7f-123">-Version</span></span>
<span data-ttu-id="c9a7f-124">게시 된 청사진 정의 버전.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="c9a7f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="c9a7f-125">-Confirm</span></span>
<span data-ttu-id="c9a7f-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a7f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a7f-127">-WhatIf</span></span>
<span data-ttu-id="c9a7f-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9a7f-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a7f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a7f-130">CommonParameters</span></span>
<span data-ttu-id="c9a7f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a7f-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c9a7f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a7f-133">입력</span><span class="sxs-lookup"><span data-stu-id="c9a7f-133">INPUTS</span></span>

### <span data-ttu-id="c9a7f-134">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="c9a7f-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c9a7f-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c9a7f-135">System.String</span></span>

## <span data-ttu-id="c9a7f-136">출력</span><span class="sxs-lookup"><span data-stu-id="c9a7f-136">OUTPUTS</span></span>

### <span data-ttu-id="c9a7f-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c9a7f-137">System.String</span></span>

## <span data-ttu-id="c9a7f-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c9a7f-138">NOTES</span></span>

## <span data-ttu-id="c9a7f-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9a7f-139">RELATED LINKS</span></span>
