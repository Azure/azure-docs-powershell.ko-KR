---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212847"
---
# <span data-ttu-id="6bfbe-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="6bfbe-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="6bfbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfbe-103">지정 된 외부 서비스 이벤트에 대 한 이벤트 트리거의 구독 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="6bfbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6bfbe-104">SYNTAX</span></span>

### <span data-ttu-id="6bfbe-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6bfbe-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bfbe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6bfbe-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bfbe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bfbe-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bfbe-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6bfbe-108">DESCRIPTION</span></span>
<span data-ttu-id="6bfbe-109">이 명령은 지정 된 외부 서비스 이벤트에 대 한 이벤트 트리거의 구독 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="6bfbe-110">반환 된 상태가 "사용"이 될 때까지 트리거를 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="6bfbe-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6bfbe-111">EXAMPLES</span></span>

### <span data-ttu-id="6bfbe-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6bfbe-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="6bfbe-113">이 명령은 외부 서비스 이벤트에 대 한 BlobEnetTrigger1 트리거의 subscribtion 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="6bfbe-114">변수</span><span class="sxs-lookup"><span data-stu-id="6bfbe-114">PARAMETERS</span></span>

### <span data-ttu-id="6bfbe-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6bfbe-115">-DataFactoryName</span></span>
<span data-ttu-id="6bfbe-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-116">The data factory name.</span></span>

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

### <span data-ttu-id="6bfbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfbe-117">-DefaultProfile</span></span>
<span data-ttu-id="6bfbe-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bfbe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bfbe-119">-InputObject</span></span>
<span data-ttu-id="6bfbe-120">트리거 개체</span><span class="sxs-lookup"><span data-stu-id="6bfbe-120">The trigger object.</span></span>

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

### <span data-ttu-id="6bfbe-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6bfbe-121">-Name</span></span>
<span data-ttu-id="6bfbe-122">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-122">The trigger name.</span></span>

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

### <span data-ttu-id="6bfbe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bfbe-123">-ResourceGroupName</span></span>
<span data-ttu-id="6bfbe-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-124">The resource group name.</span></span>

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

### <span data-ttu-id="6bfbe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bfbe-125">-ResourceId</span></span>
<span data-ttu-id="6bfbe-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6bfbe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfbe-127">CommonParameters</span></span>
<span data-ttu-id="6bfbe-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfbe-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bfbe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfbe-130">입력</span><span class="sxs-lookup"><span data-stu-id="6bfbe-130">INPUTS</span></span>

### <span data-ttu-id="6bfbe-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6bfbe-131">System.String</span></span>
<span data-ttu-id="6bfbe-132">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="6bfbe-133">출력</span><span class="sxs-lookup"><span data-stu-id="6bfbe-133">OUTPUTS</span></span>

### <span data-ttu-id="6bfbe-134">DataFactoryV2. PSTriggerSubscriptionStatus/.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="6bfbe-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6bfbe-135">NOTES</span></span>

## <span data-ttu-id="6bfbe-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bfbe-136">RELATED LINKS</span></span>

