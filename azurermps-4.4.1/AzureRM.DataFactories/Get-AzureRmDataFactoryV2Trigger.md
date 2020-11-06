---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 3d5db6b7aa1b7c2ffdd63292696230e2d12bd4c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528219"
---
# <span data-ttu-id="981cf-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="981cf-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="981cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="981cf-102">SYNOPSIS</span></span>
<span data-ttu-id="981cf-103">Data factory의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="981cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="981cf-104">SYNTAX</span></span>

### <span data-ttu-id="981cf-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="981cf-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="981cf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="981cf-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="981cf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="981cf-107">DESCRIPTION</span></span>
<span data-ttu-id="981cf-108">**AzureRmDataFactoryV2Trigger** cmdlet은 data factory의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="981cf-109">트리거의 이름을 지정 하는 경우 cmdlet은 해당 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="981cf-110">이름을 지정 하지 않으면 cmdlet은 data factory의 모든 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="981cf-111">예제의</span><span class="sxs-lookup"><span data-stu-id="981cf-111">EXAMPLES</span></span>

### <span data-ttu-id="981cf-112">예제 1: 특정 트리거에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="981cf-112">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="981cf-113">Data factory "WikiADF"에서 생성 된 모든 트리거의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="981cf-114">예제 2: 모든 트리거에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="981cf-114">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="981cf-115">"WikiADF" 데이터 팩터리에 "ScheduledTrigger" 라는 단일 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="981cf-116">변수</span><span class="sxs-lookup"><span data-stu-id="981cf-116">PARAMETERS</span></span>

### <span data-ttu-id="981cf-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="981cf-117">-DataFactory</span></span>
<span data-ttu-id="981cf-118">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-118">The data factory object.</span></span>

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

### <span data-ttu-id="981cf-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="981cf-119">-DataFactoryName</span></span>
<span data-ttu-id="981cf-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-120">The data factory name.</span></span>

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

### <span data-ttu-id="981cf-121">-이름</span><span class="sxs-lookup"><span data-stu-id="981cf-121">-Name</span></span>
<span data-ttu-id="981cf-122">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="981cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="981cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="981cf-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-124">The resource group name.</span></span>

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

### <span data-ttu-id="981cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981cf-125">-DefaultProfile</span></span>
<span data-ttu-id="981cf-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="981cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981cf-127">CommonParameters</span></span>
<span data-ttu-id="981cf-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981cf-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981cf-130">입력</span><span class="sxs-lookup"><span data-stu-id="981cf-130">INPUTS</span></span>

### <span data-ttu-id="981cf-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="981cf-131">System.String</span></span>
<span data-ttu-id="981cf-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="981cf-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="981cf-133">출력</span><span class="sxs-lookup"><span data-stu-id="981cf-133">OUTPUTS</span></span>

### <span data-ttu-id="981cf-134">DataFactoryV2 ' 1 [[Microsoft Azure. PSTrigger, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="981cf-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="981cf-135">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="981cf-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="981cf-136">상속자</span><span class="sxs-lookup"><span data-stu-id="981cf-136">NOTES</span></span>

## <span data-ttu-id="981cf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="981cf-137">RELATED LINKS</span></span>

[<span data-ttu-id="981cf-138">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="981cf-138">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="981cf-139">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="981cf-139">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="981cf-140">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="981cf-140">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="981cf-141">제거-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="981cf-141">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
