---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492419"
---
# <span data-ttu-id="fcffc-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="fcffc-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="fcffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcffc-102">SYNOPSIS</span></span>
<span data-ttu-id="fcffc-103">지정된 Relay 네임스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="fcffc-104">구문</span><span class="sxs-lookup"><span data-stu-id="fcffc-104">SYNTAX</span></span>

### <span data-ttu-id="fcffc-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fcffc-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcffc-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fcffc-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcffc-107">설명</span><span class="sxs-lookup"><span data-stu-id="fcffc-107">DESCRIPTION</span></span>
<span data-ttu-id="fcffc-108">New-AzWcfRelay cmdlet은 지정된 Relay 네임스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="fcffc-109">예제</span><span class="sxs-lookup"><span data-stu-id="fcffc-109">EXAMPLES</span></span>

### <span data-ttu-id="fcffc-110">예제 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="fcffc-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="fcffc-111">지정된 Relay 네임스페이스 \` \` \` TestNameSpace-Relay에 새 WcfRelay TestWCFRelay2를 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="fcffc-112">예제 2 - 속성</span><span class="sxs-lookup"><span data-stu-id="fcffc-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
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

<span data-ttu-id="fcffc-113">지정된 Relay 네임스페이스 \` \` \` TestNameSpace-Relay1에 새 WcfRelay TestWCFRelay를 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="fcffc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcffc-114">PARAMETERS</span></span>

### <span data-ttu-id="fcffc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcffc-115">-DefaultProfile</span></span>
<span data-ttu-id="fcffc-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcffc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcffc-117">-InputObject</span></span>
<span data-ttu-id="fcffc-118">WcfRelay 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="fcffc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fcffc-119">-Name</span></span>
<span data-ttu-id="fcffc-120">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="fcffc-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fcffc-121">-Namespace</span></span>
<span data-ttu-id="fcffc-122">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-122">Namespace Name.</span></span>

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

### <span data-ttu-id="fcffc-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="fcffc-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="fcffc-124">이 릴레이에 클라이언트 권한 부여가 필요한 경우 true입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="fcffc-124">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcffc-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="fcffc-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="fcffc-126">이 릴레이에 전송 보안이 필요한 경우 true입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="fcffc-126">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcffc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcffc-127">-ResourceGroupName</span></span>
<span data-ttu-id="fcffc-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcffc-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="fcffc-129">-UserMetadata</span></span>
<span data-ttu-id="fcffc-130">usermetadata를 얻거나 설정하는 것은 HybridConnection 엔드포인트에 대한 사용자 정의 문자열 데이터를 저장하는 자리 표시자입니다. 예: 팀 목록 및 해당 연락처 정보와 같은 설명이 있는 데이터를 저장하는 데 사용할 수 있으며 사용자 정의 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="fcffc-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="fcffc-131">-WcfRelayType</span></span>
<span data-ttu-id="fcffc-132">WcfRelay 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-132">WcfRelay Type.</span></span>
<span data-ttu-id="fcffc-133">가능한 값은 'NetTcp' 또는 'Http'입니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-133">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcffc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcffc-134">-Confirm</span></span>
<span data-ttu-id="fcffc-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcffc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcffc-136">-WhatIf</span></span>
<span data-ttu-id="fcffc-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fcffc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcffc-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcffc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcffc-139">CommonParameters</span></span>
<span data-ttu-id="fcffc-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fcffc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcffc-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fcffc-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcffc-142">입력</span><span class="sxs-lookup"><span data-stu-id="fcffc-142">INPUTS</span></span>

### <span data-ttu-id="fcffc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fcffc-143">System.String</span></span>

### <span data-ttu-id="fcffc-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="fcffc-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="fcffc-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fcffc-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fcffc-146">출력</span><span class="sxs-lookup"><span data-stu-id="fcffc-146">OUTPUTS</span></span>

### <span data-ttu-id="fcffc-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="fcffc-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="fcffc-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fcffc-148">NOTES</span></span>

## <span data-ttu-id="fcffc-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcffc-149">RELATED LINKS</span></span>
