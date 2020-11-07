---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 44e1571dbd6da015e163a69716f06d3ed3cebde5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702415"
---
# <span data-ttu-id="62541-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="62541-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="62541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62541-102">SYNOPSIS</span></span>
<span data-ttu-id="62541-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62541-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62541-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62541-104">SYNTAX</span></span>

### <span data-ttu-id="62541-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="62541-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62541-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="62541-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62541-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="62541-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62541-108">설명은</span><span class="sxs-lookup"><span data-stu-id="62541-108">DESCRIPTION</span></span>
<span data-ttu-id="62541-109">**AzureRmRelayKey** cmdlet은 지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="62541-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="62541-110">예제의</span><span class="sxs-lookup"><span data-stu-id="62541-110">EXAMPLES</span></span>

### <span data-ttu-id="62541-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="62541-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="62541-112">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="62541-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="62541-113">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="62541-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="62541-114">지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="62541-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="62541-115">변수</span><span class="sxs-lookup"><span data-stu-id="62541-115">PARAMETERS</span></span>

### <span data-ttu-id="62541-116">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="62541-116">-HybridConnection</span></span>
<span data-ttu-id="62541-117">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62541-117">HybridConnection Name.</span></span>

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

### <span data-ttu-id="62541-118">-이름</span><span class="sxs-lookup"><span data-stu-id="62541-118">-Name</span></span>
<span data-ttu-id="62541-119">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62541-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="62541-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="62541-120">-Namespace</span></span>
<span data-ttu-id="62541-121">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62541-121">Namespace Name.</span></span>

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

### <span data-ttu-id="62541-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62541-122">-ResourceGroupName</span></span>
<span data-ttu-id="62541-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62541-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="62541-124">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="62541-124">-WcfRelay</span></span>
<span data-ttu-id="62541-125">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62541-125">WcfRelay Name.</span></span>

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

### <span data-ttu-id="62541-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62541-126">-DefaultProfile</span></span>
<span data-ttu-id="62541-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62541-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62541-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62541-128">CommonParameters</span></span>
<span data-ttu-id="62541-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62541-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62541-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62541-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62541-131">입력</span><span class="sxs-lookup"><span data-stu-id="62541-131">INPUTS</span></span>

### <span data-ttu-id="62541-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62541-132">-ResourceGroupName</span></span>
 <span data-ttu-id="62541-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62541-133">System.String</span></span> 

### <span data-ttu-id="62541-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="62541-134">-NamespaceName</span></span>
 <span data-ttu-id="62541-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62541-135">System.String</span></span> 
 

### <span data-ttu-id="62541-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="62541-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="62541-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62541-137">System.String</span></span> 

### <span data-ttu-id="62541-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="62541-138">-WcfRelayName</span></span>
 <span data-ttu-id="62541-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62541-139">System.String</span></span> 

### <span data-ttu-id="62541-140">-이름</span><span class="sxs-lookup"><span data-stu-id="62541-140">-Name</span></span>
 <span data-ttu-id="62541-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62541-141">System.String</span></span>

## <span data-ttu-id="62541-142">출력</span><span class="sxs-lookup"><span data-stu-id="62541-142">OUTPUTS</span></span>

### <span data-ttu-id="62541-143">AuthorizationRuleKeysAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="62541-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="62541-144">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="62541-144">Example 1 - Namespace</span></span>
<span data-ttu-id="62541-145">PrimaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/ SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="62541-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="62541-146">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="62541-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="62541-147">PrimaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="62541-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="62541-148">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="62541-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="62541-149">PrimaryConnectionString: 끝점 = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = sb://testnamespace-relay1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="62541-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="62541-150">상속자</span><span class="sxs-lookup"><span data-stu-id="62541-150">NOTES</span></span>

## <span data-ttu-id="62541-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62541-151">RELATED LINKS</span></span>

