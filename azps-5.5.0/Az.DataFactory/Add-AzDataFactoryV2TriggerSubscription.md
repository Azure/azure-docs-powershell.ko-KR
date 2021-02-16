---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204477"
---
# <span data-ttu-id="1c09b-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="1c09b-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="1c09b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c09b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c09b-103">이벤트 트리거를 외부 서비스 이벤트에 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="1c09b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c09b-104">SYNTAX</span></span>

### <span data-ttu-id="1c09b-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c09b-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c09b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c09b-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c09b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c09b-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c09b-108">설명</span><span class="sxs-lookup"><span data-stu-id="1c09b-108">DESCRIPTION</span></span>
<span data-ttu-id="1c09b-109">이 명령은 트리거 정의에서 지정된 외부 서비스 이벤트에 이벤트 트리거를 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="1c09b-110">예제</span><span class="sxs-lookup"><span data-stu-id="1c09b-110">EXAMPLES</span></span>

### <span data-ttu-id="1c09b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c09b-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="1c09b-112">이 명령은 BlobEnetTrigger1 트리거를 트리거 정의에서 지정된 이벤트에 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="1c09b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c09b-113">PARAMETERS</span></span>

### <span data-ttu-id="1c09b-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1c09b-114">-DataFactoryName</span></span>
<span data-ttu-id="1c09b-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-115">The data factory name.</span></span>

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

### <span data-ttu-id="1c09b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c09b-116">-DefaultProfile</span></span>
<span data-ttu-id="1c09b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c09b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c09b-118">-InputObject</span></span>
<span data-ttu-id="1c09b-119">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-119">The trigger object.</span></span>

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

### <span data-ttu-id="1c09b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1c09b-120">-Name</span></span>
<span data-ttu-id="1c09b-121">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-121">The trigger name.</span></span>

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

### <span data-ttu-id="1c09b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c09b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c09b-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-123">The resource group name.</span></span>

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

### <span data-ttu-id="1c09b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c09b-124">-ResourceId</span></span>
<span data-ttu-id="1c09b-125">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1c09b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c09b-126">-Confirm</span></span>
<span data-ttu-id="1c09b-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c09b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c09b-128">-WhatIf</span></span>
<span data-ttu-id="1c09b-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c09b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c09b-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c09b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c09b-131">CommonParameters</span></span>
<span data-ttu-id="1c09b-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c09b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c09b-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1c09b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c09b-134">입력</span><span class="sxs-lookup"><span data-stu-id="1c09b-134">INPUTS</span></span>

### <span data-ttu-id="1c09b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1c09b-135">System.String</span></span>
<span data-ttu-id="1c09b-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="1c09b-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="1c09b-137">출력</span><span class="sxs-lookup"><span data-stu-id="1c09b-137">OUTPUTS</span></span>

### <span data-ttu-id="1c09b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="1c09b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="1c09b-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c09b-139">NOTES</span></span>

## <span data-ttu-id="1c09b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c09b-140">RELATED LINKS</span></span>

