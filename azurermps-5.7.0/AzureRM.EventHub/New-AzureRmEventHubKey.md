---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703056"
---
# <span data-ttu-id="874f0-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="874f0-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="874f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="874f0-102">SYNOPSIS</span></span>
<span data-ttu-id="874f0-103">지정 된 이벤트 허브 권한 부여 규칙에 대 한 새 기본 또는 보조 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="874f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="874f0-104">SYNTAX</span></span>

### <span data-ttu-id="874f0-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="874f0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="874f0-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="874f0-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="874f0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="874f0-107">DESCRIPTION</span></span>
<span data-ttu-id="874f0-108">New-AzureRmEventHubKey cmdlet은 지정 된 이벤트 허브 권한 부여 규칙에 대 한 기본 또는 보조 SAS 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="874f0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="874f0-109">EXAMPLES</span></span>

### <span data-ttu-id="874f0-110">예제 1.1</span><span class="sxs-lookup"><span data-stu-id="874f0-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="874f0-111">권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="874f0-112">예제 1.2</span><span class="sxs-lookup"><span data-stu-id="874f0-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="874f0-113">권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="874f0-114">예제 2.1</span><span class="sxs-lookup"><span data-stu-id="874f0-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="874f0-115">예제 2.2</span><span class="sxs-lookup"><span data-stu-id="874f0-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="874f0-116">권한 부여 규칙 MyAuthRuleName에 대 한 보조 키를 다시 생성 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="874f0-117">변수</span><span class="sxs-lookup"><span data-stu-id="874f0-117">PARAMETERS</span></span>

### <span data-ttu-id="874f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="874f0-118">-DefaultProfile</span></span>
<span data-ttu-id="874f0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="874f0-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="874f0-120">-EventHub</span></span>
<span data-ttu-id="874f0-121">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="874f0-121">EventHub Name</span></span>

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

### <span data-ttu-id="874f0-122">-이름</span><span class="sxs-lookup"><span data-stu-id="874f0-122">-Name</span></span>
<span data-ttu-id="874f0-123">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="874f0-123">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="874f0-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="874f0-124">-Namespace</span></span>
<span data-ttu-id="874f0-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="874f0-125">Namespace Name</span></span>

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

### <span data-ttu-id="874f0-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="874f0-126">-RegenerateKey</span></span>
<span data-ttu-id="874f0-127">키 다시 생성-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="874f0-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="874f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="874f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="874f0-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="874f0-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="874f0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="874f0-130">-Confirm</span></span>
<span data-ttu-id="874f0-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="874f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="874f0-132">-WhatIf</span></span>
<span data-ttu-id="874f0-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="874f0-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="874f0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874f0-135">CommonParameters</span></span>
<span data-ttu-id="874f0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="874f0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="874f0-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874f0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874f0-138">입력</span><span class="sxs-lookup"><span data-stu-id="874f0-138">INPUTS</span></span>

### <span data-ttu-id="874f0-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="874f0-139">System.String</span></span>


## <span data-ttu-id="874f0-140">출력</span><span class="sxs-lookup"><span data-stu-id="874f0-140">OUTPUTS</span></span>

### <span data-ttu-id="874f0-141">PSListKeysAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="874f0-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="874f0-142">상속자</span><span class="sxs-lookup"><span data-stu-id="874f0-142">NOTES</span></span>

## <span data-ttu-id="874f0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="874f0-143">RELATED LINKS</span></span>
