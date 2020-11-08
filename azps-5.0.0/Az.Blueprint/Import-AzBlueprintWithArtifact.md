---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216110"
---
# <span data-ttu-id="9c66e-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="9c66e-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="9c66e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c66e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c66e-103">JSON 형식의 청사진 파일을 청사진 개체로 가져와 지정 된 구독 또는 관리 그룹 내에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="9c66e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c66e-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c66e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9c66e-105">DESCRIPTION</span></span>
<span data-ttu-id="9c66e-106">해당 가공물을 사용 하 여 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="9c66e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9c66e-107">EXAMPLES</span></span>

### <span data-ttu-id="9c66e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c66e-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="9c66e-109">해당 가공물을 사용 하 여 청사진 정의를 가져오고 구독 내에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="9c66e-110">변수</span><span class="sxs-lookup"><span data-stu-id="9c66e-110">PARAMETERS</span></span>

### <span data-ttu-id="9c66e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c66e-111">-DefaultProfile</span></span>
<span data-ttu-id="9c66e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c66e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9c66e-113">-Force</span></span>
<span data-ttu-id="9c66e-114">True로 설정 하면 실행 시 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="9c66e-115">-IncludeSubFolders 폴더</span><span class="sxs-lookup"><span data-stu-id="9c66e-115">-IncludeSubFolders</span></span>
<span data-ttu-id="9c66e-116">True로 설정 되 면 하위 폴더의 아티팩트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="9c66e-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="9c66e-117">-InputPath</span></span>
<span data-ttu-id="9c66e-118">디스크의 청사진 JSON 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="9c66e-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9c66e-119">-ManagementGroupId</span></span>
<span data-ttu-id="9c66e-120">청사진 정의가 있거나 저장 되는 관리 그룹 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="9c66e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9c66e-121">-Name</span></span>
<span data-ttu-id="9c66e-122">청사진 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="9c66e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c66e-123">-PassThru</span></span>
<span data-ttu-id="9c66e-124">설정 되 면 cmdlet은 가져온 청사진 정의를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="9c66e-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c66e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c66e-126">-SubscriptionId</span></span>
<span data-ttu-id="9c66e-127">청사진 정의가 있는 구독 Id 또는 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="9c66e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="9c66e-128">-Confirm</span></span>
<span data-ttu-id="9c66e-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c66e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c66e-130">-WhatIf</span></span>
<span data-ttu-id="9c66e-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c66e-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c66e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c66e-133">CommonParameters</span></span>
<span data-ttu-id="9c66e-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c66e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c66e-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c66e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c66e-136">입력</span><span class="sxs-lookup"><span data-stu-id="9c66e-136">INPUTS</span></span>

### <span data-ttu-id="9c66e-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c66e-137">System.String</span></span>

## <span data-ttu-id="9c66e-138">출력</span><span class="sxs-lookup"><span data-stu-id="9c66e-138">OUTPUTS</span></span>

### <span data-ttu-id="9c66e-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c66e-139">System.String</span></span>

## <span data-ttu-id="9c66e-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9c66e-140">NOTES</span></span>

## <span data-ttu-id="9c66e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c66e-141">RELATED LINKS</span></span>
