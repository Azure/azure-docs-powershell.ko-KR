---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365716"
---
# <span data-ttu-id="f38ed-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="f38ed-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="f38ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f38ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f38ed-103">이벤트 트리거를 외부 서비스 이벤트에 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="f38ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="f38ed-104">SYNTAX</span></span>

### <span data-ttu-id="f38ed-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f38ed-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f38ed-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f38ed-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38ed-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f38ed-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f38ed-108">설명</span><span class="sxs-lookup"><span data-stu-id="f38ed-108">DESCRIPTION</span></span>
<span data-ttu-id="f38ed-109">이 명령은 트리거 정의에서 지정된 외부 서비스 이벤트에 대한 이벤트 트리거를 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="f38ed-110">예제</span><span class="sxs-lookup"><span data-stu-id="f38ed-110">EXAMPLES</span></span>

### <span data-ttu-id="f38ed-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f38ed-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="f38ed-112">이 명령은 BlobEnetTrigger1 트리거를 트리거 정의에서 지정된 이벤트로 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="f38ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f38ed-113">PARAMETERS</span></span>

### <span data-ttu-id="f38ed-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f38ed-114">-DataFactoryName</span></span>
<span data-ttu-id="f38ed-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-115">The data factory name.</span></span>

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

### <span data-ttu-id="f38ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38ed-116">-DefaultProfile</span></span>
<span data-ttu-id="f38ed-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f38ed-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f38ed-118">-Force</span></span>
<span data-ttu-id="f38ed-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-119">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38ed-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f38ed-120">-InputObject</span></span>
<span data-ttu-id="f38ed-121">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-121">The trigger object.</span></span>

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

### <span data-ttu-id="f38ed-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f38ed-122">-Name</span></span>
<span data-ttu-id="f38ed-123">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-123">The trigger name.</span></span>

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

### <span data-ttu-id="f38ed-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f38ed-124">-PassThru</span></span>
<span data-ttu-id="f38ed-125">지정된 경우 cmdlet은 성공적인 삭제 시 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-125">If specified, cmdlet will return return true on successful delete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f38ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="f38ed-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-127">The resource group name.</span></span>

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

### <span data-ttu-id="f38ed-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f38ed-128">-ResourceId</span></span>
<span data-ttu-id="f38ed-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f38ed-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f38ed-130">-Confirm</span></span>
<span data-ttu-id="f38ed-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f38ed-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38ed-132">-WhatIf</span></span>
<span data-ttu-id="f38ed-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f38ed-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f38ed-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f38ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38ed-135">CommonParameters</span></span>
<span data-ttu-id="f38ed-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38ed-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f38ed-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38ed-138">입력</span><span class="sxs-lookup"><span data-stu-id="f38ed-138">INPUTS</span></span>

### <span data-ttu-id="f38ed-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f38ed-139">System.String</span></span>
<span data-ttu-id="f38ed-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f38ed-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f38ed-141">출력</span><span class="sxs-lookup"><span data-stu-id="f38ed-141">OUTPUTS</span></span>

### <span data-ttu-id="f38ed-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f38ed-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="f38ed-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f38ed-143">NOTES</span></span>

## <span data-ttu-id="f38ed-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f38ed-144">RELATED LINKS</span></span>

