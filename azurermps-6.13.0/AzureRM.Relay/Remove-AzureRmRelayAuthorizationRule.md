---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: cebc4680e4c24bb7e19342d32e4aedd57b960e55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702092"
---
# <span data-ttu-id="e4088-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e4088-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="e4088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4088-102">SYNOPSIS</span></span>
<span data-ttu-id="e4088-103">지정 된 릴레이 엔터티에서 HybridConnection의 권한 부여 규칙을 제거 합니다 (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e4088-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4088-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4088-104">SYNTAX</span></span>

### <span data-ttu-id="e4088-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4088-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4088-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4088-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4088-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4088-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4088-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e4088-108">DESCRIPTION</span></span>
<span data-ttu-id="e4088-109">**AzureRmRelayAuthorizationRule** cmdlet은 지정 된 릴레이 엔티티의 권한 부여 규칙 (Namespace/WcfRelay/HybridConnection)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e4088-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e4088-110">EXAMPLES</span></span>

### <span data-ttu-id="e4088-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4088-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="e4088-112">네임 스페이스의 권한 부여 규칙을 제거 합니다 `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="e4088-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="e4088-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e4088-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="e4088-114">`AuthoRule1`네임 스페이스에서 WcfRelay의 권한 부여 규칙을 제거 합니다 `TestWcfRelay` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="e4088-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="e4088-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e4088-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="e4088-116">`AuthoRule1`네임 스페이스에서 HybridConnection의 권한 부여 규칙을 제거 합니다 `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="e4088-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="e4088-117">변수</span><span class="sxs-lookup"><span data-stu-id="e4088-117">PARAMETERS</span></span>

### <span data-ttu-id="e4088-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4088-118">-DefaultProfile</span></span>
<span data-ttu-id="e4088-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4088-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e4088-120">-Force</span></span>
<span data-ttu-id="e4088-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4088-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e4088-122">-HybridConnection</span></span>
<span data-ttu-id="e4088-123">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4088-124">-이름</span><span class="sxs-lookup"><span data-stu-id="e4088-124">-Name</span></span>
<span data-ttu-id="e4088-125">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4088-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4088-126">-Namespace</span></span>
<span data-ttu-id="e4088-127">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4088-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4088-128">-PassThru</span></span>
<span data-ttu-id="e4088-129">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="e4088-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4088-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4088-130">-ResourceGroupName</span></span>
<span data-ttu-id="e4088-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4088-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e4088-132">-WcfRelay</span></span>
<span data-ttu-id="e4088-133">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4088-134">-확인</span><span class="sxs-lookup"><span data-stu-id="e4088-134">-Confirm</span></span>
<span data-ttu-id="e4088-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4088-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4088-136">-WhatIf</span></span>
<span data-ttu-id="e4088-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4088-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4088-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4088-139">CommonParameters</span></span>
<span data-ttu-id="e4088-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4088-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e4088-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4088-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4088-142">입력</span><span class="sxs-lookup"><span data-stu-id="e4088-142">INPUTS</span></span>

### <span data-ttu-id="e4088-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4088-143">System.String</span></span>


## <span data-ttu-id="e4088-144">출력</span><span class="sxs-lookup"><span data-stu-id="e4088-144">OUTPUTS</span></span>

### <span data-ttu-id="e4088-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e4088-145">System.Boolean</span></span>


## <span data-ttu-id="e4088-146">상속자</span><span class="sxs-lookup"><span data-stu-id="e4088-146">NOTES</span></span>

## <span data-ttu-id="e4088-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4088-147">RELATED LINKS</span></span>
