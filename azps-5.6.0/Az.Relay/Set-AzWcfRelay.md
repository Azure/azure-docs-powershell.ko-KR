---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 85c8d65f8a690f9cc977ff069fe6972f5537a114
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000363"
---
# <span data-ttu-id="ed384-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="ed384-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="ed384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed384-102">SYNOPSIS</span></span>
<span data-ttu-id="ed384-103">지정된 릴레이 네임스페이스에서 WcfRelay에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="ed384-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed384-104">SYNTAX</span></span>

### <span data-ttu-id="ed384-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed384-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed384-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ed384-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed384-107">설명</span><span class="sxs-lookup"><span data-stu-id="ed384-107">DESCRIPTION</span></span>
<span data-ttu-id="ed384-108">Set-AzWcfRelay cmdlet은 지정된 릴레이 네임스페이스에서 WcfRelay에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="ed384-109">예제</span><span class="sxs-lookup"><span data-stu-id="ed384-109">EXAMPLES</span></span>

### <span data-ttu-id="ed384-110">예제 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="ed384-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="ed384-111">예제 2 - 속성</span><span class="sxs-lookup"><span data-stu-id="ed384-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="ed384-112">지정된 네임스페이스에서 새 설명으로 지정된 WcfRelay를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="ed384-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="ed384-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed384-114">PARAMETERS</span></span>

### <span data-ttu-id="ed384-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed384-115">-DefaultProfile</span></span>
<span data-ttu-id="ed384-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed384-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed384-117">-InputObject</span></span>
<span data-ttu-id="ed384-118">WcfRelay 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="ed384-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ed384-119">-Name</span></span>
<span data-ttu-id="ed384-120">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="ed384-121">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="ed384-121">-Namespace</span></span>
<span data-ttu-id="ed384-122">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-122">Namespace Name.</span></span>

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

### <span data-ttu-id="ed384-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed384-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed384-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="ed384-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ed384-125">-UserMetadata</span></span>
<span data-ttu-id="ed384-126">사용자 메타데이터를 얻거나 설정하는 것은 WcfRelay 엔드포인트에 대한 사용자 정의 문자열 데이터를 저장하는 자리 표시자입니다. 팀 목록 및 해당 연락처 정보와 같은 설명 데이터를 저장하는 데 사용할 수 있으며 사용자 정의 구성 설정도 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="ed384-127">-확인</span><span class="sxs-lookup"><span data-stu-id="ed384-127">-Confirm</span></span>
<span data-ttu-id="ed384-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed384-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed384-129">-WhatIf</span></span>
<span data-ttu-id="ed384-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed384-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed384-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed384-132">CommonParameters</span></span>
<span data-ttu-id="ed384-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed384-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed384-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed384-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed384-135">입력</span><span class="sxs-lookup"><span data-stu-id="ed384-135">INPUTS</span></span>

### <span data-ttu-id="ed384-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ed384-136">System.String</span></span>

### <span data-ttu-id="ed384-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="ed384-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="ed384-138">출력</span><span class="sxs-lookup"><span data-stu-id="ed384-138">OUTPUTS</span></span>

### <span data-ttu-id="ed384-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="ed384-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="ed384-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed384-140">NOTES</span></span>

## <span data-ttu-id="ed384-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed384-141">RELATED LINKS</span></span>
