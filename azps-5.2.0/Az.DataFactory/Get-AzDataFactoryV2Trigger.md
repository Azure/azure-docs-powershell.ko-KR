---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 989a898605488fc7cfaa828bfd8c5b9b61378a27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338709"
---
# <span data-ttu-id="8c2fa-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c2fa-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="8c2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2fa-103">데이터 팩터리의 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="8c2fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c2fa-104">SYNTAX</span></span>

### <span data-ttu-id="8c2fa-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8c2fa-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c2fa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8c2fa-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c2fa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c2fa-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c2fa-108">설명</span><span class="sxs-lookup"><span data-stu-id="8c2fa-108">DESCRIPTION</span></span>
<span data-ttu-id="8c2fa-109">**Get-AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리의 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="8c2fa-110">트리거의 이름을 지정하는 경우 cmdlet은 해당 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="8c2fa-111">이름을 지정하지 않으면 cmdlet은 데이터 팩터리의 모든 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="8c2fa-112">예제</span><span class="sxs-lookup"><span data-stu-id="8c2fa-112">EXAMPLES</span></span>

### <span data-ttu-id="8c2fa-113">예제 1: 특정 트리거에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="8c2fa-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="8c2fa-114">데이터 팩터리 "WikiADF"에서 생성된 모든 트리거 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="8c2fa-115">예제 2: 모든 트리거에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="8c2fa-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="8c2fa-116">데이터 팩터리 "WikiADF"에서 "ScheduledTrigger"라는 단일 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="8c2fa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c2fa-117">PARAMETERS</span></span>

### <span data-ttu-id="8c2fa-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c2fa-118">-DataFactory</span></span>
<span data-ttu-id="8c2fa-119">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2fa-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8c2fa-120">-DataFactoryName</span></span>
<span data-ttu-id="8c2fa-121">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-121">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2fa-122">-DefaultProfile</span></span>
<span data-ttu-id="8c2fa-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c2fa-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8c2fa-124">-Name</span></span>
<span data-ttu-id="8c2fa-125">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c2fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c2fa-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2fa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c2fa-128">-ResourceId</span></span>
<span data-ttu-id="8c2fa-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2fa-130">CommonParameters</span></span>
<span data-ttu-id="8c2fa-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2fa-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c2fa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2fa-133">입력</span><span class="sxs-lookup"><span data-stu-id="8c2fa-133">INPUTS</span></span>

### <span data-ttu-id="8c2fa-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8c2fa-134">System.String</span></span>

### <span data-ttu-id="8c2fa-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8c2fa-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8c2fa-136">출력</span><span class="sxs-lookup"><span data-stu-id="8c2fa-136">OUTPUTS</span></span>

### <span data-ttu-id="8c2fa-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8c2fa-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8c2fa-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c2fa-138">NOTES</span></span>

## <span data-ttu-id="8c2fa-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c2fa-139">RELATED LINKS</span></span>

[<span data-ttu-id="8c2fa-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c2fa-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8c2fa-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c2fa-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8c2fa-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c2fa-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8c2fa-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8c2fa-143">Remove-AzDataFactoryV2Trigger</span></span>]()
