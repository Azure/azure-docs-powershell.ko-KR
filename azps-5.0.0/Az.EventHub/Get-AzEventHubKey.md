---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218687"
---
# <span data-ttu-id="f2a09-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="f2a09-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="f2a09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2a09-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a09-103">지정 된 이벤트 허브 권한 부여 규칙의 기본 키 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2a09-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="f2a09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2a09-104">SYNTAX</span></span>

### <span data-ttu-id="f2a09-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2a09-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2a09-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f2a09-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2a09-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="f2a09-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2a09-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f2a09-108">DESCRIPTION</span></span>
<span data-ttu-id="f2a09-109">Get-AzEventHubKey cmdlet은 지정 된 네임 스페이스/이벤트 허브/별칭 인증 규칙에 대 한 기본 및 보조 connectionstrings 및 키 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2a09-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="f2a09-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f2a09-110">EXAMPLES</span></span>

### <span data-ttu-id="f2a09-111">예제 1: 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="f2a09-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="f2a09-112">예제 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="f2a09-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="f2a09-113">권한 부여 규칙 MyAuthRuleName에 대 한 기본 및 보조 connectionstrings 및 키의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="f2a09-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="f2a09-114">예제 3: 별칭 (GeoRecovery 구성)</span><span class="sxs-lookup"><span data-stu-id="f2a09-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="f2a09-115">권한 부여 규칙 MyAuthRuleName에 대 한 기본, 보조, AliasPrimary 및 AliasSecondary connectionstrings 및 키의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="f2a09-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="f2a09-116">변수</span><span class="sxs-lookup"><span data-stu-id="f2a09-116">PARAMETERS</span></span>

### <span data-ttu-id="f2a09-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f2a09-117">-AliasName</span></span>
<span data-ttu-id="f2a09-118">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="f2a09-118">Alias Name</span></span>

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

### <span data-ttu-id="f2a09-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a09-119">-DefaultProfile</span></span>
<span data-ttu-id="f2a09-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2a09-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2a09-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f2a09-121">-EventHub</span></span>
<span data-ttu-id="f2a09-122">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="f2a09-122">EventHub Name</span></span>

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

### <span data-ttu-id="f2a09-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f2a09-123">-Name</span></span>
<span data-ttu-id="f2a09-124">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="f2a09-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f2a09-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f2a09-125">-Namespace</span></span>
<span data-ttu-id="f2a09-126">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="f2a09-126">Namespace Name</span></span>

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

### <span data-ttu-id="f2a09-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a09-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2a09-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f2a09-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f2a09-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a09-129">CommonParameters</span></span>
<span data-ttu-id="f2a09-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2a09-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a09-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a09-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a09-132">입력</span><span class="sxs-lookup"><span data-stu-id="f2a09-132">INPUTS</span></span>

### <span data-ttu-id="f2a09-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2a09-133">System.String</span></span>

## <span data-ttu-id="f2a09-134">출력</span><span class="sxs-lookup"><span data-stu-id="f2a09-134">OUTPUTS</span></span>

### <span data-ttu-id="f2a09-135">PSListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="f2a09-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="f2a09-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f2a09-136">NOTES</span></span>

## <span data-ttu-id="f2a09-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2a09-137">RELATED LINKS</span></span>
