---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: 3aa57c1ec70d560a0fee395b27d79372bdf4fd61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526071"
---
# <span data-ttu-id="e40cf-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="e40cf-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="e40cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e40cf-102">SYNOPSIS</span></span>
<span data-ttu-id="e40cf-103">지정 된 릴레이 네임 스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e40cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e40cf-104">SYNTAX</span></span>

### <span data-ttu-id="e40cf-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e40cf-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e40cf-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e40cf-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e40cf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e40cf-107">DESCRIPTION</span></span>
<span data-ttu-id="e40cf-108">New-AzureRmWcfRelay cmdlet은 지정 된 릴레이 네임 스페이스에 WcfRelay를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="e40cf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e40cf-109">EXAMPLES</span></span>

### <span data-ttu-id="e40cf-110">예제 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="e40cf-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

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

<span data-ttu-id="e40cf-111">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-Relay에 새 WcfRelay TestWCFRelay2를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="e40cf-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="e40cf-112">예제 2-속성</span><span class="sxs-lookup"><span data-stu-id="e40cf-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

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

<span data-ttu-id="e40cf-113">\` \` 지정 된 릴레이 네임 스페이스 \` Testnamespace-Relay1에 새 WcfRelay TestWCFRelay를 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="e40cf-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="e40cf-114">변수</span><span class="sxs-lookup"><span data-stu-id="e40cf-114">PARAMETERS</span></span>

### <span data-ttu-id="e40cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e40cf-115">-DefaultProfile</span></span>
<span data-ttu-id="e40cf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e40cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e40cf-117">-InputObject</span></span>
<span data-ttu-id="e40cf-118">WcfRelay 개체</span><span class="sxs-lookup"><span data-stu-id="e40cf-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="e40cf-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e40cf-119">-Name</span></span>
<span data-ttu-id="e40cf-120">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e40cf-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e40cf-121">-Namespace</span></span>
<span data-ttu-id="e40cf-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-122">Namespace Name.</span></span>

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

### <span data-ttu-id="e40cf-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="e40cf-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="e40cf-124">이 릴레이에 대해 클라이언트 인증이 필요한 경우 true이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="e40cf-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="e40cf-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="e40cf-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="e40cf-126">이 릴레이에 대 한 전송 보안이 필요한 경우 true이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false</span><span class="sxs-lookup"><span data-stu-id="e40cf-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="e40cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e40cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="e40cf-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="e40cf-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e40cf-129">-UserMetadata</span></span>
<span data-ttu-id="e40cf-130">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="e40cf-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="e40cf-131">-WcfRelayType</span></span>
<span data-ttu-id="e40cf-132">WcfRelay 유형.</span><span class="sxs-lookup"><span data-stu-id="e40cf-132">WcfRelay Type.</span></span>
<span data-ttu-id="e40cf-133">사용할 수 있는 값은 다음과 같습니다. ' NetTcp ' 또는 ' Http '</span><span class="sxs-lookup"><span data-stu-id="e40cf-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="e40cf-134">-확인</span><span class="sxs-lookup"><span data-stu-id="e40cf-134">-Confirm</span></span>
<span data-ttu-id="e40cf-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e40cf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e40cf-136">-WhatIf</span></span>
<span data-ttu-id="e40cf-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e40cf-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e40cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40cf-139">CommonParameters</span></span>
<span data-ttu-id="e40cf-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e40cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e40cf-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e40cf-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40cf-142">입력</span><span class="sxs-lookup"><span data-stu-id="e40cf-142">INPUTS</span></span>

### <span data-ttu-id="e40cf-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e40cf-143">System.String</span></span>
<span data-ttu-id="e40cf-144">PSWcfRelayAttributes System. Null 허용 ' 1 [[4.0.0.0], [시스템 부울, mscorlib, Version =, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e40cf-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="e40cf-145">출력</span><span class="sxs-lookup"><span data-stu-id="e40cf-145">OUTPUTS</span></span>

### <span data-ttu-id="e40cf-146">PSWcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="e40cf-146">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="e40cf-147">상속자</span><span class="sxs-lookup"><span data-stu-id="e40cf-147">NOTES</span></span>

## <span data-ttu-id="e40cf-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e40cf-148">RELATED LINKS</span></span>
