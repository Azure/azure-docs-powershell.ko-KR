---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204096"
---
# <span data-ttu-id="50def-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="50def-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="50def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50def-102">SYNOPSIS</span></span>
<span data-ttu-id="50def-103">별칭을 삭제합니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="50def-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="50def-104">구문</span><span class="sxs-lookup"><span data-stu-id="50def-104">SYNTAX</span></span>

### <span data-ttu-id="50def-105">GeoDRParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="50def-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50def-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50def-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50def-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50def-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50def-108">설명</span><span class="sxs-lookup"><span data-stu-id="50def-108">DESCRIPTION</span></span>
<span data-ttu-id="50def-109">**Remove-AzEventHubGeoDRConfiguration** cmdlet은 별칭을 삭제합니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="50def-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="50def-110">예제</span><span class="sxs-lookup"><span data-stu-id="50def-110">EXAMPLES</span></span>

### <span data-ttu-id="50def-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="50def-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="50def-112">별칭을 삭제합니다(재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="50def-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="50def-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50def-113">PARAMETERS</span></span>

### <span data-ttu-id="50def-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50def-114">-AsJob</span></span>
<span data-ttu-id="50def-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="50def-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50def-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50def-116">-DefaultProfile</span></span>
<span data-ttu-id="50def-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50def-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50def-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50def-118">-InputObject</span></span>
<span data-ttu-id="50def-119">Eventhub GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="50def-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="50def-120">-Name</span><span class="sxs-lookup"><span data-stu-id="50def-120">-Name</span></span>
<span data-ttu-id="50def-121">별칭(GeoDR)</span><span class="sxs-lookup"><span data-stu-id="50def-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="50def-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="50def-122">-Namespace</span></span>
<span data-ttu-id="50def-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="50def-123">Namespace Name</span></span>

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

### <span data-ttu-id="50def-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50def-124">-PassThru</span></span>
<span data-ttu-id="50def-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="50def-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="50def-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50def-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="50def-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50def-127">-ResourceGroupName</span></span>
<span data-ttu-id="50def-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="50def-128">Resource Group Name</span></span>

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

### <span data-ttu-id="50def-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50def-129">-ResourceId</span></span>
<span data-ttu-id="50def-130">GeoDRConfiguration 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="50def-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="50def-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50def-131">-Confirm</span></span>
<span data-ttu-id="50def-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50def-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50def-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50def-133">-WhatIf</span></span>
<span data-ttu-id="50def-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="50def-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50def-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50def-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50def-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50def-136">CommonParameters</span></span>
<span data-ttu-id="50def-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50def-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50def-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="50def-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50def-139">입력</span><span class="sxs-lookup"><span data-stu-id="50def-139">INPUTS</span></span>

### <span data-ttu-id="50def-140">System.String</span><span class="sxs-lookup"><span data-stu-id="50def-140">System.String</span></span>

### <span data-ttu-id="50def-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="50def-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="50def-142">출력</span><span class="sxs-lookup"><span data-stu-id="50def-142">OUTPUTS</span></span>

### <span data-ttu-id="50def-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="50def-143">System.Boolean</span></span>

## <span data-ttu-id="50def-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50def-144">NOTES</span></span>

## <span data-ttu-id="50def-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50def-145">RELATED LINKS</span></span>
