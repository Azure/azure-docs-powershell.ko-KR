---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 25c633c2929967a5fb580addb78639bff8b6197f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000368"
---
# <span data-ttu-id="d268f-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="d268f-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="d268f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d268f-102">SYNOPSIS</span></span>
<span data-ttu-id="d268f-103">기존 릴레이 네임스페이스에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="d268f-104">구문</span><span class="sxs-lookup"><span data-stu-id="d268f-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d268f-105">설명</span><span class="sxs-lookup"><span data-stu-id="d268f-105">DESCRIPTION</span></span>
<span data-ttu-id="d268f-106">**Set-AzRelayNamespace** cmdlet은 리소스 그룹 내에서 지정된 릴레이 네임스페이스에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="d268f-107">예제</span><span class="sxs-lookup"><span data-stu-id="d268f-107">EXAMPLES</span></span>

### <span data-ttu-id="d268f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d268f-108">Example 1</span></span>
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

<span data-ttu-id="d268f-109">새 설명으로 릴레이 네임스페이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="d268f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d268f-110">PARAMETERS</span></span>

### <span data-ttu-id="d268f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d268f-111">-DefaultProfile</span></span>
<span data-ttu-id="d268f-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d268f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d268f-113">-InputObject</span></span>
<span data-ttu-id="d268f-114">릴레이 네임스페이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="d268f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d268f-115">-Name</span></span>
<span data-ttu-id="d268f-116">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="d268f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d268f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d268f-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d268f-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="d268f-119">-Tag</span></span>
<span data-ttu-id="d268f-120">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="d268f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d268f-121">-Confirm</span></span>
<span data-ttu-id="d268f-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d268f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d268f-123">-WhatIf</span></span>
<span data-ttu-id="d268f-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d268f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d268f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d268f-126">CommonParameters</span></span>
<span data-ttu-id="d268f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d268f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d268f-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d268f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d268f-129">입력</span><span class="sxs-lookup"><span data-stu-id="d268f-129">INPUTS</span></span>

### <span data-ttu-id="d268f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d268f-130">System.String</span></span>

### <span data-ttu-id="d268f-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d268f-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d268f-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="d268f-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="d268f-133">출력</span><span class="sxs-lookup"><span data-stu-id="d268f-133">OUTPUTS</span></span>

### <span data-ttu-id="d268f-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d268f-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="d268f-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d268f-135">NOTES</span></span>

## <span data-ttu-id="d268f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d268f-136">RELATED LINKS</span></span>
