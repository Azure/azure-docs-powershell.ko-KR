---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 2b029b2a93a063a322c11ea84cd46b787acc9960
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491667"
---
# <span data-ttu-id="d0070-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="d0070-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="d0070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0070-102">SYNOPSIS</span></span>
<span data-ttu-id="d0070-103">지정된 Relay 네임스페이스에서 HybridConnection에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="d0070-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0070-104">SYNTAX</span></span>

### <span data-ttu-id="d0070-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0070-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0070-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d0070-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0070-107">설명</span><span class="sxs-lookup"><span data-stu-id="d0070-107">DESCRIPTION</span></span>
<span data-ttu-id="d0070-108">이 Set-AzRelayHybridConnection cmdlet은 지정된 Relay 네임스페이스에서 HybridConnection에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="d0070-109">예제</span><span class="sxs-lookup"><span data-stu-id="d0070-109">EXAMPLES</span></span>

### <span data-ttu-id="d0070-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0070-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="d0070-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0070-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="d0070-112">지정된 HybridConnection을 지정된 네임스페이스의 새 설명으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="d0070-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="d0070-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0070-114">PARAMETERS</span></span>

### <span data-ttu-id="d0070-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0070-115">-DefaultProfile</span></span>
<span data-ttu-id="d0070-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0070-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0070-117">-InputObject</span></span>
<span data-ttu-id="d0070-118">HybridConnections 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0070-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d0070-119">-Name</span></span>
<span data-ttu-id="d0070-120">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="d0070-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0070-121">-Namespace</span></span>
<span data-ttu-id="d0070-122">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-122">Namespace Name.</span></span>

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

### <span data-ttu-id="d0070-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0070-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0070-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0070-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d0070-125">-UserMetadata</span></span>
<span data-ttu-id="d0070-126">usermetadata를 얻거나 설정하는 것은 HybridConnection 엔드포인트에 대한 사용자 정의 문자열 데이터를 저장하는 자리 표시자입니다. 예: 팀 목록 및 해당 연락처 정보와 같은 설명이 있는 데이터를 저장하는 데 사용할 수 있으며 사용자 정의 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0070-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0070-127">-Confirm</span></span>
<span data-ttu-id="d0070-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0070-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0070-129">-WhatIf</span></span>
<span data-ttu-id="d0070-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d0070-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0070-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0070-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0070-132">CommonParameters</span></span>
<span data-ttu-id="d0070-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0070-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0070-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d0070-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0070-135">입력</span><span class="sxs-lookup"><span data-stu-id="d0070-135">INPUTS</span></span>

### <span data-ttu-id="d0070-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d0070-136">System.String</span></span>

### <span data-ttu-id="d0070-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="d0070-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="d0070-138">출력</span><span class="sxs-lookup"><span data-stu-id="d0070-138">OUTPUTS</span></span>

### <span data-ttu-id="d0070-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="d0070-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="d0070-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0070-140">NOTES</span></span>

## <span data-ttu-id="d0070-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0070-141">RELATED LINKS</span></span>
