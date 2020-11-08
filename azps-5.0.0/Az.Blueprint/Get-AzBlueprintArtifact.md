---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216111"
---
# <span data-ttu-id="2008c-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="2008c-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="2008c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2008c-102">SYNOPSIS</span></span>
<span data-ttu-id="2008c-103">청사진 정의에서 아티팩트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2008c-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="2008c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2008c-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2008c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2008c-105">DESCRIPTION</span></span>
<span data-ttu-id="2008c-106">청사진 정의에서 아티팩트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2008c-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="2008c-107">청사진 정의 버전을 지정 하지 않으면 초안 버전이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2008c-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="2008c-108">초안 버전이 없는 경우에는 게시 된 최신 청사진 정의가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2008c-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="2008c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2008c-109">EXAMPLES</span></span>

### <span data-ttu-id="2008c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2008c-110">Example 1</span></span>
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

<span data-ttu-id="2008c-111">청사진 정의에서 아티팩트 검색.</span><span class="sxs-lookup"><span data-stu-id="2008c-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="2008c-112">변수</span><span class="sxs-lookup"><span data-stu-id="2008c-112">PARAMETERS</span></span>

### <span data-ttu-id="2008c-113">-청사진</span><span class="sxs-lookup"><span data-stu-id="2008c-113">-Blueprint</span></span>
<span data-ttu-id="2008c-114">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="2008c-114">Blueprint object.</span></span>

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

### <span data-ttu-id="2008c-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="2008c-115">-BlueprintVersion</span></span>
<span data-ttu-id="2008c-116">아티팩트를 가져올 청사진 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2008c-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="2008c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2008c-117">-DefaultProfile</span></span>
<span data-ttu-id="2008c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2008c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2008c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2008c-119">-Name</span></span>
<span data-ttu-id="2008c-120">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="2008c-120">Name of the artifact</span></span>

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

### <span data-ttu-id="2008c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2008c-121">CommonParameters</span></span>
<span data-ttu-id="2008c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2008c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2008c-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2008c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2008c-124">입력</span><span class="sxs-lookup"><span data-stu-id="2008c-124">INPUTS</span></span>

### <span data-ttu-id="2008c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2008c-125">System.String</span></span>

### <span data-ttu-id="2008c-126">Microsoft. i a m. 모델. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="2008c-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="2008c-127">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="2008c-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2008c-128">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2008c-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2008c-129">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2008c-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2008c-130">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="2008c-130">System.String[]</span></span>

## <span data-ttu-id="2008c-131">출력</span><span class="sxs-lookup"><span data-stu-id="2008c-131">OUTPUTS</span></span>

### <span data-ttu-id="2008c-132">PSBlueprintAssignment (.).</span><span class="sxs-lookup"><span data-stu-id="2008c-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="2008c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="2008c-133">NOTES</span></span>

## <span data-ttu-id="2008c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2008c-134">RELATED LINKS</span></span>
