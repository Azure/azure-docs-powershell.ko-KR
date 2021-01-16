---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363861"
---
# <span data-ttu-id="b6f33-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b6f33-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b6f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f33-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f33-103">지정된 청사진 정의를 JSON 파일로 지정된 출력 위치로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="b6f33-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6f33-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f33-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6f33-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f33-106">해당 아티팩트를 통해 청사진 정의를 내보내고 디스크에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="b6f33-107">이 cmdlet은 청사진의 최신 버전(초안 또는 게시)을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="b6f33-108">예제</span><span class="sxs-lookup"><span data-stu-id="b6f33-108">EXAMPLES</span></span>

### <span data-ttu-id="b6f33-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6f33-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="b6f33-110">해당 아티팩트를 통해 청사진 정의를 내보내고 디스크에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="b6f33-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6f33-111">PARAMETERS</span></span>

### <span data-ttu-id="b6f33-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="b6f33-112">-Blueprint</span></span>
<span data-ttu-id="b6f33-113">내보낼 청사진 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="b6f33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f33-114">-DefaultProfile</span></span>
<span data-ttu-id="b6f33-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f33-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b6f33-116">-Force</span></span>
<span data-ttu-id="b6f33-117">true로 설정하면 실행에서 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b6f33-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b6f33-118">-OutputPath</span></span>
<span data-ttu-id="b6f33-119">JSON 형식으로 청사진 정의를 내보낼 디스크의 파일에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="b6f33-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6f33-120">-PassThru</span></span>
<span data-ttu-id="b6f33-121">설정하면 cmdlet은 내보낼 청사진 정의를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="b6f33-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6f33-123">-Version</span><span class="sxs-lookup"><span data-stu-id="b6f33-123">-Version</span></span>
<span data-ttu-id="b6f33-124">게시된 청사진 정의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="b6f33-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6f33-125">-Confirm</span></span>
<span data-ttu-id="b6f33-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f33-127">-WhatIf</span></span>
<span data-ttu-id="b6f33-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b6f33-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6f33-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f33-130">CommonParameters</span></span>
<span data-ttu-id="b6f33-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f33-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6f33-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f33-133">입력</span><span class="sxs-lookup"><span data-stu-id="b6f33-133">INPUTS</span></span>

### <span data-ttu-id="b6f33-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b6f33-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b6f33-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b6f33-135">System.String</span></span>

## <span data-ttu-id="b6f33-136">출력</span><span class="sxs-lookup"><span data-stu-id="b6f33-136">OUTPUTS</span></span>

### <span data-ttu-id="b6f33-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b6f33-137">System.String</span></span>

## <span data-ttu-id="b6f33-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6f33-138">NOTES</span></span>

## <span data-ttu-id="b6f33-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6f33-139">RELATED LINKS</span></span>
