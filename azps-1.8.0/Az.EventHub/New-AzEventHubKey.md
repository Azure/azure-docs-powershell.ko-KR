---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: bb66aacb406871731cb2f356c19a91e8bb27429c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700833"
---
# <span data-ttu-id="d129f-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="d129f-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="d129f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d129f-102">SYNOPSIS</span></span>
<span data-ttu-id="d129f-103">지정 된 이벤트 허브 권한 부여 규칙에 대 한 새 기본 또는 보조 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="d129f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d129f-104">SYNTAX</span></span>

### <span data-ttu-id="d129f-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d129f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d129f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d129f-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d129f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d129f-107">DESCRIPTION</span></span>
<span data-ttu-id="d129f-108">New-AzEventHubKey cmdlet은 지정 된 이벤트 허브 권한 부여 규칙에 대 한 기본 또는 보조 SAS 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="d129f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d129f-109">EXAMPLES</span></span>

### <span data-ttu-id="d129f-110">예제 1.1-Namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d129f-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="d129f-111">권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="d129f-112">예제 1.2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d129f-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="d129f-113">권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="d129f-114">예제 2.1-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d129f-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="d129f-115">예제 2.2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d129f-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="d129f-116">권한 부여 규칙 MyAuthRuleName에 대 한 보조 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="d129f-117">변수</span><span class="sxs-lookup"><span data-stu-id="d129f-117">PARAMETERS</span></span>

### <span data-ttu-id="d129f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d129f-118">-DefaultProfile</span></span>
<span data-ttu-id="d129f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d129f-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d129f-120">-EventHub</span></span>
<span data-ttu-id="d129f-121">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="d129f-121">EventHub Name</span></span>

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

### <span data-ttu-id="d129f-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="d129f-122">-KeyValue</span></span>
<span data-ttu-id="d129f-123">SAS 토큰에 서명 하 고 유효성을 검사 하기 위한 base64 인코딩된 256 비트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="d129f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d129f-124">-Name</span></span>
<span data-ttu-id="d129f-125">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="d129f-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="d129f-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d129f-126">-Namespace</span></span>
<span data-ttu-id="d129f-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="d129f-127">Namespace Name</span></span>

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

### <span data-ttu-id="d129f-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="d129f-128">-RegenerateKey</span></span>
<span data-ttu-id="d129f-129">키 다시 생성-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="d129f-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="d129f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d129f-130">-ResourceGroupName</span></span>
<span data-ttu-id="d129f-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d129f-131">Resource Group Name</span></span>

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

### <span data-ttu-id="d129f-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d129f-132">-Confirm</span></span>
<span data-ttu-id="d129f-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d129f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d129f-134">-WhatIf</span></span>
<span data-ttu-id="d129f-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d129f-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d129f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d129f-137">CommonParameters</span></span>
<span data-ttu-id="d129f-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d129f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d129f-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d129f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d129f-140">입력</span><span class="sxs-lookup"><span data-stu-id="d129f-140">INPUTS</span></span>

### <span data-ttu-id="d129f-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d129f-141">System.String</span></span>

## <span data-ttu-id="d129f-142">출력</span><span class="sxs-lookup"><span data-stu-id="d129f-142">OUTPUTS</span></span>

### <span data-ttu-id="d129f-143">PSListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="d129f-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="d129f-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d129f-144">NOTES</span></span>

## <span data-ttu-id="d129f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d129f-145">RELATED LINKS</span></span>
