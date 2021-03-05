---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: bc1ec66846037a7081af85809f2187b5d35aecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010832"
---
# <span data-ttu-id="3e65f-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="3e65f-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="3e65f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e65f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e65f-103">청사진의 새 버전을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="3e65f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e65f-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e65f-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e65f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e65f-106">청사진 정의의 새 버전을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="3e65f-107">예제</span><span class="sxs-lookup"><span data-stu-id="3e65f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e65f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3e65f-108">Example 1</span></span>
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

<span data-ttu-id="3e65f-109">청사진 정의의 새 버전을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="3e65f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3e65f-110">PARAMETERS</span></span>

### <span data-ttu-id="3e65f-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="3e65f-111">-Blueprint</span></span>
<span data-ttu-id="3e65f-112">청사진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-112">Blueprint object.</span></span>

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

### <span data-ttu-id="3e65f-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="3e65f-113">-ChangeNote</span></span>
<span data-ttu-id="3e65f-114">이 청사진 버전의 내용을 설명하는 참고 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="3e65f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e65f-115">-DefaultProfile</span></span>
<span data-ttu-id="3e65f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e65f-117">-Version</span><span class="sxs-lookup"><span data-stu-id="3e65f-117">-Version</span></span>
<span data-ttu-id="3e65f-118">청사진 정의에 대한 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="3e65f-119">-확인</span><span class="sxs-lookup"><span data-stu-id="3e65f-119">-Confirm</span></span>
<span data-ttu-id="3e65f-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e65f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e65f-121">-WhatIf</span></span>
<span data-ttu-id="3e65f-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e65f-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e65f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e65f-124">CommonParameters</span></span>
<span data-ttu-id="3e65f-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e65f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e65f-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e65f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e65f-127">입력</span><span class="sxs-lookup"><span data-stu-id="3e65f-127">INPUTS</span></span>

### <span data-ttu-id="3e65f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3e65f-128">System.String</span></span>

### <span data-ttu-id="3e65f-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="3e65f-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="3e65f-130">출력</span><span class="sxs-lookup"><span data-stu-id="3e65f-130">OUTPUTS</span></span>

### <span data-ttu-id="3e65f-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="3e65f-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="3e65f-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e65f-132">NOTES</span></span>

## <span data-ttu-id="3e65f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e65f-133">RELATED LINKS</span></span>
