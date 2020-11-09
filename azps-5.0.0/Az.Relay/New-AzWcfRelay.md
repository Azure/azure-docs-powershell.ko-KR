---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310010"
---
# <span data-ttu-id="a4008-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="a4008-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="a4008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4008-102">SYNOPSIS</span></span>
<span data-ttu-id="a4008-103">지정 된 릴레이 네임 스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="a4008-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4008-104">SYNTAX</span></span>

### <span data-ttu-id="a4008-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4008-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4008-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a4008-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4008-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a4008-107">DESCRIPTION</span></span>
<span data-ttu-id="a4008-108">New-AzWcfRelay cmdlet은 지정 된 릴레이 네임 스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="a4008-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a4008-109">EXAMPLES</span></span>

### <span data-ttu-id="a4008-110">예제 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4008-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="a4008-111">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-Relay에 새 WcfRelay TestWCFRelay2를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="a4008-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="a4008-112">예제 2-속성</span><span class="sxs-lookup"><span data-stu-id="a4008-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="a4008-113">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-Relay1에 새 WcfRelay TestWCFRelay를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="a4008-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="a4008-114">변수</span><span class="sxs-lookup"><span data-stu-id="a4008-114">PARAMETERS</span></span>

### <span data-ttu-id="a4008-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4008-115">-DefaultProfile</span></span>
<span data-ttu-id="a4008-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4008-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4008-117">-InputObject</span></span>
<span data-ttu-id="a4008-118">WcfRelay 개체</span><span class="sxs-lookup"><span data-stu-id="a4008-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="a4008-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a4008-119">-Name</span></span>
<span data-ttu-id="a4008-120">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="a4008-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4008-121">-Namespace</span></span>
<span data-ttu-id="a4008-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-122">Namespace Name.</span></span>

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

### <span data-ttu-id="a4008-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="a4008-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="a4008-124">이 릴레이에 대해 클라이언트 인증이 필요한 경우 true이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="a4008-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="a4008-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="a4008-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="a4008-126">이 릴레이에 대 한 전송 보안이 필요한 경우 true이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="a4008-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="a4008-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4008-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4008-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4008-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a4008-129">-UserMetadata</span></span>
<span data-ttu-id="a4008-130">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="a4008-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="a4008-131">-WcfRelayType</span></span>
<span data-ttu-id="a4008-132">WcfRelay 유형.</span><span class="sxs-lookup"><span data-stu-id="a4008-132">WcfRelay Type.</span></span>
<span data-ttu-id="a4008-133">사용할 수 있는 값은 다음과 같습니다. ' NetTcp ' 또는 ' Http '</span><span class="sxs-lookup"><span data-stu-id="a4008-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="a4008-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a4008-134">-Confirm</span></span>
<span data-ttu-id="a4008-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4008-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4008-136">-WhatIf</span></span>
<span data-ttu-id="a4008-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4008-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4008-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4008-139">CommonParameters</span></span>
<span data-ttu-id="a4008-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4008-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4008-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4008-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4008-142">입력</span><span class="sxs-lookup"><span data-stu-id="a4008-142">INPUTS</span></span>

### <span data-ttu-id="a4008-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a4008-143">System.String</span></span>

### <span data-ttu-id="a4008-144">PSWcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="a4008-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="a4008-145">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a4008-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a4008-146">출력</span><span class="sxs-lookup"><span data-stu-id="a4008-146">OUTPUTS</span></span>

### <span data-ttu-id="a4008-147">PSWcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="a4008-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="a4008-148">상속자</span><span class="sxs-lookup"><span data-stu-id="a4008-148">NOTES</span></span>

## <span data-ttu-id="a4008-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4008-149">RELATED LINKS</span></span>
