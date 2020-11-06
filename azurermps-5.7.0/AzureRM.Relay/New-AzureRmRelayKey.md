---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533664"
---
# <span data-ttu-id="ff4ea-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="ff4ea-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="ff4ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4ea-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff4ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff4ea-104">SYNTAX</span></span>

### <span data-ttu-id="ff4ea-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff4ea-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff4ea-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff4ea-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff4ea-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff4ea-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff4ea-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ff4ea-108">DESCRIPTION</span></span>
<span data-ttu-id="ff4ea-109">**AzureRmRelayKey** cmdlet은 지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ff4ea-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ff4ea-110">EXAMPLES</span></span>

### <span data-ttu-id="ff4ea-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="ff4ea-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="ff4ea-112">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ff4ea-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="ff4ea-113">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ff4ea-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="ff4ea-114">지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ff4ea-115">변수</span><span class="sxs-lookup"><span data-stu-id="ff4ea-115">PARAMETERS</span></span>

### <span data-ttu-id="ff4ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4ea-116">-DefaultProfile</span></span>
<span data-ttu-id="ff4ea-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff4ea-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ff4ea-118">-HybridConnection</span></span>
<span data-ttu-id="ff4ea-119">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ff4ea-120">-Name</span></span>
<span data-ttu-id="ff4ea-121">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff4ea-122">-Namespace</span></span>
<span data-ttu-id="ff4ea-123">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ff4ea-124">-RegenerateKey</span></span>
<span data-ttu-id="ff4ea-125">' PrimaryKey '/' SecondaryKey ' 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff4ea-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff4ea-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ff4ea-128">-WcfRelay</span></span>
<span data-ttu-id="ff4ea-129">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ff4ea-130">-Confirm</span></span>
<span data-ttu-id="ff4ea-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff4ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff4ea-132">-WhatIf</span></span>
<span data-ttu-id="ff4ea-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff4ea-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff4ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4ea-135">CommonParameters</span></span>
<span data-ttu-id="ff4ea-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4ea-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4ea-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4ea-138">입력</span><span class="sxs-lookup"><span data-stu-id="ff4ea-138">INPUTS</span></span>

### <span data-ttu-id="ff4ea-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="ff4ea-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff4ea-140">System.String</span></span> 

### <span data-ttu-id="ff4ea-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-141">-NamespaceName</span></span>
 <span data-ttu-id="ff4ea-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff4ea-142">System.String</span></span> 
 

### <span data-ttu-id="ff4ea-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="ff4ea-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff4ea-144">System.String</span></span> 

### <span data-ttu-id="ff4ea-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-145">-WcfRelayName</span></span>
 <span data-ttu-id="ff4ea-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff4ea-146">System.String</span></span> 

### <span data-ttu-id="ff4ea-147">-이름</span><span class="sxs-lookup"><span data-stu-id="ff4ea-147">-Name</span></span>
 <span data-ttu-id="ff4ea-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff4ea-148">System.String</span></span>

### <span data-ttu-id="ff4ea-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="ff4ea-149">-RegenerateKeys</span></span>
 <span data-ttu-id="ff4ea-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff4ea-150">System.String</span></span>

## <span data-ttu-id="ff4ea-151">출력</span><span class="sxs-lookup"><span data-stu-id="ff4ea-151">OUTPUTS</span></span>

### <span data-ttu-id="ff4ea-152">AuthorizationRuleKeysAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="ff4ea-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="ff4ea-153">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="ff4ea-153">Example 1 - Namespace</span></span>
<span data-ttu-id="ff4ea-154">PrimaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/ SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="ff4ea-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="ff4ea-155">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ff4ea-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="ff4ea-156">PrimaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="ff4ea-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="ff4ea-157">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ff4ea-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="ff4ea-158">PrimaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="ff4ea-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="ff4ea-159">상속자</span><span class="sxs-lookup"><span data-stu-id="ff4ea-159">NOTES</span></span>

## <span data-ttu-id="ff4ea-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff4ea-160">RELATED LINKS</span></span>

