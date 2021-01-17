---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323560"
---
# <span data-ttu-id="74c0f-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="74c0f-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="74c0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="74c0f-103">지정된 Event Hubs 권한 부여 규칙의 기본 키 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="74c0f-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="74c0f-104">구문</span><span class="sxs-lookup"><span data-stu-id="74c0f-104">SYNTAX</span></span>

### <span data-ttu-id="74c0f-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="74c0f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74c0f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="74c0f-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74c0f-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="74c0f-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c0f-108">설명</span><span class="sxs-lookup"><span data-stu-id="74c0f-108">DESCRIPTION</span></span>
<span data-ttu-id="74c0f-109">이 Get-AzEventHubKey cmdlet은 지정된 NameSpace/Event Hubs/별칭 권한 부여 규칙의 기본 및 보조 연결 및 키 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="74c0f-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="74c0f-110">예제</span><span class="sxs-lookup"><span data-stu-id="74c0f-110">EXAMPLES</span></span>

### <span data-ttu-id="74c0f-111">예제 1: 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="74c0f-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="74c0f-112">예제 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="74c0f-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="74c0f-113">권한 부여 규칙 \` MyAuthRuleName에 대한 기본 및 보조 연결 및 키에 대한 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="74c0f-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="74c0f-114">예제 3: 별칭(GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="74c0f-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="74c0f-115">권한 부여 규칙 \` MyAuthRuleName에 대한 기본, 보조, AliasPrimary 및 AliasSecondary 연결strings 및 키에 대한 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="74c0f-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="74c0f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74c0f-116">PARAMETERS</span></span>

### <span data-ttu-id="74c0f-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="74c0f-117">-AliasName</span></span>
<span data-ttu-id="74c0f-118">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="74c0f-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c0f-119">-DefaultProfile</span></span>
<span data-ttu-id="74c0f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74c0f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c0f-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="74c0f-121">-EventHub</span></span>
<span data-ttu-id="74c0f-122">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="74c0f-122">EventHub Name</span></span>

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

### <span data-ttu-id="74c0f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="74c0f-123">-Name</span></span>
<span data-ttu-id="74c0f-124">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="74c0f-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="74c0f-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="74c0f-125">-Namespace</span></span>
<span data-ttu-id="74c0f-126">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="74c0f-126">Namespace Name</span></span>

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

### <span data-ttu-id="74c0f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c0f-127">-ResourceGroupName</span></span>
<span data-ttu-id="74c0f-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="74c0f-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c0f-129">CommonParameters</span></span>
<span data-ttu-id="74c0f-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74c0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c0f-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74c0f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c0f-132">입력</span><span class="sxs-lookup"><span data-stu-id="74c0f-132">INPUTS</span></span>

### <span data-ttu-id="74c0f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="74c0f-133">System.String</span></span>

## <span data-ttu-id="74c0f-134">출력</span><span class="sxs-lookup"><span data-stu-id="74c0f-134">OUTPUTS</span></span>

### <span data-ttu-id="74c0f-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="74c0f-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="74c0f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74c0f-136">NOTES</span></span>

## <span data-ttu-id="74c0f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74c0f-137">RELATED LINKS</span></span>
