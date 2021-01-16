---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368488"
---
# <span data-ttu-id="241fa-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="241fa-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="241fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="241fa-102">SYNOPSIS</span></span>
<span data-ttu-id="241fa-103">청사진 정의에서 아티팩트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="241fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="241fa-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="241fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="241fa-105">DESCRIPTION</span></span>
<span data-ttu-id="241fa-106">청사진 정의에서 아티팩트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="241fa-107">청사진 정의 버전을 지정하지 않으면 초안 버전이 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="241fa-108">초안 버전이 없는 경우 게시된 최신 청사진 정의가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="241fa-109">예제</span><span class="sxs-lookup"><span data-stu-id="241fa-109">EXAMPLES</span></span>

### <span data-ttu-id="241fa-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="241fa-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192
```

<span data-ttu-id="241fa-111">청사진 정의에서 아티팩트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="241fa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="241fa-112">PARAMETERS</span></span>

### <span data-ttu-id="241fa-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="241fa-113">-Blueprint</span></span>
<span data-ttu-id="241fa-114">청사진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-114">Blueprint object.</span></span>

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

### <span data-ttu-id="241fa-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="241fa-115">-BlueprintVersion</span></span>
<span data-ttu-id="241fa-116">아티팩트를 얻을 청사진의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-116">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241fa-117">-DefaultProfile</span></span>
<span data-ttu-id="241fa-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="241fa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="241fa-119">-Name</span></span>
<span data-ttu-id="241fa-120">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="241fa-120">Name of the artifact</span></span>

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

### <span data-ttu-id="241fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241fa-121">CommonParameters</span></span>
<span data-ttu-id="241fa-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="241fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241fa-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="241fa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241fa-124">입력</span><span class="sxs-lookup"><span data-stu-id="241fa-124">INPUTS</span></span>

### <span data-ttu-id="241fa-125">System.String</span><span class="sxs-lookup"><span data-stu-id="241fa-125">System.String</span></span>

### <span data-ttu-id="241fa-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="241fa-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="241fa-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="241fa-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="241fa-128">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="241fa-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="241fa-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="241fa-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="241fa-130">System.String[]</span><span class="sxs-lookup"><span data-stu-id="241fa-130">System.String[]</span></span>

## <span data-ttu-id="241fa-131">출력</span><span class="sxs-lookup"><span data-stu-id="241fa-131">OUTPUTS</span></span>

### <span data-ttu-id="241fa-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="241fa-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="241fa-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="241fa-133">NOTES</span></span>

## <span data-ttu-id="241fa-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="241fa-134">RELATED LINKS</span></span>
