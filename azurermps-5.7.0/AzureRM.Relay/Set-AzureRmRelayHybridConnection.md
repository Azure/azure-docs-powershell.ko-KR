---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 88f44a2b399f36f8edf6a57d2f1dc5821029a156
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528851"
---
# <span data-ttu-id="73bbd-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="73bbd-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="73bbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="73bbd-103">지정 된 릴레이 네임 스페이스의 HybridConnection에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73bbd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73bbd-104">SYNTAX</span></span>

### <span data-ttu-id="73bbd-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="73bbd-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73bbd-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="73bbd-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73bbd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="73bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="73bbd-108">Set-AzureRmRelayHybridConnection cmdlet은 지정 된 릴레이 네임 스페이스의 HybridConnection에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="73bbd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="73bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="73bbd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="73bbd-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

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

### <span data-ttu-id="73bbd-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="73bbd-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

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

<span data-ttu-id="73bbd-112">지정 된 HybridConnection를 지정 된 네임 스페이스의 새 설명으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="73bbd-113">이 예제에서는 UserMetadata 속성을 새 값으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="73bbd-114">변수</span><span class="sxs-lookup"><span data-stu-id="73bbd-114">PARAMETERS</span></span>

### <span data-ttu-id="73bbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bbd-115">-DefaultProfile</span></span>
<span data-ttu-id="73bbd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73bbd-117">-InputObject</span></span>
<span data-ttu-id="73bbd-118">HybridConnections 개체</span><span class="sxs-lookup"><span data-stu-id="73bbd-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-119">-이름</span><span class="sxs-lookup"><span data-stu-id="73bbd-119">-Name</span></span>
<span data-ttu-id="73bbd-120">HybridConnections 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73bbd-121">-Namespace</span></span>
<span data-ttu-id="73bbd-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bbd-123">-ResourceGroupName</span></span>
<span data-ttu-id="73bbd-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-124">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="73bbd-125">-UserMetadata</span></span>
<span data-ttu-id="73bbd-126">Usermetadata 가져오거나 설정 HybridConnection 끝점에 대 한 사용자 정의 문자열 데이터를 저장 하는 자리 표시자입니다. 예: 팀 목록과 같은 설명 데이터를 저장 하는 데 사용 될 수 있으며 사용자가 정의한 구성 설정을 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-127">-확인</span><span class="sxs-lookup"><span data-stu-id="73bbd-127">-Confirm</span></span>
<span data-ttu-id="73bbd-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73bbd-129">-WhatIf</span></span>
<span data-ttu-id="73bbd-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73bbd-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bbd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bbd-132">CommonParameters</span></span>
<span data-ttu-id="73bbd-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bbd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bbd-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bbd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bbd-135">입력</span><span class="sxs-lookup"><span data-stu-id="73bbd-135">INPUTS</span></span>

### <span data-ttu-id="73bbd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bbd-136">-ResourceGroupName</span></span>
<span data-ttu-id="73bbd-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73bbd-137">System.String</span></span>

### <span data-ttu-id="73bbd-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="73bbd-138">-NamespaceName</span></span>
<span data-ttu-id="73bbd-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73bbd-139">System.String</span></span>

### <span data-ttu-id="73bbd-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="73bbd-140">-WcfRelayName</span></span>
<span data-ttu-id="73bbd-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73bbd-141">System.String</span></span>

### <span data-ttu-id="73bbd-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73bbd-142">-InputObject</span></span>
<span data-ttu-id="73bbd-143">HybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="73bbd-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="73bbd-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="73bbd-144">-UserMetadata</span></span>
<span data-ttu-id="73bbd-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73bbd-145">System.String</span></span>

## <span data-ttu-id="73bbd-146">출력</span><span class="sxs-lookup"><span data-stu-id="73bbd-146">OUTPUTS</span></span>

### <span data-ttu-id="73bbd-147">HybridConnectionAttibutes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="73bbd-147">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="73bbd-148">상속자</span><span class="sxs-lookup"><span data-stu-id="73bbd-148">NOTES</span></span>

## <span data-ttu-id="73bbd-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73bbd-149">RELATED LINKS</span></span>

