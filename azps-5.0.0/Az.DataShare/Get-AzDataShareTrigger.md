---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305228"
---
# <span data-ttu-id="cca0c-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="cca0c-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="cca0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca0c-102">SYNOPSIS</span></span>
<span data-ttu-id="cca0c-103">공유 구독의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cca0c-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="cca0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cca0c-104">SYNTAX</span></span>

### <span data-ttu-id="cca0c-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cca0c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cca0c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cca0c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca0c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cca0c-107">DESCRIPTION</span></span>
<span data-ttu-id="cca0c-108">**AzDataShareTrigger** cmdlet은 데이터 공유 계정에서 공유 구독의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cca0c-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="cca0c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cca0c-109">EXAMPLES</span></span>

### <span data-ttu-id="cca0c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cca0c-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="cca0c-111">이 명령은 data 공유 계정 WikiAds 아래에서 구독 공유 AdsShareSubscription에 대 한 트리거 AdsTrigger에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cca0c-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="cca0c-112">변수</span><span class="sxs-lookup"><span data-stu-id="cca0c-112">PARAMETERS</span></span>

### <span data-ttu-id="cca0c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cca0c-113">-AccountName</span></span>
<span data-ttu-id="cca0c-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="cca0c-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca0c-115">-DefaultProfile</span></span>
<span data-ttu-id="cca0c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cca0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca0c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="cca0c-117">-Name</span></span>
<span data-ttu-id="cca0c-118">Azure data share 트리거 이름</span><span class="sxs-lookup"><span data-stu-id="cca0c-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca0c-119">-ResourceGroupName</span></span>
<span data-ttu-id="cca0c-120">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cca0c-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca0c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cca0c-121">-ResourceId</span></span>
<span data-ttu-id="cca0c-122">트리거의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cca0c-122">The resource id of the trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cca0c-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cca0c-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="cca0c-124">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="cca0c-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca0c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca0c-125">CommonParameters</span></span>
<span data-ttu-id="cca0c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca0c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca0c-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cca0c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca0c-128">입력</span><span class="sxs-lookup"><span data-stu-id="cca0c-128">INPUTS</span></span>

### <span data-ttu-id="cca0c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cca0c-129">System.String</span></span>

## <span data-ttu-id="cca0c-130">출력</span><span class="sxs-lookup"><span data-stu-id="cca0c-130">OUTPUTS</span></span>

### <span data-ttu-id="cca0c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="cca0c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="cca0c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="cca0c-132">NOTES</span></span>

## <span data-ttu-id="cca0c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cca0c-133">RELATED LINKS</span></span>
