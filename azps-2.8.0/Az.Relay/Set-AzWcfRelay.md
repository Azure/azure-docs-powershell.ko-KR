---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 04925f904861eea006c6480dbdb48794afc55c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873421"
---
# <span data-ttu-id="40123-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="40123-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="40123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40123-102">SYNOPSIS</span></span>
<span data-ttu-id="40123-103">지정 된 릴레이 네임 스페이스의 WcfRelay에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40123-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="40123-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40123-104">SYNTAX</span></span>

### <span data-ttu-id="40123-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40123-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40123-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="40123-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40123-107">설명은</span><span class="sxs-lookup"><span data-stu-id="40123-107">DESCRIPTION</span></span>
<span data-ttu-id="40123-108">Set-AzWcfRelay cmdlet은 지정 된 릴레이 네임 스페이스의 WcfRelay에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40123-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="40123-109">예제의</span><span class="sxs-lookup"><span data-stu-id="40123-109">EXAMPLES</span></span>

### <span data-ttu-id="40123-110">예제 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="40123-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="40123-111">예제 2-속성</span><span class="sxs-lookup"><span data-stu-id="40123-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="40123-112">지정 된 WcfRelay를 지정 된 네임 스페이스의 새 설명으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40123-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="40123-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40123-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="40123-114">변수</span><span class="sxs-lookup"><span data-stu-id="40123-114">PARAMETERS</span></span>

### <span data-ttu-id="40123-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40123-115">-DefaultProfile</span></span>
<span data-ttu-id="40123-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40123-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40123-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40123-117">-InputObject</span></span>
<span data-ttu-id="40123-118">WcfRelay 개체</span><span class="sxs-lookup"><span data-stu-id="40123-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="40123-119">-이름</span><span class="sxs-lookup"><span data-stu-id="40123-119">-Name</span></span>
<span data-ttu-id="40123-120">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40123-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="40123-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40123-121">-Namespace</span></span>
<span data-ttu-id="40123-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40123-122">Namespace Name.</span></span>

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

### <span data-ttu-id="40123-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40123-123">-ResourceGroupName</span></span>
<span data-ttu-id="40123-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40123-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="40123-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="40123-125">-UserMetadata</span></span>
<span data-ttu-id="40123-126">Usermetadata 가져오거나 설정 WcfRelay 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40123-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="40123-127">-확인</span><span class="sxs-lookup"><span data-stu-id="40123-127">-Confirm</span></span>
<span data-ttu-id="40123-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40123-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40123-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40123-129">-WhatIf</span></span>
<span data-ttu-id="40123-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40123-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40123-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40123-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40123-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40123-132">CommonParameters</span></span>
<span data-ttu-id="40123-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40123-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40123-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40123-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40123-135">입력</span><span class="sxs-lookup"><span data-stu-id="40123-135">INPUTS</span></span>

### <span data-ttu-id="40123-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40123-136">System.String</span></span>

### <span data-ttu-id="40123-137">PSWcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="40123-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="40123-138">출력</span><span class="sxs-lookup"><span data-stu-id="40123-138">OUTPUTS</span></span>

### <span data-ttu-id="40123-139">PSWcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="40123-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="40123-140">상속자</span><span class="sxs-lookup"><span data-stu-id="40123-140">NOTES</span></span>

## <span data-ttu-id="40123-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40123-141">RELATED LINKS</span></span>
