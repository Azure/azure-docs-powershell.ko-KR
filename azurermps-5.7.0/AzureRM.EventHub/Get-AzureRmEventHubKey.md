---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534815"
---
# <span data-ttu-id="eec1e-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="eec1e-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="eec1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec1e-102">SYNOPSIS</span></span>
<span data-ttu-id="eec1e-103">지정 된 이벤트 허브 권한 부여 규칙의 기본 키 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eec1e-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eec1e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eec1e-104">SYNTAX</span></span>

### <span data-ttu-id="eec1e-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="eec1e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eec1e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eec1e-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eec1e-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="eec1e-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eec1e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eec1e-108">DESCRIPTION</span></span>
<span data-ttu-id="eec1e-109">Get-AzureRmEventHubKey cmdlet은 지정 된 네임 스페이스/이벤트 허브/별칭 인증 규칙에 대 한 기본 및 보조 connectionstrings 및 키 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eec1e-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="eec1e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="eec1e-110">EXAMPLES</span></span>

### <span data-ttu-id="eec1e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="eec1e-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="eec1e-112">권한 부여 규칙 MyAuthRuleName에 대 한 기본 및 보조 connectionstrings 및 키의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="eec1e-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="eec1e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="eec1e-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="eec1e-114">권한 부여 규칙 MyAuthRuleName에 대 한 기본, 보조, AliasPrimary 및 AliasSecondary connectionstrings 및 키의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="eec1e-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="eec1e-115">변수</span><span class="sxs-lookup"><span data-stu-id="eec1e-115">PARAMETERS</span></span>

### <span data-ttu-id="eec1e-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="eec1e-116">-AliasName</span></span>
<span data-ttu-id="eec1e-117">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="eec1e-117">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec1e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec1e-118">-DefaultProfile</span></span>
<span data-ttu-id="eec1e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eec1e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec1e-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="eec1e-120">-EventHub</span></span>
<span data-ttu-id="eec1e-121">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="eec1e-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec1e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="eec1e-122">-Name</span></span>
<span data-ttu-id="eec1e-123">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="eec1e-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec1e-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eec1e-124">-Namespace</span></span>
<span data-ttu-id="eec1e-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="eec1e-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec1e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec1e-126">-ResourceGroupName</span></span>
<span data-ttu-id="eec1e-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="eec1e-127">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec1e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec1e-128">CommonParameters</span></span>
<span data-ttu-id="eec1e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eec1e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eec1e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec1e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec1e-131">입력</span><span class="sxs-lookup"><span data-stu-id="eec1e-131">INPUTS</span></span>

### <span data-ttu-id="eec1e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eec1e-132">System.String</span></span>


## <span data-ttu-id="eec1e-133">출력</span><span class="sxs-lookup"><span data-stu-id="eec1e-133">OUTPUTS</span></span>

### <span data-ttu-id="eec1e-134">PSListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="eec1e-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="eec1e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="eec1e-135">NOTES</span></span>

## <span data-ttu-id="eec1e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eec1e-136">RELATED LINKS</span></span>
