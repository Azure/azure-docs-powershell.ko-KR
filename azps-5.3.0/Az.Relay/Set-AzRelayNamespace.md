---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378022"
---
# <span data-ttu-id="9af5e-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="9af5e-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="9af5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af5e-102">SYNOPSIS</span></span>
<span data-ttu-id="9af5e-103">기존 Relay 네임스페이스에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="9af5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9af5e-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9af5e-105">설명</span><span class="sxs-lookup"><span data-stu-id="9af5e-105">DESCRIPTION</span></span>
<span data-ttu-id="9af5e-106">**Set-AzRelayNamespace** cmdlet은 리소스 그룹 내에서 지정된 Relay 네임스페이스에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="9af5e-107">예제</span><span class="sxs-lookup"><span data-stu-id="9af5e-107">EXAMPLES</span></span>

### <span data-ttu-id="9af5e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9af5e-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="9af5e-109">릴레이 네임스페이스를 새 설명으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="9af5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9af5e-110">PARAMETERS</span></span>

### <span data-ttu-id="9af5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af5e-111">-DefaultProfile</span></span>
<span data-ttu-id="9af5e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af5e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9af5e-113">-InputObject</span></span>
<span data-ttu-id="9af5e-114">Relay 네임스페이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9af5e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9af5e-115">-Name</span></span>
<span data-ttu-id="9af5e-116">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="9af5e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af5e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9af5e-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="9af5e-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="9af5e-119">-Tag</span></span>
<span data-ttu-id="9af5e-120">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-120">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af5e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9af5e-121">-Confirm</span></span>
<span data-ttu-id="9af5e-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9af5e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af5e-123">-WhatIf</span></span>
<span data-ttu-id="9af5e-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9af5e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af5e-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9af5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af5e-126">CommonParameters</span></span>
<span data-ttu-id="9af5e-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9af5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af5e-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9af5e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af5e-129">입력</span><span class="sxs-lookup"><span data-stu-id="9af5e-129">INPUTS</span></span>

### <span data-ttu-id="9af5e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9af5e-130">System.String</span></span>

### <span data-ttu-id="9af5e-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9af5e-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9af5e-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="9af5e-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="9af5e-133">출력</span><span class="sxs-lookup"><span data-stu-id="9af5e-133">OUTPUTS</span></span>

### <span data-ttu-id="9af5e-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9af5e-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="9af5e-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9af5e-135">NOTES</span></span>

## <span data-ttu-id="9af5e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9af5e-136">RELATED LINKS</span></span>
