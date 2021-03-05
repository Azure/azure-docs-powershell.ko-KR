---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 10fc65f492c76a3b240bd2287b080d56bb20836e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000411"
---
# <span data-ttu-id="44225-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="44225-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="44225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44225-102">SYNOPSIS</span></span>
<span data-ttu-id="44225-103">지정된 릴레이 네임스페이스에서 HybridConnection에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="44225-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="44225-104">구문</span><span class="sxs-lookup"><span data-stu-id="44225-104">SYNTAX</span></span>

### <span data-ttu-id="44225-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44225-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44225-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="44225-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44225-107">설명</span><span class="sxs-lookup"><span data-stu-id="44225-107">DESCRIPTION</span></span>
<span data-ttu-id="44225-108">Set-AzRelayHybridConnection cmdlet은 지정된 릴레이 네임스페이스에서 HybridConnection에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="44225-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="44225-109">예제</span><span class="sxs-lookup"><span data-stu-id="44225-109">EXAMPLES</span></span>

### <span data-ttu-id="44225-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="44225-110">Example 1</span></span>
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

### <span data-ttu-id="44225-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="44225-111">Example 2</span></span>
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

<span data-ttu-id="44225-112">지정된 네임스페이스에서 새 설명으로 지정된 HybridConnection을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="44225-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="44225-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="44225-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="44225-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="44225-114">PARAMETERS</span></span>

### <span data-ttu-id="44225-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44225-115">-DefaultProfile</span></span>
<span data-ttu-id="44225-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44225-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44225-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44225-117">-InputObject</span></span>
<span data-ttu-id="44225-118">HybridConnections 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="44225-118">HybridConnections object.</span></span>

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

### <span data-ttu-id="44225-119">-Name</span><span class="sxs-lookup"><span data-stu-id="44225-119">-Name</span></span>
<span data-ttu-id="44225-120">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44225-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="44225-121">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="44225-121">-Namespace</span></span>
<span data-ttu-id="44225-122">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44225-122">Namespace Name.</span></span>

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

### <span data-ttu-id="44225-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44225-123">-ResourceGroupName</span></span>
<span data-ttu-id="44225-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44225-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="44225-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="44225-125">-UserMetadata</span></span>
<span data-ttu-id="44225-126">사용자 메타데이터를 얻거나 설정하는 것은 HybridConnection 엔드포인트에 대한 사용자 정의 문자열 데이터를 저장하는 자리 표시자입니다. 팀 목록 및 해당 연락처 정보와 같은 설명 데이터를 저장하는 데 사용할 수 있으며 사용자 정의 구성 설정도 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44225-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="44225-127">-확인</span><span class="sxs-lookup"><span data-stu-id="44225-127">-Confirm</span></span>
<span data-ttu-id="44225-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44225-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44225-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44225-129">-WhatIf</span></span>
<span data-ttu-id="44225-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="44225-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44225-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44225-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44225-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44225-132">CommonParameters</span></span>
<span data-ttu-id="44225-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44225-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44225-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="44225-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44225-135">입력</span><span class="sxs-lookup"><span data-stu-id="44225-135">INPUTS</span></span>

### <span data-ttu-id="44225-136">System.String</span><span class="sxs-lookup"><span data-stu-id="44225-136">System.String</span></span>

### <span data-ttu-id="44225-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="44225-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="44225-138">출력</span><span class="sxs-lookup"><span data-stu-id="44225-138">OUTPUTS</span></span>

### <span data-ttu-id="44225-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="44225-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="44225-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44225-140">NOTES</span></span>

## <span data-ttu-id="44225-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44225-141">RELATED LINKS</span></span>
