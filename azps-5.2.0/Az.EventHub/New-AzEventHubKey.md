---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370735"
---
# <span data-ttu-id="f56a4-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="f56a4-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="f56a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f56a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f56a4-103">지정된 Event Hubs 권한 부여 규칙에 대한 새 기본 또는 보조 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f56a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="f56a4-104">SYNTAX</span></span>

### <span data-ttu-id="f56a4-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f56a4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f56a4-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f56a4-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f56a4-107">설명</span><span class="sxs-lookup"><span data-stu-id="f56a4-107">DESCRIPTION</span></span>
<span data-ttu-id="f56a4-108">이 New-AzEventHubKey cmdlet은 지정된 Event Hubs 권한 부여 규칙에 대한 기본 또는 보조 SAS 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f56a4-109">예제</span><span class="sxs-lookup"><span data-stu-id="f56a4-109">EXAMPLES</span></span>

### <span data-ttu-id="f56a4-110">예제 1: 네임스페이스 - AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f56a4-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f56a4-111">권한 부여 규칙 \` MyAuthRuleName에 대한 기본 키를 다시 \` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f56a4-112">예제 2: EventHub - AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f56a4-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="f56a4-113">권한 부여 규칙 \` MyAuthRuleName에 대한 기본 키를 다시 \` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f56a4-114">예제 3: - 네임스페이스 - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f56a4-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="f56a4-115">예제 4: EventHub - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f56a4-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="f56a4-116">권한 부여 규칙 \` MyAuthRuleName에 대한 보조 키를 다시 \` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="f56a4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f56a4-117">PARAMETERS</span></span>

### <span data-ttu-id="f56a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56a4-118">-DefaultProfile</span></span>
<span data-ttu-id="f56a4-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f56a4-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f56a4-120">-EventHub</span></span>
<span data-ttu-id="f56a4-121">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="f56a4-121">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f56a4-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="f56a4-122">-KeyValue</span></span>
<span data-ttu-id="f56a4-123">SAS 토큰 서명 및 유효성을 검사하기 위한 base64로 인코딩된 256비트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56a4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f56a4-124">-Name</span></span>
<span data-ttu-id="f56a4-125">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="f56a4-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f56a4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f56a4-126">-Namespace</span></span>
<span data-ttu-id="f56a4-127">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="f56a4-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f56a4-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f56a4-128">-RegenerateKey</span></span>
<span data-ttu-id="f56a4-129">키 다시 생성 - 'PrimaryKey'/'SecondaryKey'</span><span class="sxs-lookup"><span data-stu-id="f56a4-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f56a4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56a4-130">-ResourceGroupName</span></span>
<span data-ttu-id="f56a4-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f56a4-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f56a4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f56a4-132">-Confirm</span></span>
<span data-ttu-id="f56a4-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f56a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f56a4-134">-WhatIf</span></span>
<span data-ttu-id="f56a4-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f56a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f56a4-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f56a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56a4-137">CommonParameters</span></span>
<span data-ttu-id="f56a4-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f56a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56a4-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f56a4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56a4-140">입력</span><span class="sxs-lookup"><span data-stu-id="f56a4-140">INPUTS</span></span>

### <span data-ttu-id="f56a4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f56a4-141">System.String</span></span>

## <span data-ttu-id="f56a4-142">출력</span><span class="sxs-lookup"><span data-stu-id="f56a4-142">OUTPUTS</span></span>

### <span data-ttu-id="f56a4-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f56a4-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="f56a4-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f56a4-144">NOTES</span></span>

## <span data-ttu-id="f56a4-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f56a4-145">RELATED LINKS</span></span>
