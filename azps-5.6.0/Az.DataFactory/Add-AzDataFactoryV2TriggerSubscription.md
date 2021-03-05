---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c74eb60e698cff0d95a4361235c9282f1405dce0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992805"
---
# <span data-ttu-id="f54d2-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="f54d2-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="f54d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f54d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f54d2-103">외부 서비스 이벤트에 이벤트 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="f54d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="f54d2-104">SYNTAX</span></span>

### <span data-ttu-id="f54d2-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f54d2-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f54d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f54d2-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f54d2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f54d2-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f54d2-108">설명</span><span class="sxs-lookup"><span data-stu-id="f54d2-108">DESCRIPTION</span></span>
<span data-ttu-id="f54d2-109">이 명령은 트리거 정의에서 지정된 외부 서비스 이벤트에 이벤트 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="f54d2-110">예제</span><span class="sxs-lookup"><span data-stu-id="f54d2-110">EXAMPLES</span></span>

### <span data-ttu-id="f54d2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f54d2-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="f54d2-112">이 명령은 BlobEnetTrigger1 트리거를 트리거 정의에서 지정된 이벤트에 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="f54d2-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f54d2-113">PARAMETERS</span></span>

### <span data-ttu-id="f54d2-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f54d2-114">-DataFactoryName</span></span>
<span data-ttu-id="f54d2-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54d2-116">-DefaultProfile</span></span>
<span data-ttu-id="f54d2-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f54d2-118">-InputObject</span></span>
<span data-ttu-id="f54d2-119">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f54d2-120">-Name</span></span>
<span data-ttu-id="f54d2-121">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f54d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="f54d2-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f54d2-124">-ResourceId</span></span>
<span data-ttu-id="f54d2-125">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-126">-확인</span><span class="sxs-lookup"><span data-stu-id="f54d2-126">-Confirm</span></span>
<span data-ttu-id="f54d2-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f54d2-128">-WhatIf</span></span>
<span data-ttu-id="f54d2-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f54d2-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f54d2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54d2-131">CommonParameters</span></span>
<span data-ttu-id="f54d2-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f54d2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54d2-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f54d2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54d2-134">입력</span><span class="sxs-lookup"><span data-stu-id="f54d2-134">INPUTS</span></span>

### <span data-ttu-id="f54d2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f54d2-135">System.String</span></span>
<span data-ttu-id="f54d2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f54d2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f54d2-137">출력</span><span class="sxs-lookup"><span data-stu-id="f54d2-137">OUTPUTS</span></span>

### <span data-ttu-id="f54d2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f54d2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="f54d2-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f54d2-139">NOTES</span></span>

## <span data-ttu-id="f54d2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f54d2-140">RELATED LINKS</span></span>

