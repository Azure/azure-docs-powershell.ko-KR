---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 1ab801c9eca278d5d117ddca881867371882980c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996809"
---
# <span data-ttu-id="d02c0-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="d02c0-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="d02c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d02c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d02c0-103">외부 서비스 이벤트에 대한 이벤트 트리거 구독을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="d02c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="d02c0-104">SYNTAX</span></span>

### <span data-ttu-id="d02c0-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d02c0-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d02c0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d02c0-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d02c0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d02c0-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d02c0-108">설명</span><span class="sxs-lookup"><span data-stu-id="d02c0-108">DESCRIPTION</span></span>
<span data-ttu-id="d02c0-109">이 명령은 트리거 정의에서 지정된 외부 서비스 이벤트에 대한 이벤트 트리거를 구독 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="d02c0-110">예제</span><span class="sxs-lookup"><span data-stu-id="d02c0-110">EXAMPLES</span></span>

### <span data-ttu-id="d02c0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d02c0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="d02c0-112">이 명령은 BlobEnetTrigger1 트리거를 트리거 정의에서 지정된 이벤트에 구독을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="d02c0-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d02c0-113">PARAMETERS</span></span>

### <span data-ttu-id="d02c0-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d02c0-114">-DataFactoryName</span></span>
<span data-ttu-id="d02c0-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-115">The data factory name.</span></span>

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

### <span data-ttu-id="d02c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d02c0-116">-DefaultProfile</span></span>
<span data-ttu-id="d02c0-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d02c0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d02c0-118">-Force</span></span>
<span data-ttu-id="d02c0-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d02c0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d02c0-120">-InputObject</span></span>
<span data-ttu-id="d02c0-121">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-121">The trigger object.</span></span>

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

### <span data-ttu-id="d02c0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d02c0-122">-Name</span></span>
<span data-ttu-id="d02c0-123">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-123">The trigger name.</span></span>

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

### <span data-ttu-id="d02c0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d02c0-124">-PassThru</span></span>
<span data-ttu-id="d02c0-125">지정된 경우 cmdlet은 성공적인 삭제 시 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="d02c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d02c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="d02c0-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-127">The resource group name.</span></span>

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

### <span data-ttu-id="d02c0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d02c0-128">-ResourceId</span></span>
<span data-ttu-id="d02c0-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d02c0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d02c0-130">-Confirm</span></span>
<span data-ttu-id="d02c0-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d02c0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d02c0-132">-WhatIf</span></span>
<span data-ttu-id="d02c0-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d02c0-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d02c0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d02c0-135">CommonParameters</span></span>
<span data-ttu-id="d02c0-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d02c0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d02c0-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d02c0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d02c0-138">입력</span><span class="sxs-lookup"><span data-stu-id="d02c0-138">INPUTS</span></span>

### <span data-ttu-id="d02c0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d02c0-139">System.String</span></span>
<span data-ttu-id="d02c0-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d02c0-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="d02c0-141">출력</span><span class="sxs-lookup"><span data-stu-id="d02c0-141">OUTPUTS</span></span>

### <span data-ttu-id="d02c0-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="d02c0-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="d02c0-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d02c0-143">NOTES</span></span>

## <span data-ttu-id="d02c0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d02c0-144">RELATED LINKS</span></span>

