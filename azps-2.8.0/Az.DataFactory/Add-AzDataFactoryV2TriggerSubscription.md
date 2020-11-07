---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c99626e1323f10e98dcef1efc7ae622aab5f6b5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697092"
---
# <span data-ttu-id="24b3c-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="24b3c-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="24b3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="24b3c-103">이벤트 트리거를 외부 서비스 이벤트에 가입 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="24b3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24b3c-104">SYNTAX</span></span>

### <span data-ttu-id="24b3c-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="24b3c-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24b3c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24b3c-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24b3c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24b3c-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b3c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24b3c-108">DESCRIPTION</span></span>
<span data-ttu-id="24b3c-109">이 명령은 트리거 정의에서 지정 된 외부 서비스 이벤트에 대 한 이벤트 트리거를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="24b3c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24b3c-110">EXAMPLES</span></span>

### <span data-ttu-id="24b3c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="24b3c-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="24b3c-112">이 명령은 트리거 정의에서 지정 된 이벤트에 BlobEnetTrigger1 트리거를 구독 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="24b3c-113">변수</span><span class="sxs-lookup"><span data-stu-id="24b3c-113">PARAMETERS</span></span>

### <span data-ttu-id="24b3c-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24b3c-114">-DataFactoryName</span></span>
<span data-ttu-id="24b3c-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-115">The data factory name.</span></span>

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

### <span data-ttu-id="24b3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b3c-116">-DefaultProfile</span></span>
<span data-ttu-id="24b3c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b3c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24b3c-118">-InputObject</span></span>
<span data-ttu-id="24b3c-119">트리거 개체</span><span class="sxs-lookup"><span data-stu-id="24b3c-119">The trigger object.</span></span>

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

### <span data-ttu-id="24b3c-120">-이름</span><span class="sxs-lookup"><span data-stu-id="24b3c-120">-Name</span></span>
<span data-ttu-id="24b3c-121">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-121">The trigger name.</span></span>

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

### <span data-ttu-id="24b3c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b3c-122">-ResourceGroupName</span></span>
<span data-ttu-id="24b3c-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-123">The resource group name.</span></span>

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

### <span data-ttu-id="24b3c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24b3c-124">-ResourceId</span></span>
<span data-ttu-id="24b3c-125">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24b3c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="24b3c-126">-Confirm</span></span>
<span data-ttu-id="24b3c-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24b3c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b3c-128">-WhatIf</span></span>
<span data-ttu-id="24b3c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b3c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24b3c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b3c-131">CommonParameters</span></span>
<span data-ttu-id="24b3c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b3c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b3c-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b3c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b3c-134">입력</span><span class="sxs-lookup"><span data-stu-id="24b3c-134">INPUTS</span></span>

### <span data-ttu-id="24b3c-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24b3c-135">System.String</span></span>
<span data-ttu-id="24b3c-136">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="24b3c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="24b3c-137">출력</span><span class="sxs-lookup"><span data-stu-id="24b3c-137">OUTPUTS</span></span>

### <span data-ttu-id="24b3c-138">DataFactoryV2. PSTriggerSubscriptionStatus/.</span><span class="sxs-lookup"><span data-stu-id="24b3c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="24b3c-139">상속자</span><span class="sxs-lookup"><span data-stu-id="24b3c-139">NOTES</span></span>

## <span data-ttu-id="24b3c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24b3c-140">RELATED LINKS</span></span>

