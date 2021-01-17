---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368054"
---
# <span data-ttu-id="dca6e-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="dca6e-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="dca6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca6e-102">SYNOPSIS</span></span>
<span data-ttu-id="dca6e-103">새 Relay 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="dca6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="dca6e-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca6e-105">설명</span><span class="sxs-lookup"><span data-stu-id="dca6e-105">DESCRIPTION</span></span>
<span data-ttu-id="dca6e-106">**New-AzRelayNamespace** cmdlet은 새 Relay 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="dca6e-107">네임스페이스 리소스 매니페스트를 만들면 변경이 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="dca6e-108">예제</span><span class="sxs-lookup"><span data-stu-id="dca6e-108">EXAMPLES</span></span>

### <span data-ttu-id="dca6e-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="dca6e-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="dca6e-110">지정된 리소스 그룹 내에서 새 Relay 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="dca6e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dca6e-111">PARAMETERS</span></span>

### <span data-ttu-id="dca6e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca6e-112">-DefaultProfile</span></span>
<span data-ttu-id="dca6e-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dca6e-114">-Location</span><span class="sxs-lookup"><span data-stu-id="dca6e-114">-Location</span></span>
<span data-ttu-id="dca6e-115">릴레이 네임스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="dca6e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dca6e-116">-Name</span></span>
<span data-ttu-id="dca6e-117">릴레이 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="dca6e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca6e-118">-ResourceGroupName</span></span>
<span data-ttu-id="dca6e-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="dca6e-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="dca6e-120">-Tag</span></span>
<span data-ttu-id="dca6e-121">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="dca6e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dca6e-122">-Confirm</span></span>
<span data-ttu-id="dca6e-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca6e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca6e-124">-WhatIf</span></span>
<span data-ttu-id="dca6e-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dca6e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca6e-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca6e-127">CommonParameters</span></span>
<span data-ttu-id="dca6e-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dca6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca6e-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dca6e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca6e-130">입력</span><span class="sxs-lookup"><span data-stu-id="dca6e-130">INPUTS</span></span>

### <span data-ttu-id="dca6e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dca6e-131">System.String</span></span>

### <span data-ttu-id="dca6e-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="dca6e-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dca6e-133">출력</span><span class="sxs-lookup"><span data-stu-id="dca6e-133">OUTPUTS</span></span>

### <span data-ttu-id="dca6e-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="dca6e-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="dca6e-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dca6e-135">NOTES</span></span>

## <span data-ttu-id="dca6e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dca6e-136">RELATED LINKS</span></span>
