---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: f7671d35901705ef96f6c1bf13c487c688a6214c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370189"
---
# <span data-ttu-id="e2ae2-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="e2ae2-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="e2ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ae2-103">지정된 Relay 네임스페이스에서 WcfRelay에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="e2ae2-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2ae2-104">SYNTAX</span></span>

### <span data-ttu-id="e2ae2-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2ae2-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2ae2-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e2ae2-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ae2-107">설명</span><span class="sxs-lookup"><span data-stu-id="e2ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="e2ae2-108">이 Set-AzWcfRelay cmdlet은 지정된 Relay 네임스페이스에서 WcfRelay에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="e2ae2-109">예제</span><span class="sxs-lookup"><span data-stu-id="e2ae2-109">EXAMPLES</span></span>

### <span data-ttu-id="e2ae2-110">예제 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ae2-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="e2ae2-111">예제 2 - 속성</span><span class="sxs-lookup"><span data-stu-id="e2ae2-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="e2ae2-112">지정된 WcfRelay를 지정된 네임스페이스의 새 설명으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="e2ae2-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="e2ae2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2ae2-114">PARAMETERS</span></span>

### <span data-ttu-id="e2ae2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ae2-115">-DefaultProfile</span></span>
<span data-ttu-id="e2ae2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ae2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ae2-117">-InputObject</span></span>
<span data-ttu-id="e2ae2-118">WcfRelay 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e2ae2-119">-Name</span></span>
<span data-ttu-id="e2ae2-120">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-120">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2ae2-121">-Namespace</span></span>
<span data-ttu-id="e2ae2-122">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-122">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ae2-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2ae2-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2ae2-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e2ae2-125">-UserMetadata</span></span>
<span data-ttu-id="e2ae2-126">사용자 메타데이터를 얻거나 설정하는 것은 WcfRelay 엔드포인트에 대한 사용자 정의 문자열 데이터를 저장하는 자리 표시자입니다. 예: 팀 목록 및 해당 연락처 정보와 같은 설명이 있는 데이터를 저장하는 데 사용할 수 있으며 사용자 정의 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2ae2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2ae2-127">-Confirm</span></span>
<span data-ttu-id="e2ae2-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ae2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ae2-129">-WhatIf</span></span>
<span data-ttu-id="e2ae2-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e2ae2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ae2-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ae2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ae2-132">CommonParameters</span></span>
<span data-ttu-id="e2ae2-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ae2-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2ae2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ae2-135">입력</span><span class="sxs-lookup"><span data-stu-id="e2ae2-135">INPUTS</span></span>

### <span data-ttu-id="e2ae2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e2ae2-136">System.String</span></span>

### <span data-ttu-id="e2ae2-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="e2ae2-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="e2ae2-138">출력</span><span class="sxs-lookup"><span data-stu-id="e2ae2-138">OUTPUTS</span></span>

### <span data-ttu-id="e2ae2-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="e2ae2-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="e2ae2-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2ae2-140">NOTES</span></span>

## <span data-ttu-id="e2ae2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2ae2-141">RELATED LINKS</span></span>
