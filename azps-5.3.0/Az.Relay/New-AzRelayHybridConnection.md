---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491677"
---
# <span data-ttu-id="8d868-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="8d868-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="8d868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d868-102">SYNOPSIS</span></span>
<span data-ttu-id="8d868-103">지정된 Relay 네임스페이스에 HybridConnection을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="8d868-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d868-104">SYNTAX</span></span>

### <span data-ttu-id="8d868-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8d868-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d868-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8d868-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d868-107">설명</span><span class="sxs-lookup"><span data-stu-id="8d868-107">DESCRIPTION</span></span>
<span data-ttu-id="8d868-108">New-AzRelayHybridConnection cmdlet은 지정된 Relay 네임스페이스에 HybridConnection을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="8d868-109">예제</span><span class="sxs-lookup"><span data-stu-id="8d868-109">EXAMPLES</span></span>

### <span data-ttu-id="8d868-110">예제 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="8d868-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="8d868-111">지정된 Relay 네임스페이스 \` \` \` TestNameSpace-HybirdConnection에 새 HybirdConnection TestHybirdConnection2를 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="8d868-112">예제 2 - 속성</span><span class="sxs-lookup"><span data-stu-id="8d868-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="8d868-113">지정된 Relay 네임스페이스 \` \` \` TestNameSpace-HybirdConnection에 새 HybirdConnection TestHybirdConnection1을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="8d868-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d868-114">PARAMETERS</span></span>

### <span data-ttu-id="8d868-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d868-115">-DefaultProfile</span></span>
<span data-ttu-id="8d868-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d868-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d868-117">-InputObject</span></span>
<span data-ttu-id="8d868-118">HybridConnections 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d868-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8d868-119">-Name</span></span>
<span data-ttu-id="8d868-120">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="8d868-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8d868-121">-Namespace</span></span>
<span data-ttu-id="8d868-122">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-122">Namespace Name.</span></span>

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

### <span data-ttu-id="8d868-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="8d868-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="8d868-124">이 HybridConnections에 클라이언트 권한 부여가 필요한 경우 true입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="8d868-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d868-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d868-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d868-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="8d868-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8d868-127">-UserMetadata</span></span>
<span data-ttu-id="8d868-128">usermetadata를 얻거나 설정하는 것은 HybridConnection 엔드포인트에 대한 사용자 정의 문자열 데이터를 저장하는 자리 표시자입니다. 예: 팀 목록 및 해당 연락처 정보와 같은 설명이 있는 데이터를 저장하는 데 사용할 수 있으며 사용자 정의 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="8d868-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d868-129">-Confirm</span></span>
<span data-ttu-id="8d868-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d868-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d868-131">-WhatIf</span></span>
<span data-ttu-id="8d868-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8d868-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d868-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d868-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d868-134">CommonParameters</span></span>
<span data-ttu-id="8d868-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d868-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d868-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8d868-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d868-137">입력</span><span class="sxs-lookup"><span data-stu-id="8d868-137">INPUTS</span></span>

### <span data-ttu-id="8d868-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8d868-138">System.String</span></span>

### <span data-ttu-id="8d868-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="8d868-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="8d868-140">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d868-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8d868-141">출력</span><span class="sxs-lookup"><span data-stu-id="8d868-141">OUTPUTS</span></span>

### <span data-ttu-id="8d868-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="8d868-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="8d868-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d868-143">NOTES</span></span>

## <span data-ttu-id="8d868-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d868-144">RELATED LINKS</span></span>
