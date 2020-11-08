---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216098"
---
# <span data-ttu-id="e21a2-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="e21a2-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="e21a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e21a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e21a2-103">새 버전의 청사진을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="e21a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e21a2-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e21a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e21a2-105">DESCRIPTION</span></span>
<span data-ttu-id="e21a2-106">새 버전의 청사진 정의를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e21a2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e21a2-107">EXAMPLES</span></span>

### <span data-ttu-id="e21a2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e21a2-108">Example 1</span></span>
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

<span data-ttu-id="e21a2-109">새 버전의 청사진 정의를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e21a2-110">변수</span><span class="sxs-lookup"><span data-stu-id="e21a2-110">PARAMETERS</span></span>

### <span data-ttu-id="e21a2-111">-청사진</span><span class="sxs-lookup"><span data-stu-id="e21a2-111">-Blueprint</span></span>
<span data-ttu-id="e21a2-112">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="e21a2-112">Blueprint object.</span></span>

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

### <span data-ttu-id="e21a2-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="e21a2-113">-ChangeNote</span></span>
<span data-ttu-id="e21a2-114">이 청사진 버전의 내용에 대 한 설명을 참고 하세요.</span><span class="sxs-lookup"><span data-stu-id="e21a2-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="e21a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21a2-115">-DefaultProfile</span></span>
<span data-ttu-id="e21a2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21a2-117">-버전</span><span class="sxs-lookup"><span data-stu-id="e21a2-117">-Version</span></span>
<span data-ttu-id="e21a2-118">청사진 정의 버전.</span><span class="sxs-lookup"><span data-stu-id="e21a2-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="e21a2-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e21a2-119">-Confirm</span></span>
<span data-ttu-id="e21a2-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e21a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e21a2-121">-WhatIf</span></span>
<span data-ttu-id="e21a2-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e21a2-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e21a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21a2-124">CommonParameters</span></span>
<span data-ttu-id="e21a2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e21a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21a2-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e21a2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21a2-127">입력</span><span class="sxs-lookup"><span data-stu-id="e21a2-127">INPUTS</span></span>

### <span data-ttu-id="e21a2-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e21a2-128">System.String</span></span>

### <span data-ttu-id="e21a2-129">Microsoft. m a. 모델. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="e21a2-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="e21a2-130">출력</span><span class="sxs-lookup"><span data-stu-id="e21a2-130">OUTPUTS</span></span>

### <span data-ttu-id="e21a2-131">PSPublishedBlueprint (.).</span><span class="sxs-lookup"><span data-stu-id="e21a2-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="e21a2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e21a2-132">NOTES</span></span>

## <span data-ttu-id="e21a2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e21a2-133">RELATED LINKS</span></span>
