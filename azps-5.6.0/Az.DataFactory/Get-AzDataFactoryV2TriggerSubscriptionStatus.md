---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: a83028b47d487f4bbb2732497d7e9eefd01882ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975115"
---
# <span data-ttu-id="982a4-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="982a4-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="982a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="982a4-102">SYNOPSIS</span></span>
<span data-ttu-id="982a4-103">지정된 외부 서비스 이벤트에 대한 이벤트 트리거에 대한 구독 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="982a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="982a4-104">SYNTAX</span></span>

### <span data-ttu-id="982a4-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="982a4-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="982a4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="982a4-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="982a4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="982a4-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="982a4-108">설명</span><span class="sxs-lookup"><span data-stu-id="982a4-108">DESCRIPTION</span></span>
<span data-ttu-id="982a4-109">이 명령은 지정된 외부 서비스 이벤트에 대한 이벤트 트리거에 대한 구독 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="982a4-110">반환된 상태가 "사용"으로 설정될 때까지 트리거를 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="982a4-111">예제</span><span class="sxs-lookup"><span data-stu-id="982a4-111">EXAMPLES</span></span>

### <span data-ttu-id="982a4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="982a4-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="982a4-113">이 명령은 BlobEnetTrigger1 트리거에 대한 하위 구성의 상태를 외부 서비스 이벤트에 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="982a4-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="982a4-114">PARAMETERS</span></span>

### <span data-ttu-id="982a4-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="982a4-115">-DataFactoryName</span></span>
<span data-ttu-id="982a4-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-116">The data factory name.</span></span>

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

### <span data-ttu-id="982a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982a4-117">-DefaultProfile</span></span>
<span data-ttu-id="982a4-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="982a4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="982a4-119">-InputObject</span></span>
<span data-ttu-id="982a4-120">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-120">The trigger object.</span></span>

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

### <span data-ttu-id="982a4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="982a4-121">-Name</span></span>
<span data-ttu-id="982a4-122">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-122">The trigger name.</span></span>

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

### <span data-ttu-id="982a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="982a4-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-124">The resource group name.</span></span>

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

### <span data-ttu-id="982a4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="982a4-125">-ResourceId</span></span>
<span data-ttu-id="982a4-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="982a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982a4-127">CommonParameters</span></span>
<span data-ttu-id="982a4-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="982a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982a4-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="982a4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982a4-130">입력</span><span class="sxs-lookup"><span data-stu-id="982a4-130">INPUTS</span></span>

### <span data-ttu-id="982a4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="982a4-131">System.String</span></span>
<span data-ttu-id="982a4-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="982a4-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="982a4-133">출력</span><span class="sxs-lookup"><span data-stu-id="982a4-133">OUTPUTS</span></span>

### <span data-ttu-id="982a4-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="982a4-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="982a4-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="982a4-135">NOTES</span></span>

## <span data-ttu-id="982a4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="982a4-136">RELATED LINKS</span></span>

