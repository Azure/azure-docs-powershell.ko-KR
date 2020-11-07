---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 68ba115bb74bf0eae780944037532b0d37424704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699521"
---
# <span data-ttu-id="2f1d7-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="2f1d7-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="2f1d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f1d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1d7-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2f1d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f1d7-104">SYNTAX</span></span>

### <span data-ttu-id="2f1d7-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2f1d7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f1d7-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f1d7-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f1d7-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f1d7-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f1d7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2f1d7-108">DESCRIPTION</span></span>
<span data-ttu-id="2f1d7-109">**AzRelayKey** cmdlet은 지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2f1d7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2f1d7-110">EXAMPLES</span></span>

### <span data-ttu-id="2f1d7-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="2f1d7-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="2f1d7-112">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2f1d7-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="2f1d7-113">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2f1d7-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="2f1d7-114">지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2f1d7-115">변수</span><span class="sxs-lookup"><span data-stu-id="2f1d7-115">PARAMETERS</span></span>

### <span data-ttu-id="2f1d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1d7-116">-DefaultProfile</span></span>
<span data-ttu-id="2f1d7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f1d7-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2f1d7-118">-HybridConnection</span></span>
<span data-ttu-id="2f1d7-119">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2f1d7-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2f1d7-120">-Name</span></span>
<span data-ttu-id="2f1d7-121">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2f1d7-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f1d7-122">-Namespace</span></span>
<span data-ttu-id="2f1d7-123">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-123">Namespace Name.</span></span>

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

### <span data-ttu-id="2f1d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f1d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f1d7-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2f1d7-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2f1d7-126">-WcfRelay</span></span>
<span data-ttu-id="2f1d7-127">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2f1d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1d7-128">CommonParameters</span></span>
<span data-ttu-id="2f1d7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1d7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1d7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1d7-131">입력</span><span class="sxs-lookup"><span data-stu-id="2f1d7-131">INPUTS</span></span>

### <span data-ttu-id="2f1d7-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2f1d7-132">System.String</span></span>

## <span data-ttu-id="2f1d7-133">출력</span><span class="sxs-lookup"><span data-stu-id="2f1d7-133">OUTPUTS</span></span>

### <span data-ttu-id="2f1d7-134">PSAuthorizationRuleKeysAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="2f1d7-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="2f1d7-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2f1d7-135">NOTES</span></span>

## <span data-ttu-id="2f1d7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f1d7-136">RELATED LINKS</span></span>