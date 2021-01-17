---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326598"
---
# <span data-ttu-id="5d5a6-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="5d5a6-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="5d5a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5a6-103">새 버전의 청사진을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="5d5a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d5a6-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d5a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="5d5a6-105">DESCRIPTION</span></span>
<span data-ttu-id="5d5a6-106">청사진 정의의 새 버전을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="5d5a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="5d5a6-107">EXAMPLES</span></span>

### <span data-ttu-id="5d5a6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d5a6-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="5d5a6-109">청사진 정의의 새 버전을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="5d5a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d5a6-110">PARAMETERS</span></span>

### <span data-ttu-id="5d5a6-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="5d5a6-111">-Blueprint</span></span>
<span data-ttu-id="5d5a6-112">청사진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5a6-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="5d5a6-113">-ChangeNote</span></span>
<span data-ttu-id="5d5a6-114">이 청사진 버전의 내용을 설명하는 참고 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="5d5a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5a6-115">-DefaultProfile</span></span>
<span data-ttu-id="5d5a6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d5a6-117">-Version</span><span class="sxs-lookup"><span data-stu-id="5d5a6-117">-Version</span></span>
<span data-ttu-id="5d5a6-118">청사진 정의에 대한 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="5d5a6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d5a6-119">-Confirm</span></span>
<span data-ttu-id="5d5a6-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5a6-121">-WhatIf</span></span>
<span data-ttu-id="5d5a6-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5d5a6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d5a6-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5a6-124">CommonParameters</span></span>
<span data-ttu-id="5d5a6-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5a6-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d5a6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5a6-127">입력</span><span class="sxs-lookup"><span data-stu-id="5d5a6-127">INPUTS</span></span>

### <span data-ttu-id="5d5a6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5d5a6-128">System.String</span></span>

### <span data-ttu-id="5d5a6-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="5d5a6-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="5d5a6-130">출력</span><span class="sxs-lookup"><span data-stu-id="5d5a6-130">OUTPUTS</span></span>

### <span data-ttu-id="5d5a6-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="5d5a6-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="5d5a6-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d5a6-132">NOTES</span></span>

## <span data-ttu-id="5d5a6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d5a6-133">RELATED LINKS</span></span>
