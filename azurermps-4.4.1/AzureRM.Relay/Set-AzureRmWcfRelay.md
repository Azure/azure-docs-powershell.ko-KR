---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: af4927631b126f068495b3b130dfc560874834cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702199"
---
# <span data-ttu-id="3943d-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="3943d-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="3943d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3943d-102">SYNOPSIS</span></span>
<span data-ttu-id="3943d-103">지정 된 릴레이 네임 스페이스의 WcfRelay에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3943d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3943d-104">SYNTAX</span></span>

### <span data-ttu-id="3943d-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3943d-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3943d-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="3943d-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3943d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3943d-107">DESCRIPTION</span></span>
<span data-ttu-id="3943d-108">Set-AzureRmWcfRelay cmdlet은 지정 된 릴레이 네임 스페이스의 WcfRelay에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="3943d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3943d-109">EXAMPLES</span></span>

### <span data-ttu-id="3943d-110">예제 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="3943d-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="3943d-111">예제 2-속성</span><span class="sxs-lookup"><span data-stu-id="3943d-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="3943d-112">지정 된 WcfRelay를 지정 된 네임 스페이스의 새 설명으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="3943d-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="3943d-114">변수</span><span class="sxs-lookup"><span data-stu-id="3943d-114">PARAMETERS</span></span>

### <span data-ttu-id="3943d-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="3943d-115">-UserMetadata</span></span>
<span data-ttu-id="3943d-116">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="3943d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="3943d-117">-Confirm</span></span>
<span data-ttu-id="3943d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3943d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3943d-119">-WhatIf</span></span>
<span data-ttu-id="3943d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3943d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3943d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3943d-122">-InputObject</span></span>
<span data-ttu-id="3943d-123">WcfRelay 개체</span><span class="sxs-lookup"><span data-stu-id="3943d-123">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3943d-124">-이름</span><span class="sxs-lookup"><span data-stu-id="3943d-124">-Name</span></span>
<span data-ttu-id="3943d-125">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-125">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3943d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3943d-126">-Namespace</span></span>
<span data-ttu-id="3943d-127">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3943d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3943d-128">-ResourceGroupName</span></span>
<span data-ttu-id="3943d-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3943d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3943d-130">-DefaultProfile</span></span>
<span data-ttu-id="3943d-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3943d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3943d-132">CommonParameters</span></span>
<span data-ttu-id="3943d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3943d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3943d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3943d-135">입력</span><span class="sxs-lookup"><span data-stu-id="3943d-135">INPUTS</span></span>

### <span data-ttu-id="3943d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3943d-136">-ResourceGroupName</span></span>
<span data-ttu-id="3943d-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3943d-137">System.String</span></span>

### <span data-ttu-id="3943d-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="3943d-138">-NamespaceName</span></span>
<span data-ttu-id="3943d-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3943d-139">System.String</span></span>

### <span data-ttu-id="3943d-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="3943d-140">-WcfRelayName</span></span>
<span data-ttu-id="3943d-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3943d-141">System.String</span></span>

### <span data-ttu-id="3943d-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3943d-142">-InputObject</span></span>
<span data-ttu-id="3943d-143">WcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="3943d-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="3943d-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="3943d-144">-WcfRelayType</span></span>
<span data-ttu-id="3943d-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3943d-145">System.String</span></span>

### <span data-ttu-id="3943d-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="3943d-146">-UserMetadata</span></span>
<span data-ttu-id="3943d-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3943d-147">System.String</span></span>

## <span data-ttu-id="3943d-148">출력</span><span class="sxs-lookup"><span data-stu-id="3943d-148">OUTPUTS</span></span>

### <span data-ttu-id="3943d-149">WcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="3943d-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="3943d-150">예제 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="3943d-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="3943d-151">WcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="3943d-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="3943d-152">RelayType: Http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: False RequiresTransportSecurity: True IsDynamic: False UserMetadata: usermetadata는 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록 및 해당 연락처 정보 (예: 사용자 정의 구성 설정을 저장할 수 있음)와 같은 desc riptive 데이터를 저장 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3943d-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="3943d-153">Id:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/네임 스페이스/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. 릴레이/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="3943d-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="3943d-154">예제 2-속성</span><span class="sxs-lookup"><span data-stu-id="3943d-154">Example 2 - Properties</span></span>

### <span data-ttu-id="3943d-155">WcfRelayAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="3943d-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="3943d-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: True RequiresTransportSecurity: True IsDynamic: False UserMetadata: 사용자 메타 데이터 Id:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/네임 스페이스/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 이름: TestWCFRelay 형식: Microsoft. 릴레이/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="3943d-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="3943d-157">상속자</span><span class="sxs-lookup"><span data-stu-id="3943d-157">NOTES</span></span>

## <span data-ttu-id="3943d-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3943d-158">RELATED LINKS</span></span>

