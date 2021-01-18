---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496198"
---
# <span data-ttu-id="bec9a-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="bec9a-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="bec9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec9a-102">SYNOPSIS</span></span>
<span data-ttu-id="bec9a-103">JSON 형식으로 청사진 파일을 청사진 개체로 가져오고 지정된 구독 또는 관리 그룹 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="bec9a-104">구문</span><span class="sxs-lookup"><span data-stu-id="bec9a-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec9a-105">설명</span><span class="sxs-lookup"><span data-stu-id="bec9a-105">DESCRIPTION</span></span>
<span data-ttu-id="bec9a-106">아티팩트를 통해 청사진 정의를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="bec9a-107">예제</span><span class="sxs-lookup"><span data-stu-id="bec9a-107">EXAMPLES</span></span>

### <span data-ttu-id="bec9a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bec9a-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="bec9a-109">해당 아티팩트를 통해 청사진 정의를 가져오고 구독 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="bec9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bec9a-110">PARAMETERS</span></span>

### <span data-ttu-id="bec9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec9a-111">-DefaultProfile</span></span>
<span data-ttu-id="bec9a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec9a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bec9a-113">-Force</span></span>
<span data-ttu-id="bec9a-114">true로 설정하면 실행에서 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="bec9a-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="bec9a-115">-IncludeSubFolders</span></span>
<span data-ttu-id="bec9a-116">true로 설정하면 하위폴더의 아티팩트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="bec9a-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="bec9a-117">-InputPath</span></span>
<span data-ttu-id="bec9a-118">디스크의 청사진 JSON 파일에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="bec9a-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="bec9a-119">-ManagementGroupId</span></span>
<span data-ttu-id="bec9a-120">청사진 정의가 저장되거나 저장될 관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="bec9a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bec9a-121">-Name</span></span>
<span data-ttu-id="bec9a-122">청사진 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="bec9a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bec9a-123">-PassThru</span></span>
<span data-ttu-id="bec9a-124">설정하면 cmdlet은 가져온 청사진 정의를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="bec9a-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bec9a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bec9a-126">-SubscriptionId</span></span>
<span data-ttu-id="bec9a-127">청사진 정의가 저장되거나 저장될 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="bec9a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec9a-128">-Confirm</span></span>
<span data-ttu-id="bec9a-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec9a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec9a-130">-WhatIf</span></span>
<span data-ttu-id="bec9a-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bec9a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bec9a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec9a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec9a-133">CommonParameters</span></span>
<span data-ttu-id="bec9a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bec9a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec9a-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bec9a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec9a-136">입력</span><span class="sxs-lookup"><span data-stu-id="bec9a-136">INPUTS</span></span>

### <span data-ttu-id="bec9a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bec9a-137">System.String</span></span>

## <span data-ttu-id="bec9a-138">출력</span><span class="sxs-lookup"><span data-stu-id="bec9a-138">OUTPUTS</span></span>

### <span data-ttu-id="bec9a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bec9a-139">System.String</span></span>

## <span data-ttu-id="bec9a-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bec9a-140">NOTES</span></span>

## <span data-ttu-id="bec9a-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bec9a-141">RELATED LINKS</span></span>
