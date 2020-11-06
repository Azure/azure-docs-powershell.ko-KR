---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530670"
---
# <span data-ttu-id="f5848-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f5848-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f5848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5848-102">SYNOPSIS</span></span>
<span data-ttu-id="f5848-103">주어진 네임 스페이스에 대 한 지정 된 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5848-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5848-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5848-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5848-105">DESCRIPTION</span></span>
<span data-ttu-id="f5848-106">**AzureRmServiceBusNamespaceAuthorizationRule** cmdlet은 주어진 네임 스페이스에 지정 된 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="f5848-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5848-107">EXAMPLES</span></span>

### <span data-ttu-id="f5848-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5848-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="f5848-109">지정 된 네임 스페이스에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="f5848-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5848-110">PARAMETERS</span></span>

### <span data-ttu-id="f5848-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5848-111">-ResourceGroup</span></span>
<span data-ttu-id="f5848-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5848-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5848-113">-DefaultProfile</span></span>
<span data-ttu-id="f5848-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5848-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f5848-115">-Name</span></span>
<span data-ttu-id="f5848-116">ServiceBus 네임 스페이스 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5848-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5848-117">-Namespace</span></span>
<span data-ttu-id="f5848-118">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5848-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5848-119">CommonParameters</span></span>
<span data-ttu-id="f5848-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5848-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5848-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5848-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5848-122">입력</span><span class="sxs-lookup"><span data-stu-id="f5848-122">INPUTS</span></span>

### <span data-ttu-id="f5848-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5848-123">-ResourceGroup</span></span>
 <span data-ttu-id="f5848-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5848-124">System.String</span></span>
 

### <span data-ttu-id="f5848-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f5848-125">-NamespaceName</span></span>
 <span data-ttu-id="f5848-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5848-126">System.String</span></span>
 

### <span data-ttu-id="f5848-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f5848-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f5848-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5848-128">System.String</span></span>

## <span data-ttu-id="f5848-129">출력</span><span class="sxs-lookup"><span data-stu-id="f5848-129">OUTPUTS</span></span>

### <span data-ttu-id="f5848-130">System.webserver. List ' 1 [[ServiceBus]. ServiceBus, Version = 0.0.1.0, Culture = 중립, PublicKeyToken = null]). 목록 ' ' [[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="f5848-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f5848-131">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 유형: Microsoft. ServiceBus/AuthorizationRules 이름: AuthoRule1 Location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="f5848-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f5848-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f5848-132">NOTES</span></span>

## <span data-ttu-id="f5848-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5848-133">RELATED LINKS</span></span>

