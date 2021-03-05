---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 5511be0e20c99a6a120e2f7591287b9ee17b0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965099"
---
# <span data-ttu-id="e7371-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="e7371-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="e7371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7371-102">SYNOPSIS</span></span>
<span data-ttu-id="e7371-103">청사진 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="e7371-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7371-104">SYNTAX</span></span>

### <span data-ttu-id="e7371-105">UpdateBlueprintBySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="e7371-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7371-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e7371-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7371-107">설명</span><span class="sxs-lookup"><span data-stu-id="e7371-107">DESCRIPTION</span></span>
<span data-ttu-id="e7371-108">청사진 정의를 업데이트하고 지정된 구독 또는 관리 그룹 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="e7371-109">예제</span><span class="sxs-lookup"><span data-stu-id="e7371-109">EXAMPLES</span></span>

### <span data-ttu-id="e7371-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7371-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="e7371-111">새 매개 변수로 청사진 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="e7371-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7371-112">PARAMETERS</span></span>

### <span data-ttu-id="e7371-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="e7371-113">-BlueprintFile</span></span>
<span data-ttu-id="e7371-114">디스크의 청사진 JSON 파일에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="e7371-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7371-115">-DefaultProfile</span></span>
<span data-ttu-id="e7371-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7371-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e7371-117">-ManagementGroupId</span></span>
<span data-ttu-id="e7371-118">청사진 정의가 저장되거나 저장될 관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7371-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e7371-119">-Name</span></span>
<span data-ttu-id="e7371-120">청사진 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="e7371-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7371-121">-SubscriptionId</span></span>
<span data-ttu-id="e7371-122">청사진 정의가 저장되거나 저장될 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7371-123">-확인</span><span class="sxs-lookup"><span data-stu-id="e7371-123">-Confirm</span></span>
<span data-ttu-id="e7371-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7371-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7371-125">-WhatIf</span></span>
<span data-ttu-id="e7371-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7371-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7371-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7371-128">CommonParameters</span></span>
<span data-ttu-id="e7371-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7371-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7371-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7371-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7371-131">입력</span><span class="sxs-lookup"><span data-stu-id="e7371-131">INPUTS</span></span>

### <span data-ttu-id="e7371-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e7371-132">System.String</span></span>

## <span data-ttu-id="e7371-133">출력</span><span class="sxs-lookup"><span data-stu-id="e7371-133">OUTPUTS</span></span>

### <span data-ttu-id="e7371-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="e7371-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="e7371-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7371-135">NOTES</span></span>

## <span data-ttu-id="e7371-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7371-136">RELATED LINKS</span></span>
