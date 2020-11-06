---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: c15528befc90a0249101602fef9b178e7a63c0ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530538"
---
# <span data-ttu-id="eadcf-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eadcf-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="eadcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eadcf-102">SYNOPSIS</span></span>
<span data-ttu-id="eadcf-103">지정 된 이벤트 허브 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eadcf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eadcf-104">SYNTAX</span></span>

### <span data-ttu-id="eadcf-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="eadcf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eadcf-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="eadcf-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eadcf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eadcf-107">DESCRIPTION</span></span>
<span data-ttu-id="eadcf-108">Remove-AzureRmEventHubAuthorizationRule cmdlet은 지정 된 이벤트 허브에서 지정한 권한 부여 규칙을 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="eadcf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eadcf-109">EXAMPLES</span></span>

### <span data-ttu-id="eadcf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="eadcf-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="eadcf-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="eadcf-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="eadcf-112">\` \` 이벤트 허브 MyEventHubName에서 권한 부여 규칙 MyAuthRuleName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="eadcf-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="eadcf-113">변수</span><span class="sxs-lookup"><span data-stu-id="eadcf-113">PARAMETERS</span></span>

### <span data-ttu-id="eadcf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadcf-114">-DefaultProfile</span></span>
<span data-ttu-id="eadcf-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eadcf-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="eadcf-116">-EventHub</span></span>
<span data-ttu-id="eadcf-117">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="eadcf-117">EventHub Name</span></span>

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

### <span data-ttu-id="eadcf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="eadcf-118">-Force</span></span>
<span data-ttu-id="eadcf-119">확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="eadcf-119">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadcf-120">-이름</span><span class="sxs-lookup"><span data-stu-id="eadcf-120">-Name</span></span>
<span data-ttu-id="eadcf-121">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="eadcf-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="eadcf-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eadcf-122">-Namespace</span></span>
<span data-ttu-id="eadcf-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="eadcf-123">Namespace Name</span></span>

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

### <span data-ttu-id="eadcf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eadcf-124">-PassThru</span></span>
<span data-ttu-id="eadcf-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eadcf-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadcf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eadcf-127">-ResourceGroupName</span></span>
<span data-ttu-id="eadcf-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="eadcf-128">Resource Group Name</span></span>

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

### <span data-ttu-id="eadcf-129">-확인</span><span class="sxs-lookup"><span data-stu-id="eadcf-129">-Confirm</span></span>
<span data-ttu-id="eadcf-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eadcf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eadcf-131">-WhatIf</span></span>
<span data-ttu-id="eadcf-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eadcf-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eadcf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadcf-134">CommonParameters</span></span>
<span data-ttu-id="eadcf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadcf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eadcf-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eadcf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadcf-137">입력</span><span class="sxs-lookup"><span data-stu-id="eadcf-137">INPUTS</span></span>

### <span data-ttu-id="eadcf-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eadcf-138">System.String</span></span>


## <span data-ttu-id="eadcf-139">출력</span><span class="sxs-lookup"><span data-stu-id="eadcf-139">OUTPUTS</span></span>

### <span data-ttu-id="eadcf-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="eadcf-140">System.Boolean</span></span>


## <span data-ttu-id="eadcf-141">상속자</span><span class="sxs-lookup"><span data-stu-id="eadcf-141">NOTES</span></span>

## <span data-ttu-id="eadcf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eadcf-142">RELATED LINKS</span></span>
