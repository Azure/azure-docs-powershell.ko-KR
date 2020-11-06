---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: c22bb41702bb4e338d0548be6c7544d597ef0230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532455"
---
# <span data-ttu-id="c6e1e-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="c6e1e-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="c6e1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e1e-103">지정 된 이벤트 허브 권한 부여 규칙의 기본 키 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6e1e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6e1e-104">SYNTAX</span></span>

### <span data-ttu-id="c6e1e-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6e1e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6e1e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6e1e-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6e1e-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6e1e-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6e1e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c6e1e-108">DESCRIPTION</span></span>
<span data-ttu-id="c6e1e-109">Get-AzureRmEventHubKey cmdlet은 지정 된 네임 스페이스/이벤트 허브/별칭 인증 규칙에 대 한 기본 및 보조 connectionstrings 및 키 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="c6e1e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c6e1e-110">EXAMPLES</span></span>

### <span data-ttu-id="c6e1e-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="c6e1e-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="c6e1e-112">예제 2-EventHub</span><span class="sxs-lookup"><span data-stu-id="c6e1e-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="c6e1e-113">권한 부여 규칙 MyAuthRuleName에 대 한 기본 및 보조 connectionstrings 및 키의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="c6e1e-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="c6e1e-114">예제 3-별칭 (GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="c6e1e-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="c6e1e-115">권한 부여 규칙 MyAuthRuleName에 대 한 기본, 보조, AliasPrimary 및 AliasSecondary connectionstrings 및 키의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="c6e1e-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="c6e1e-116">변수</span><span class="sxs-lookup"><span data-stu-id="c6e1e-116">PARAMETERS</span></span>

### <span data-ttu-id="c6e1e-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="c6e1e-117">-AliasName</span></span>
<span data-ttu-id="c6e1e-118">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="c6e1e-118">Alias Name</span></span>

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

### <span data-ttu-id="c6e1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e1e-119">-DefaultProfile</span></span>
<span data-ttu-id="c6e1e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e1e-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c6e1e-121">-EventHub</span></span>
<span data-ttu-id="c6e1e-122">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="c6e1e-122">EventHub Name</span></span>

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

### <span data-ttu-id="c6e1e-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c6e1e-123">-Name</span></span>
<span data-ttu-id="c6e1e-124">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="c6e1e-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c6e1e-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6e1e-125">-Namespace</span></span>
<span data-ttu-id="c6e1e-126">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="c6e1e-126">Namespace Name</span></span>

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

### <span data-ttu-id="c6e1e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e1e-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6e1e-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c6e1e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="c6e1e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e1e-129">CommonParameters</span></span>
<span data-ttu-id="c6e1e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e1e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e1e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e1e-132">입력</span><span class="sxs-lookup"><span data-stu-id="c6e1e-132">INPUTS</span></span>

### <span data-ttu-id="c6e1e-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6e1e-133">System.String</span></span>

## <span data-ttu-id="c6e1e-134">출력</span><span class="sxs-lookup"><span data-stu-id="c6e1e-134">OUTPUTS</span></span>

### <span data-ttu-id="c6e1e-135">PSListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="c6e1e-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="c6e1e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c6e1e-136">NOTES</span></span>

## <span data-ttu-id="c6e1e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6e1e-137">RELATED LINKS</span></span>
