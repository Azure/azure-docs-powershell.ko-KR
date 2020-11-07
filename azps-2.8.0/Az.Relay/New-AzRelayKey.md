---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: b768b7838629ce25e4202ca309de8741cfa7f0de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871933"
---
# <span data-ttu-id="d4e14-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="d4e14-101">New-AzRelayKey</span></span>

## <span data-ttu-id="d4e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e14-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e14-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="d4e14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4e14-104">SYNTAX</span></span>

### <span data-ttu-id="d4e14-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d4e14-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e14-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4e14-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4e14-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4e14-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e14-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d4e14-108">DESCRIPTION</span></span>
<span data-ttu-id="d4e14-109">**AzRelayKey** cmdlet은 지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d4e14-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d4e14-110">EXAMPLES</span></span>

### <span data-ttu-id="d4e14-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="d4e14-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="d4e14-112">지정 된 Relay-Namespace 엔터티에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="d4e14-113">예제 1.1-네임 스페이스 KeyValue 제공</span><span class="sxs-lookup"><span data-stu-id="d4e14-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="d4e14-114">키 값을 제공 하 여 지정 된 Relay-Namespace 엔터티에 대 한 기본 또는 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="d4e14-115">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d4e14-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="d4e14-116">지정 된 Relay-WcfRelay 엔터티에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="d4e14-117">예제 2.1-WcfRelay KeyValue 제공 됨</span><span class="sxs-lookup"><span data-stu-id="d4e14-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="d4e14-118">키 값을 제공 하 여 지정 된 Relay-WcfRelay 엔터티에 대 한 기본 또는 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="d4e14-119">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d4e14-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="d4e14-120">지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="d4e14-121">예제 3.1-HybridConnection KeyValue 제공 됨</span><span class="sxs-lookup"><span data-stu-id="d4e14-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="d4e14-122">키 값을 제공 하 여 지정 된 Relay-HybridConnection 엔터티에 대 한 기본 또는 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="d4e14-123">변수</span><span class="sxs-lookup"><span data-stu-id="d4e14-123">PARAMETERS</span></span>

### <span data-ttu-id="d4e14-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e14-124">-DefaultProfile</span></span>
<span data-ttu-id="d4e14-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e14-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d4e14-126">-HybridConnection</span></span>
<span data-ttu-id="d4e14-127">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="d4e14-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="d4e14-128">-KeyValue</span></span>
<span data-ttu-id="d4e14-129">SAS 토큰에 서명 하 고 유효성을 검사 하기 위한 base64 인코딩된 256 비트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e14-130">-이름</span><span class="sxs-lookup"><span data-stu-id="d4e14-130">-Name</span></span>
<span data-ttu-id="d4e14-131">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="d4e14-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4e14-132">-Namespace</span></span>
<span data-ttu-id="d4e14-133">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-133">Namespace Name.</span></span>

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

### <span data-ttu-id="d4e14-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="d4e14-134">-RegenerateKey</span></span>
<span data-ttu-id="d4e14-135">' PrimaryKey '/' SecondaryKey ' 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e14-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e14-136">-ResourceGroupName</span></span>
<span data-ttu-id="d4e14-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4e14-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d4e14-138">-WcfRelay</span></span>
<span data-ttu-id="d4e14-139">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d4e14-140">-확인</span><span class="sxs-lookup"><span data-stu-id="d4e14-140">-Confirm</span></span>
<span data-ttu-id="d4e14-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e14-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e14-142">-WhatIf</span></span>
<span data-ttu-id="d4e14-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e14-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e14-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e14-145">CommonParameters</span></span>
<span data-ttu-id="d4e14-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e14-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e14-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e14-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e14-148">입력</span><span class="sxs-lookup"><span data-stu-id="d4e14-148">INPUTS</span></span>

### <span data-ttu-id="d4e14-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d4e14-149">System.String</span></span>

## <span data-ttu-id="d4e14-150">출력</span><span class="sxs-lookup"><span data-stu-id="d4e14-150">OUTPUTS</span></span>

### <span data-ttu-id="d4e14-151">PSAuthorizationRuleKeysAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="d4e14-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="d4e14-152">상속자</span><span class="sxs-lookup"><span data-stu-id="d4e14-152">NOTES</span></span>

## <span data-ttu-id="d4e14-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4e14-153">RELATED LINKS</span></span>
