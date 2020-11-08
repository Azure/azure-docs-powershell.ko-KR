---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212526"
---
# <span data-ttu-id="a11f7-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="a11f7-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="a11f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a11f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a11f7-103">이벤트 트리거를 외부 서비스 이벤트에 대 한 구독 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="a11f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a11f7-104">SYNTAX</span></span>

### <span data-ttu-id="a11f7-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a11f7-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a11f7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a11f7-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a11f7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a11f7-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a11f7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a11f7-108">DESCRIPTION</span></span>
<span data-ttu-id="a11f7-109">이 명령은 트리거 정의에서 지정 된 외부 서비스 이벤트에 대 한 이벤트 트리거를 구독 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="a11f7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a11f7-110">EXAMPLES</span></span>

### <span data-ttu-id="a11f7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a11f7-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="a11f7-112">이 명령은 트리거 정의에서 지정 된 이벤트에 대 한 BlobEnetTrigger1 trigger의 구독을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="a11f7-113">변수</span><span class="sxs-lookup"><span data-stu-id="a11f7-113">PARAMETERS</span></span>

### <span data-ttu-id="a11f7-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a11f7-114">-DataFactoryName</span></span>
<span data-ttu-id="a11f7-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-115">The data factory name.</span></span>

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

### <span data-ttu-id="a11f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11f7-116">-DefaultProfile</span></span>
<span data-ttu-id="a11f7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a11f7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a11f7-118">-Force</span></span>
<span data-ttu-id="a11f7-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a11f7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a11f7-120">-InputObject</span></span>
<span data-ttu-id="a11f7-121">트리거 개체</span><span class="sxs-lookup"><span data-stu-id="a11f7-121">The trigger object.</span></span>

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

### <span data-ttu-id="a11f7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a11f7-122">-Name</span></span>
<span data-ttu-id="a11f7-123">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-123">The trigger name.</span></span>

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

### <span data-ttu-id="a11f7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a11f7-124">-PassThru</span></span>
<span data-ttu-id="a11f7-125">지정 하면 delete가 성공한 경우 false를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="a11f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="a11f7-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-127">The resource group name.</span></span>

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

### <span data-ttu-id="a11f7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a11f7-128">-ResourceId</span></span>
<span data-ttu-id="a11f7-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a11f7-130">-확인</span><span class="sxs-lookup"><span data-stu-id="a11f7-130">-Confirm</span></span>
<span data-ttu-id="a11f7-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a11f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11f7-132">-WhatIf</span></span>
<span data-ttu-id="a11f7-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11f7-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a11f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11f7-135">CommonParameters</span></span>
<span data-ttu-id="a11f7-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11f7-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a11f7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11f7-138">입력</span><span class="sxs-lookup"><span data-stu-id="a11f7-138">INPUTS</span></span>

### <span data-ttu-id="a11f7-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a11f7-139">System.String</span></span>
<span data-ttu-id="a11f7-140">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="a11f7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="a11f7-141">출력</span><span class="sxs-lookup"><span data-stu-id="a11f7-141">OUTPUTS</span></span>

### <span data-ttu-id="a11f7-142">DataFactoryV2. PSTriggerSubscriptionStatus/.</span><span class="sxs-lookup"><span data-stu-id="a11f7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="a11f7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a11f7-143">NOTES</span></span>

## <span data-ttu-id="a11f7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a11f7-144">RELATED LINKS</span></span>

