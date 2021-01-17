---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378134"
---
# <span data-ttu-id="f4d32-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="f4d32-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="f4d32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d32-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d32-103">주어진 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대한 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f4d32-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4d32-104">SYNTAX</span></span>

### <span data-ttu-id="f4d32-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f4d32-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4d32-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4d32-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4d32-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4d32-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d32-108">설명</span><span class="sxs-lookup"><span data-stu-id="f4d32-108">DESCRIPTION</span></span>
<span data-ttu-id="f4d32-109">**Get-AzRelayKey** cmdlet은 주어진 Relay 엔터티(Namespace/WcfRelay/HybridConnection)에 대한 기본 및 보조 연결 문자열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f4d32-110">예제</span><span class="sxs-lookup"><span data-stu-id="f4d32-110">EXAMPLES</span></span>

### <span data-ttu-id="f4d32-111">예제 1: 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="f4d32-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="f4d32-112">예제 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f4d32-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="f4d32-113">예제 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f4d32-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="f4d32-114">지정된 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f4d32-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4d32-115">PARAMETERS</span></span>

### <span data-ttu-id="f4d32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d32-116">-DefaultProfile</span></span>
<span data-ttu-id="f4d32-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d32-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f4d32-118">-HybridConnection</span></span>
<span data-ttu-id="f4d32-119">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f4d32-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f4d32-120">-Name</span></span>
<span data-ttu-id="f4d32-121">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f4d32-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4d32-122">-Namespace</span></span>
<span data-ttu-id="f4d32-123">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-123">Namespace Name.</span></span>

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

### <span data-ttu-id="f4d32-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d32-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4d32-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f4d32-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f4d32-126">-WcfRelay</span></span>
<span data-ttu-id="f4d32-127">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f4d32-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d32-128">CommonParameters</span></span>
<span data-ttu-id="f4d32-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d32-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d32-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f4d32-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d32-131">입력</span><span class="sxs-lookup"><span data-stu-id="f4d32-131">INPUTS</span></span>

### <span data-ttu-id="f4d32-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f4d32-132">System.String</span></span>

## <span data-ttu-id="f4d32-133">출력</span><span class="sxs-lookup"><span data-stu-id="f4d32-133">OUTPUTS</span></span>

### <span data-ttu-id="f4d32-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f4d32-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="f4d32-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4d32-135">NOTES</span></span>

## <span data-ttu-id="f4d32-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4d32-136">RELATED LINKS</span></span>
