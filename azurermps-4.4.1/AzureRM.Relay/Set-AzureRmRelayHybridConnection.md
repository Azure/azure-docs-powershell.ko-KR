---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703336"
---
# <span data-ttu-id="1389c-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="1389c-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="1389c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1389c-102">SYNOPSIS</span></span>
<span data-ttu-id="1389c-103">지정 된 릴레이 네임 스페이스의 HybridConnection에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1389c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1389c-104">SYNTAX</span></span>

### <span data-ttu-id="1389c-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1389c-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1389c-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1389c-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1389c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1389c-107">DESCRIPTION</span></span>
<span data-ttu-id="1389c-108">Set-AzureRmRelayHybridConnection cmdlet은 지정 된 릴레이 네임 스페이스의 HybridConnection에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="1389c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1389c-109">EXAMPLES</span></span>

### <span data-ttu-id="1389c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1389c-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### <span data-ttu-id="1389c-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="1389c-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

<span data-ttu-id="1389c-112">지정 된 HybridConnection를 지정 된 네임 스페이스의 새 설명으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="1389c-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="1389c-114">변수</span><span class="sxs-lookup"><span data-stu-id="1389c-114">PARAMETERS</span></span>

### <span data-ttu-id="1389c-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1389c-115">-UserMetadata</span></span>
<span data-ttu-id="1389c-116">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="1389c-117">-확인</span><span class="sxs-lookup"><span data-stu-id="1389c-117">-Confirm</span></span>
<span data-ttu-id="1389c-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1389c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1389c-119">-WhatIf</span></span>
<span data-ttu-id="1389c-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1389c-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1389c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1389c-122">-InputObject</span></span>
<span data-ttu-id="1389c-123">HybridConnections 개체</span><span class="sxs-lookup"><span data-stu-id="1389c-123">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1389c-124">-이름</span><span class="sxs-lookup"><span data-stu-id="1389c-124">-Name</span></span>
<span data-ttu-id="1389c-125">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-125">HybridConnections Name.</span></span>

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

### <span data-ttu-id="1389c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1389c-126">-Namespace</span></span>
<span data-ttu-id="1389c-127">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-127">Namespace Name.</span></span>

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

### <span data-ttu-id="1389c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1389c-128">-ResourceGroupName</span></span>
<span data-ttu-id="1389c-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="1389c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1389c-130">-DefaultProfile</span></span>
<span data-ttu-id="1389c-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1389c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1389c-132">CommonParameters</span></span>
<span data-ttu-id="1389c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1389c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1389c-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1389c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1389c-135">입력</span><span class="sxs-lookup"><span data-stu-id="1389c-135">INPUTS</span></span>

### <span data-ttu-id="1389c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1389c-136">-ResourceGroupName</span></span>
<span data-ttu-id="1389c-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1389c-137">System.String</span></span>

### <span data-ttu-id="1389c-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1389c-138">-NamespaceName</span></span>
<span data-ttu-id="1389c-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1389c-139">System.String</span></span>

### <span data-ttu-id="1389c-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="1389c-140">-WcfRelayName</span></span>
<span data-ttu-id="1389c-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1389c-141">System.String</span></span>

### <span data-ttu-id="1389c-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1389c-142">-InputObject</span></span>
<span data-ttu-id="1389c-143">HybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="1389c-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="1389c-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1389c-144">-UserMetadata</span></span>
<span data-ttu-id="1389c-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1389c-145">System.String</span></span>

## <span data-ttu-id="1389c-146">출력</span><span class="sxs-lookup"><span data-stu-id="1389c-146">OUTPUTS</span></span>

### <span data-ttu-id="1389c-147">예제-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="1389c-147">Examples - 1 : InputObject</span></span>
<span data-ttu-id="1389c-148">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:08:11 PM ListenerCount: RequiresClientAuthorization: True UserMetadata: Test UserMetadata Id:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 이름: TestHybirdConnection2 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="1389c-148">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:08:11 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="1389c-149">예제-2: 속성</span><span class="sxs-lookup"><span data-stu-id="1389c-149">Examples - 2 : Properties</span></span>
<span data-ttu-id="1389c-150">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:10:25 PM ListenerCount: RequiresClientAuthorization: True UserMetadata: 테스트 UserMetadata 업데이트 됨 Id:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name: TestHybirdConnection1 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="1389c-150">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:10:25 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata updated Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="1389c-151">상속자</span><span class="sxs-lookup"><span data-stu-id="1389c-151">NOTES</span></span>

## <span data-ttu-id="1389c-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1389c-152">RELATED LINKS</span></span>

