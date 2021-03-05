---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 837c6e69f2b01ec0ae8de8ed7a711a041096dd2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000475"
---
# <span data-ttu-id="8e8cf-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="8e8cf-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="8e8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8cf-103">지정된 릴레이 네임스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="8e8cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e8cf-104">SYNTAX</span></span>

### <span data-ttu-id="8e8cf-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e8cf-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e8cf-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8e8cf-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8cf-107">설명</span><span class="sxs-lookup"><span data-stu-id="8e8cf-107">DESCRIPTION</span></span>
<span data-ttu-id="8e8cf-108">New-AzWcfRelay cmdlet은 지정된 릴레이 네임스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="8e8cf-109">예제</span><span class="sxs-lookup"><span data-stu-id="8e8cf-109">EXAMPLES</span></span>

### <span data-ttu-id="8e8cf-110">예제 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="8e8cf-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="8e8cf-111">지정된 릴레이 네임스페이스 \` \` \` TestNameSpace-Relay에서 새 WcfRelay TestWCFRelay2를 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="8e8cf-112">예제 2 - 속성</span><span class="sxs-lookup"><span data-stu-id="8e8cf-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="8e8cf-113">지정된 릴레이 네임스페이스 \` \` \` TestNameSpace-Relay1에서 새 WcfRelay TestWCFRelay를 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="8e8cf-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e8cf-114">PARAMETERS</span></span>

### <span data-ttu-id="8e8cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8cf-115">-DefaultProfile</span></span>
<span data-ttu-id="8e8cf-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e8cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e8cf-117">-InputObject</span></span>
<span data-ttu-id="8e8cf-118">WcfRelay 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="8e8cf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e8cf-119">-Name</span></span>
<span data-ttu-id="8e8cf-120">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8e8cf-121">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="8e8cf-121">-Namespace</span></span>
<span data-ttu-id="8e8cf-122">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-122">Namespace Name.</span></span>

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

### <span data-ttu-id="8e8cf-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="8e8cf-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="8e8cf-124">이 릴레이에 클라이언트 권한 부여가 필요한 경우 true입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="8e8cf-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="8e8cf-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="8e8cf-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="8e8cf-126">이 릴레이에 전송 보안이 필요한 경우 true입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="8e8cf-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="8e8cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e8cf-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e8cf-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8e8cf-129">-UserMetadata</span></span>
<span data-ttu-id="8e8cf-130">사용자 메타데이터를 얻거나 설정하는 것은 HybridConnection 엔드포인트에 대한 사용자 정의 문자열 데이터를 저장하는 자리 표시자입니다. 팀 목록 및 해당 연락처 정보와 같은 설명 데이터를 저장하는 데 사용할 수 있으며 사용자 정의 구성 설정도 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="8e8cf-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="8e8cf-131">-WcfRelayType</span></span>
<span data-ttu-id="8e8cf-132">WcfRelay 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-132">WcfRelay Type.</span></span>
<span data-ttu-id="8e8cf-133">가능한 값은 다음과 같습니다. 'NetTcp' 또는 'Http'</span><span class="sxs-lookup"><span data-stu-id="8e8cf-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="8e8cf-134">-확인</span><span class="sxs-lookup"><span data-stu-id="8e8cf-134">-Confirm</span></span>
<span data-ttu-id="8e8cf-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e8cf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8cf-136">-WhatIf</span></span>
<span data-ttu-id="8e8cf-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e8cf-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e8cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8cf-139">CommonParameters</span></span>
<span data-ttu-id="8e8cf-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8cf-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e8cf-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8cf-142">입력</span><span class="sxs-lookup"><span data-stu-id="8e8cf-142">INPUTS</span></span>

### <span data-ttu-id="8e8cf-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8e8cf-143">System.String</span></span>

### <span data-ttu-id="8e8cf-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="8e8cf-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="8e8cf-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e8cf-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8e8cf-146">출력</span><span class="sxs-lookup"><span data-stu-id="8e8cf-146">OUTPUTS</span></span>

### <span data-ttu-id="8e8cf-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="8e8cf-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="8e8cf-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e8cf-148">NOTES</span></span>

## <span data-ttu-id="8e8cf-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e8cf-149">RELATED LINKS</span></span>
