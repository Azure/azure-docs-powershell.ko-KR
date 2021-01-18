---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493023"
---
# <span data-ttu-id="0ed12-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="0ed12-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="0ed12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed12-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed12-103">이 작업은 재해 복구를 사용하지 않도록 설정하고 기본 네임스페이스에서 보조 네임스페이스로 변경 내용 복제를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0ed12-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ed12-104">SYNTAX</span></span>

### <span data-ttu-id="0ed12-105">GeoDRParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ed12-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ed12-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0ed12-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ed12-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ed12-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ed12-108">설명</span><span class="sxs-lookup"><span data-stu-id="0ed12-108">DESCRIPTION</span></span>
<span data-ttu-id="0ed12-109">**Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet은 재해 복구를 사용하지 않도록 설정하고 기본 네임스페이스에서 보조 네임스페이스로 변경 내용 복제를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0ed12-110">예제</span><span class="sxs-lookup"><span data-stu-id="0ed12-110">EXAMPLES</span></span>

### <span data-ttu-id="0ed12-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ed12-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="0ed12-112">이 작업은 재해 복구를 사용하지 않도록 설정하고 기본 네임스페이스에서 보조 네임스페이스로 변경 내용 복제를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="0ed12-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ed12-113">PARAMETERS</span></span>

### <span data-ttu-id="0ed12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed12-114">-DefaultProfile</span></span>
<span data-ttu-id="0ed12-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed12-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ed12-116">-InputObject</span></span>
<span data-ttu-id="0ed12-117">Eventhub GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="0ed12-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed12-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0ed12-118">-Name</span></span>
<span data-ttu-id="0ed12-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="0ed12-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed12-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0ed12-120">-Namespace</span></span>
<span data-ttu-id="0ed12-121">네임스페이스 이름 - 기본 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="0ed12-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed12-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ed12-122">-PassThru</span></span>
<span data-ttu-id="0ed12-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ed12-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed12-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ed12-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0ed12-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed12-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ed12-127">-ResourceId</span></span>
<span data-ttu-id="0ed12-128">GeoDRConfiguration 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0ed12-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed12-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ed12-129">-Confirm</span></span>
<span data-ttu-id="0ed12-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed12-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed12-131">-WhatIf</span></span>
<span data-ttu-id="0ed12-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0ed12-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ed12-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed12-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed12-134">CommonParameters</span></span>
<span data-ttu-id="0ed12-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed12-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed12-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0ed12-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed12-137">입력</span><span class="sxs-lookup"><span data-stu-id="0ed12-137">INPUTS</span></span>

### <span data-ttu-id="0ed12-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0ed12-138">System.String</span></span>

### <span data-ttu-id="0ed12-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0ed12-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="0ed12-140">출력</span><span class="sxs-lookup"><span data-stu-id="0ed12-140">OUTPUTS</span></span>

### <span data-ttu-id="0ed12-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ed12-141">System.Boolean</span></span>

## <span data-ttu-id="0ed12-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ed12-142">NOTES</span></span>

## <span data-ttu-id="0ed12-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ed12-143">RELATED LINKS</span></span>
