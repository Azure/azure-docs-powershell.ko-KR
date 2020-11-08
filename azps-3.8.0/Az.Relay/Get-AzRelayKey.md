---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 4434802f1025e24bb249ee503ed2267e9187a2c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879126"
---
# <span data-ttu-id="710c4-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="710c4-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="710c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="710c4-102">SYNOPSIS</span></span>
<span data-ttu-id="710c4-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="710c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="710c4-104">SYNTAX</span></span>

### <span data-ttu-id="710c4-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="710c4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="710c4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="710c4-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="710c4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="710c4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="710c4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="710c4-108">DESCRIPTION</span></span>
<span data-ttu-id="710c4-109">**AzRelayKey** cmdlet은 지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="710c4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="710c4-110">EXAMPLES</span></span>

### <span data-ttu-id="710c4-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="710c4-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="710c4-112">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="710c4-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="710c4-113">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="710c4-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="710c4-114">지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="710c4-115">변수</span><span class="sxs-lookup"><span data-stu-id="710c4-115">PARAMETERS</span></span>

### <span data-ttu-id="710c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710c4-116">-DefaultProfile</span></span>
<span data-ttu-id="710c4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="710c4-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="710c4-118">-HybridConnection</span></span>
<span data-ttu-id="710c4-119">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="710c4-120">-이름</span><span class="sxs-lookup"><span data-stu-id="710c4-120">-Name</span></span>
<span data-ttu-id="710c4-121">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="710c4-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="710c4-122">-Namespace</span></span>
<span data-ttu-id="710c4-123">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-123">Namespace Name.</span></span>

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

### <span data-ttu-id="710c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="710c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="710c4-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="710c4-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="710c4-126">-WcfRelay</span></span>
<span data-ttu-id="710c4-127">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="710c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710c4-128">CommonParameters</span></span>
<span data-ttu-id="710c4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="710c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710c4-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="710c4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710c4-131">입력</span><span class="sxs-lookup"><span data-stu-id="710c4-131">INPUTS</span></span>

### <span data-ttu-id="710c4-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="710c4-132">System.String</span></span>

## <span data-ttu-id="710c4-133">출력</span><span class="sxs-lookup"><span data-stu-id="710c4-133">OUTPUTS</span></span>

### <span data-ttu-id="710c4-134">PSAuthorizationRuleKeysAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="710c4-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="710c4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="710c4-135">NOTES</span></span>

## <span data-ttu-id="710c4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="710c4-136">RELATED LINKS</span></span>