---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378106"
---
# <span data-ttu-id="9136f-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="9136f-101">New-AzRelayKey</span></span>

## <span data-ttu-id="9136f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9136f-102">SYNOPSIS</span></span>
<span data-ttu-id="9136f-103">주어진 Relay 엔터티에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다(네임스페이스/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="9136f-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="9136f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9136f-104">SYNTAX</span></span>

### <span data-ttu-id="9136f-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9136f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9136f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9136f-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9136f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9136f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9136f-108">설명</span><span class="sxs-lookup"><span data-stu-id="9136f-108">DESCRIPTION</span></span>
<span data-ttu-id="9136f-109">**New-AzRelayKey** cmdlet은 주어진 Relay 엔터티(Namespace/WcfRelay/HybridConnection)에 대한 기본 및 보조 연결 문자열을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9136f-110">예제</span><span class="sxs-lookup"><span data-stu-id="9136f-110">EXAMPLES</span></span>

### <span data-ttu-id="9136f-111">예제 1 - 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="9136f-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="9136f-112">주어진 Relay-Namespace 엔터티에 대한 기본 또는 보조 연결 문자열을 Relay-Namespace 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="9136f-113">예제 1.1 - 네임스페이스 KeyValue 제공</span><span class="sxs-lookup"><span data-stu-id="9136f-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="9136f-114">제공된 키 값을 사용하여 제공된 Relay-Namespace 엔터티에 대한 기본 또는 보조 연결 문자열을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="9136f-115">예제 2 - WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9136f-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="9136f-116">주어진 Relay-WcfRelay 엔터티에 대한 기본 또는 보조 연결 문자열을 Relay-WcfRelay 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="9136f-117">예제 2.1 - 제공된 WcfRelay KeyValue</span><span class="sxs-lookup"><span data-stu-id="9136f-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="9136f-118">제공된 키 값을 사용하여 제공된 Relay-WcfRelay 엔터티에 대한 기본 또는 보조 연결 문자열을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="9136f-119">예제 3 - HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9136f-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="9136f-120">주어진 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="9136f-121">예제 3.1 - HybridConnection KeyValue 제공</span><span class="sxs-lookup"><span data-stu-id="9136f-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="9136f-122">제공된 키 값을 사용하여 제공된 Relay-HybridConnection 엔터티에 대한 기본 또는 보조 연결 문자열을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="9136f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9136f-123">PARAMETERS</span></span>

### <span data-ttu-id="9136f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9136f-124">-DefaultProfile</span></span>
<span data-ttu-id="9136f-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9136f-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9136f-126">-HybridConnection</span></span>
<span data-ttu-id="9136f-127">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="9136f-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="9136f-128">-KeyValue</span></span>
<span data-ttu-id="9136f-129">SAS 토큰 서명 및 유효성을 검사하기 위한 base64로 인코딩된 256비트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="9136f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9136f-130">-Name</span></span>
<span data-ttu-id="9136f-131">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9136f-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9136f-132">-Namespace</span></span>
<span data-ttu-id="9136f-133">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-133">Namespace Name.</span></span>

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

### <span data-ttu-id="9136f-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="9136f-134">-RegenerateKey</span></span>
<span data-ttu-id="9136f-135">키 다시 생성 - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="9136f-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="9136f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9136f-136">-ResourceGroupName</span></span>
<span data-ttu-id="9136f-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="9136f-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9136f-138">-WcfRelay</span></span>
<span data-ttu-id="9136f-139">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9136f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9136f-140">-Confirm</span></span>
<span data-ttu-id="9136f-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9136f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9136f-142">-WhatIf</span></span>
<span data-ttu-id="9136f-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9136f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9136f-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9136f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9136f-145">CommonParameters</span></span>
<span data-ttu-id="9136f-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9136f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9136f-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9136f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9136f-148">입력</span><span class="sxs-lookup"><span data-stu-id="9136f-148">INPUTS</span></span>

### <span data-ttu-id="9136f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9136f-149">System.String</span></span>

## <span data-ttu-id="9136f-150">출력</span><span class="sxs-lookup"><span data-stu-id="9136f-150">OUTPUTS</span></span>

### <span data-ttu-id="9136f-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="9136f-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="9136f-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9136f-152">NOTES</span></span>

## <span data-ttu-id="9136f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9136f-153">RELATED LINKS</span></span>
