---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: f9f4eb7f60683524eccec8b3d35926b86fa52bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957243"
---
# <span data-ttu-id="44ae2-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="44ae2-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="44ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="44ae2-103">지정된 Event Hubs 권한 부여 규칙의 기본 키 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44ae2-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="44ae2-104">구문</span><span class="sxs-lookup"><span data-stu-id="44ae2-104">SYNTAX</span></span>

### <span data-ttu-id="44ae2-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="44ae2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44ae2-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="44ae2-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44ae2-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="44ae2-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ae2-108">설명</span><span class="sxs-lookup"><span data-stu-id="44ae2-108">DESCRIPTION</span></span>
<span data-ttu-id="44ae2-109">Get-AzEventHubKey cmdlet은 지정된 NameSpace/Event Hubs/별칭 권한 부여 규칙의 기본 및 보조 연결스트링 및 키 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="44ae2-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="44ae2-110">예제</span><span class="sxs-lookup"><span data-stu-id="44ae2-110">EXAMPLES</span></span>

### <span data-ttu-id="44ae2-111">예제 1: 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="44ae2-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="44ae2-112">예제 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="44ae2-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="44ae2-113">권한 부여 규칙 \` MyAuthRuleName에 대한 기본 및 보조 연결스트링 및 키에 대한 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44ae2-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="44ae2-114">예제 3: 별칭(GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="44ae2-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="44ae2-115">권한 부여 규칙 \` MyAuthRuleName에 대한 기본, 보조, AliasPrimary 및 AliasSecondary 연결스트링 및 키에 대한 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="44ae2-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="44ae2-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="44ae2-116">PARAMETERS</span></span>

### <span data-ttu-id="44ae2-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="44ae2-117">-AliasName</span></span>
<span data-ttu-id="44ae2-118">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="44ae2-118">Alias Name</span></span>

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

### <span data-ttu-id="44ae2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ae2-119">-DefaultProfile</span></span>
<span data-ttu-id="44ae2-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44ae2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ae2-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="44ae2-121">-EventHub</span></span>
<span data-ttu-id="44ae2-122">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="44ae2-122">EventHub Name</span></span>

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

### <span data-ttu-id="44ae2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="44ae2-123">-Name</span></span>
<span data-ttu-id="44ae2-124">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="44ae2-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="44ae2-125">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="44ae2-125">-Namespace</span></span>
<span data-ttu-id="44ae2-126">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="44ae2-126">Namespace Name</span></span>

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

### <span data-ttu-id="44ae2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ae2-127">-ResourceGroupName</span></span>
<span data-ttu-id="44ae2-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="44ae2-128">Resource Group Name</span></span>

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

### <span data-ttu-id="44ae2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ae2-129">CommonParameters</span></span>
<span data-ttu-id="44ae2-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44ae2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ae2-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44ae2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ae2-132">입력</span><span class="sxs-lookup"><span data-stu-id="44ae2-132">INPUTS</span></span>

### <span data-ttu-id="44ae2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="44ae2-133">System.String</span></span>

## <span data-ttu-id="44ae2-134">출력</span><span class="sxs-lookup"><span data-stu-id="44ae2-134">OUTPUTS</span></span>

### <span data-ttu-id="44ae2-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="44ae2-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="44ae2-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44ae2-136">NOTES</span></span>

## <span data-ttu-id="44ae2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44ae2-137">RELATED LINKS</span></span>
