---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537319"
---
# <span data-ttu-id="3059f-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3059f-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="3059f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3059f-102">SYNOPSIS</span></span>
<span data-ttu-id="3059f-103">Data factory의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3059f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3059f-104">SYNTAX</span></span>

### <span data-ttu-id="3059f-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3059f-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="3059f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3059f-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="3059f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3059f-107">DESCRIPTION</span></span>
<span data-ttu-id="3059f-108">**AzureRmDataFactoryV2Trigger** cmdlet은 data factory의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="3059f-109">트리거의 이름을 지정 하는 경우 cmdlet은 해당 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="3059f-110">이름을 지정 하지 않으면 cmdlet은 data factory의 모든 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="3059f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3059f-111">EXAMPLES</span></span>

### <span data-ttu-id="3059f-112">예제 1: 특정 트리거에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="3059f-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="3059f-113">Data factory "WikiADF"에서 생성 된 모든 트리거의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="3059f-114">예제 2: 모든 트리거에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="3059f-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="3059f-115">"WikiADF" 데이터 팩터리에 "ScheduledTrigger" 라는 단일 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="3059f-116">변수</span><span class="sxs-lookup"><span data-stu-id="3059f-116">PARAMETERS</span></span>

### <span data-ttu-id="3059f-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3059f-117">-DataFactory</span></span>
<span data-ttu-id="3059f-118">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3059f-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3059f-119">-DataFactoryName</span></span>
<span data-ttu-id="3059f-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-120">The data factory name.</span></span>

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

### <span data-ttu-id="3059f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="3059f-121">-Name</span></span>
<span data-ttu-id="3059f-122">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3059f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3059f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3059f-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-124">The resource group name.</span></span>

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

## <span data-ttu-id="3059f-125">입력</span><span class="sxs-lookup"><span data-stu-id="3059f-125">INPUTS</span></span>

### <span data-ttu-id="3059f-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3059f-126">System.String</span></span>
<span data-ttu-id="3059f-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3059f-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="3059f-128">출력</span><span class="sxs-lookup"><span data-stu-id="3059f-128">OUTPUTS</span></span>

### <span data-ttu-id="3059f-129">DataFactoryV2 ' 1 [[Microsoft Azure. PSTrigger, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3059f-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="3059f-130">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="3059f-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="3059f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3059f-131">NOTES</span></span>

## <span data-ttu-id="3059f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3059f-132">RELATED LINKS</span></span>
[<span data-ttu-id="3059f-133">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3059f-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3059f-134">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3059f-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3059f-135">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3059f-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3059f-136">제거-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3059f-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
