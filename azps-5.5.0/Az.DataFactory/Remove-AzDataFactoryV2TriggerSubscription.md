---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208709"
---
# <span data-ttu-id="e8339-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="e8339-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="e8339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8339-102">SYNOPSIS</span></span>
<span data-ttu-id="e8339-103">이벤트 트리거를 외부 서비스 이벤트에 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="e8339-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8339-104">SYNTAX</span></span>

### <span data-ttu-id="e8339-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e8339-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8339-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8339-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8339-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8339-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8339-108">설명</span><span class="sxs-lookup"><span data-stu-id="e8339-108">DESCRIPTION</span></span>
<span data-ttu-id="e8339-109">이 명령은 트리거 정의에서 지정된 외부 서비스 이벤트에 대한 이벤트 트리거를 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="e8339-110">예제</span><span class="sxs-lookup"><span data-stu-id="e8339-110">EXAMPLES</span></span>

### <span data-ttu-id="e8339-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8339-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="e8339-112">이 명령은 BlobEnetTrigger1 트리거를 트리거 정의에서 지정된 이벤트로 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="e8339-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8339-113">PARAMETERS</span></span>

### <span data-ttu-id="e8339-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8339-114">-DataFactoryName</span></span>
<span data-ttu-id="e8339-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-115">The data factory name.</span></span>

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

### <span data-ttu-id="e8339-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8339-116">-DefaultProfile</span></span>
<span data-ttu-id="e8339-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8339-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e8339-118">-Force</span></span>
<span data-ttu-id="e8339-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e8339-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8339-120">-InputObject</span></span>
<span data-ttu-id="e8339-121">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-121">The trigger object.</span></span>

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

### <span data-ttu-id="e8339-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8339-122">-Name</span></span>
<span data-ttu-id="e8339-123">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-123">The trigger name.</span></span>

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

### <span data-ttu-id="e8339-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8339-124">-PassThru</span></span>
<span data-ttu-id="e8339-125">지정된 경우 cmdlet은 성공적인 삭제 시 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="e8339-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8339-126">-ResourceGroupName</span></span>
<span data-ttu-id="e8339-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-127">The resource group name.</span></span>

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

### <span data-ttu-id="e8339-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8339-128">-ResourceId</span></span>
<span data-ttu-id="e8339-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e8339-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8339-130">-Confirm</span></span>
<span data-ttu-id="e8339-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8339-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8339-132">-WhatIf</span></span>
<span data-ttu-id="e8339-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e8339-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8339-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8339-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8339-135">CommonParameters</span></span>
<span data-ttu-id="e8339-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8339-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8339-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8339-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8339-138">입력</span><span class="sxs-lookup"><span data-stu-id="e8339-138">INPUTS</span></span>

### <span data-ttu-id="e8339-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e8339-139">System.String</span></span>
<span data-ttu-id="e8339-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e8339-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="e8339-141">출력</span><span class="sxs-lookup"><span data-stu-id="e8339-141">OUTPUTS</span></span>

### <span data-ttu-id="e8339-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e8339-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="e8339-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8339-143">NOTES</span></span>

## <span data-ttu-id="e8339-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8339-144">RELATED LINKS</span></span>

