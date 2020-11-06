---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529148"
---
# <span data-ttu-id="bb892-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bb892-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="bb892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb892-102">SYNOPSIS</span></span>
<span data-ttu-id="bb892-103">지정 된 리소스 그룹에서 서비스 버스 네임 스페이스의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb892-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb892-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb892-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb892-105">DESCRIPTION</span></span>
<span data-ttu-id="bb892-106">**AzureRmServiceBusNamespaceAuthorizationRule** cmdlet은 지정 된 리소스 그룹에 대 한 Service Bus 네임 스페이스의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="bb892-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb892-107">EXAMPLES</span></span>

### <span data-ttu-id="bb892-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb892-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="bb892-109">`SBAuthoRule1`지정 된 리소스 그룹에서 네임 스페이스의 권한 부여 규칙을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="bb892-110">변수</span><span class="sxs-lookup"><span data-stu-id="bb892-110">PARAMETERS</span></span>

### <span data-ttu-id="bb892-111">-확인</span><span class="sxs-lookup"><span data-stu-id="bb892-111">-Confirm</span></span>
<span data-ttu-id="bb892-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb892-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb892-113">-WhatIf</span></span>
<span data-ttu-id="bb892-114">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb892-115">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb892-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb892-116">-DefaultProfile</span></span>
<span data-ttu-id="bb892-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb892-118">-이름</span><span class="sxs-lookup"><span data-stu-id="bb892-118">-Name</span></span>
<span data-ttu-id="bb892-119">네임 스페이스 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-119">Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb892-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bb892-120">-Namespace</span></span>
<span data-ttu-id="bb892-121">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-121">Namespace Name.</span></span>

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

### <span data-ttu-id="bb892-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb892-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb892-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb892-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb892-124">CommonParameters</span></span>
<span data-ttu-id="bb892-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb892-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb892-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb892-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb892-127">입력</span><span class="sxs-lookup"><span data-stu-id="bb892-127">INPUTS</span></span>

### <span data-ttu-id="bb892-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb892-128">-ResourceGroup</span></span>
 <span data-ttu-id="bb892-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb892-129">System.String</span></span>

### <span data-ttu-id="bb892-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="bb892-130">-NamespaceName</span></span>
 <span data-ttu-id="bb892-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb892-131">System.String</span></span>

### <span data-ttu-id="bb892-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="bb892-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="bb892-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb892-133">System.String</span></span>

## <span data-ttu-id="bb892-134">출력</span><span class="sxs-lookup"><span data-stu-id="bb892-134">OUTPUTS</span></span>

### <span data-ttu-id="bb892-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bb892-135">System.Boolean</span></span>

## <span data-ttu-id="bb892-136">상속자</span><span class="sxs-lookup"><span data-stu-id="bb892-136">NOTES</span></span>

## <span data-ttu-id="bb892-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb892-137">RELATED LINKS</span></span>

