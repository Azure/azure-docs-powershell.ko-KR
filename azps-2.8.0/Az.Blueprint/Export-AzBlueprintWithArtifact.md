---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697652"
---
# <span data-ttu-id="37fb1-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="37fb1-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="37fb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="37fb1-103">지정 된 청사진 정의를 JSON 파일로 지정 된 출력 위치에 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="37fb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37fb1-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37fb1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="37fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="37fb1-106">해당 가공물을 사용 하 여 청사진 정의를 내보내고 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="37fb1-107">이 cmdlet은 청사진의 최신 버전 (초안 또는 게시)을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="37fb1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="37fb1-108">EXAMPLES</span></span>

### <span data-ttu-id="37fb1-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="37fb1-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="37fb1-110">해당 가공물을 사용 하 여 청사진 정의를 내보내고 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="37fb1-111">변수</span><span class="sxs-lookup"><span data-stu-id="37fb1-111">PARAMETERS</span></span>

### <span data-ttu-id="37fb1-112">-청사진</span><span class="sxs-lookup"><span data-stu-id="37fb1-112">-Blueprint</span></span>
<span data-ttu-id="37fb1-113">내보낼 청사진 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37fb1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fb1-114">-DefaultProfile</span></span>
<span data-ttu-id="37fb1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fb1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="37fb1-116">-Force</span></span>
<span data-ttu-id="37fb1-117">True로 설정 하면 실행 시 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fb1-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="37fb1-118">-OutputPath</span></span>
<span data-ttu-id="37fb1-119">JSON 형식으로 청사진 정의를 내보낼 디스크의 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fb1-120">-버전</span><span class="sxs-lookup"><span data-stu-id="37fb1-120">-Version</span></span>
<span data-ttu-id="37fb1-121">게시 된 청사진 정의 버전.</span><span class="sxs-lookup"><span data-stu-id="37fb1-121">Published blueprint definition version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fb1-122">CommonParameters</span></span>
<span data-ttu-id="37fb1-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37fb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="37fb1-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37fb1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fb1-125">입력</span><span class="sxs-lookup"><span data-stu-id="37fb1-125">INPUTS</span></span>

### <span data-ttu-id="37fb1-126">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="37fb1-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="37fb1-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="37fb1-127">System.String</span></span>

## <span data-ttu-id="37fb1-128">출력</span><span class="sxs-lookup"><span data-stu-id="37fb1-128">OUTPUTS</span></span>

### <span data-ttu-id="37fb1-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="37fb1-129">System.String</span></span>

## <span data-ttu-id="37fb1-130">상속자</span><span class="sxs-lookup"><span data-stu-id="37fb1-130">NOTES</span></span>

## <span data-ttu-id="37fb1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37fb1-131">RELATED LINKS</span></span>
