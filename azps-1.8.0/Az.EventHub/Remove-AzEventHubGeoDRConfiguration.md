---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: a0f5b056b273109b9b6372eaaeac275542275594
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700829"
---
# <span data-ttu-id="3a8c6-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8c6-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="3a8c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8c6-103">별칭을 삭제 합니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="3a8c6-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3a8c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a8c6-104">SYNTAX</span></span>

### <span data-ttu-id="3a8c6-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a8c6-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8c6-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a8c6-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8c6-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8c6-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8c6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3a8c6-108">DESCRIPTION</span></span>
<span data-ttu-id="3a8c6-109">AzEventHubGeoDRConfiguration cmdlet이 별칭 (재해 복구 구성)을 삭제 **함**</span><span class="sxs-lookup"><span data-stu-id="3a8c6-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3a8c6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3a8c6-110">EXAMPLES</span></span>

### <span data-ttu-id="3a8c6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a8c6-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="3a8c6-112">별칭을 삭제 합니다 (재해 복구 구성).</span><span class="sxs-lookup"><span data-stu-id="3a8c6-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="3a8c6-113">변수</span><span class="sxs-lookup"><span data-stu-id="3a8c6-113">PARAMETERS</span></span>

### <span data-ttu-id="3a8c6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a8c6-114">-AsJob</span></span>
<span data-ttu-id="3a8c6-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3a8c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a8c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8c6-116">-DefaultProfile</span></span>
<span data-ttu-id="3a8c6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a8c6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a8c6-118">-InputObject</span></span>
<span data-ttu-id="3a8c6-119">Eventhub GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="3a8c6-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="3a8c6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="3a8c6-120">-Name</span></span>
<span data-ttu-id="3a8c6-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="3a8c6-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="3a8c6-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3a8c6-122">-Namespace</span></span>
<span data-ttu-id="3a8c6-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3a8c6-123">Namespace Name</span></span>

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

### <span data-ttu-id="3a8c6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a8c6-124">-PassThru</span></span>
<span data-ttu-id="3a8c6-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a8c6-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a8c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a8c6-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3a8c6-128">Resource Group Name</span></span>

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

### <span data-ttu-id="3a8c6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a8c6-129">-ResourceId</span></span>
<span data-ttu-id="3a8c6-130">GeoDRConfiguration 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="3a8c6-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="3a8c6-131">-확인</span><span class="sxs-lookup"><span data-stu-id="3a8c6-131">-Confirm</span></span>
<span data-ttu-id="3a8c6-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8c6-133">-WhatIf</span></span>
<span data-ttu-id="3a8c6-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8c6-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8c6-136">CommonParameters</span></span>
<span data-ttu-id="3a8c6-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a8c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8c6-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a8c6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8c6-139">입력</span><span class="sxs-lookup"><span data-stu-id="3a8c6-139">INPUTS</span></span>

### <span data-ttu-id="3a8c6-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a8c6-140">System.String</span></span>

### <span data-ttu-id="3a8c6-141">PSEventHubDRConfigurationAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="3a8c6-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="3a8c6-142">출력</span><span class="sxs-lookup"><span data-stu-id="3a8c6-142">OUTPUTS</span></span>

### <span data-ttu-id="3a8c6-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3a8c6-143">System.Boolean</span></span>

## <span data-ttu-id="3a8c6-144">상속자</span><span class="sxs-lookup"><span data-stu-id="3a8c6-144">NOTES</span></span>

## <span data-ttu-id="3a8c6-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a8c6-145">RELATED LINKS</span></span>
