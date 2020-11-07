---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 9f0145cee1facbd409406b86b2a6fc15f034737a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699506"
---
# <span data-ttu-id="67108-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="67108-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="67108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67108-102">SYNOPSIS</span></span>
<span data-ttu-id="67108-103">지정 된 릴레이 네임 스페이스에 HybridConnection를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67108-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="67108-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67108-104">SYNTAX</span></span>

### <span data-ttu-id="67108-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67108-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67108-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="67108-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67108-107">설명은</span><span class="sxs-lookup"><span data-stu-id="67108-107">DESCRIPTION</span></span>
<span data-ttu-id="67108-108">New-AzRelayHybridConnection cmdlet은 지정 된 릴레이 네임 스페이스에 HybridConnection를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67108-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="67108-109">예제의</span><span class="sxs-lookup"><span data-stu-id="67108-109">EXAMPLES</span></span>

### <span data-ttu-id="67108-110">예제 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="67108-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="67108-111">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-HybirdConnection에 새 HybirdConnection TestHybirdConnection2를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="67108-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="67108-112">예제 2-속성</span><span class="sxs-lookup"><span data-stu-id="67108-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="67108-113">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-HybirdConnection에 새 HybirdConnection TestHybirdConnection1를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="67108-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="67108-114">변수</span><span class="sxs-lookup"><span data-stu-id="67108-114">PARAMETERS</span></span>

### <span data-ttu-id="67108-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67108-115">-DefaultProfile</span></span>
<span data-ttu-id="67108-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67108-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67108-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67108-117">-InputObject</span></span>
<span data-ttu-id="67108-118">HybridConnections 개체</span><span class="sxs-lookup"><span data-stu-id="67108-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67108-119">-이름</span><span class="sxs-lookup"><span data-stu-id="67108-119">-Name</span></span>
<span data-ttu-id="67108-120">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67108-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="67108-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67108-121">-Namespace</span></span>
<span data-ttu-id="67108-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67108-122">Namespace Name.</span></span>

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

### <span data-ttu-id="67108-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="67108-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="67108-124">이 HybridConnections에 대해 클라이언트 인증이 필요한 경우 true이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="67108-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="67108-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67108-125">-ResourceGroupName</span></span>
<span data-ttu-id="67108-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67108-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="67108-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="67108-127">-UserMetadata</span></span>
<span data-ttu-id="67108-128">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67108-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="67108-129">-확인</span><span class="sxs-lookup"><span data-stu-id="67108-129">-Confirm</span></span>
<span data-ttu-id="67108-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67108-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67108-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67108-131">-WhatIf</span></span>
<span data-ttu-id="67108-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67108-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67108-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67108-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67108-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67108-134">CommonParameters</span></span>
<span data-ttu-id="67108-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67108-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67108-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67108-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67108-137">입력</span><span class="sxs-lookup"><span data-stu-id="67108-137">INPUTS</span></span>

### <span data-ttu-id="67108-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67108-138">System.String</span></span>

### <span data-ttu-id="67108-139">PSHybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="67108-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

### <span data-ttu-id="67108-140">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="67108-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="67108-141">출력</span><span class="sxs-lookup"><span data-stu-id="67108-141">OUTPUTS</span></span>

### <span data-ttu-id="67108-142">PSHybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="67108-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

## <span data-ttu-id="67108-143">상속자</span><span class="sxs-lookup"><span data-stu-id="67108-143">NOTES</span></span>

## <span data-ttu-id="67108-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67108-144">RELATED LINKS</span></span>