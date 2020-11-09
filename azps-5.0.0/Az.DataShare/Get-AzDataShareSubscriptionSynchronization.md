---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305258"
---
# <span data-ttu-id="d94b1-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="d94b1-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="d94b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d94b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d94b1-103">공유 구독에서 동기화 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d94b1-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="d94b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d94b1-104">SYNTAX</span></span>

### <span data-ttu-id="d94b1-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d94b1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d94b1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d94b1-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d94b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d94b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d94b1-108">**AzDataShareSubscriptionSynchronization** cmdlet은 소비자의 데이터 공유 계정에서 공유 구독의 모든 동기화 실행에 대 한 informaiton을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d94b1-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="d94b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d94b1-109">EXAMPLES</span></span>

### <span data-ttu-id="d94b1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d94b1-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="d94b1-111">이 명령은 data share 계정 WikiAds에서 공유 구독 AdsShareSubscription에 대 한 모든 동기화 실행에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d94b1-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="d94b1-112">변수</span><span class="sxs-lookup"><span data-stu-id="d94b1-112">PARAMETERS</span></span>

### <span data-ttu-id="d94b1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d94b1-113">-AccountName</span></span>
<span data-ttu-id="d94b1-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="d94b1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d94b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94b1-115">-DefaultProfile</span></span>
<span data-ttu-id="d94b1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d94b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d94b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="d94b1-118">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d94b1-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d94b1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d94b1-119">-ResourceId</span></span>
<span data-ttu-id="d94b1-120">Azure data share 구독 리소스 id</span><span class="sxs-lookup"><span data-stu-id="d94b1-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="d94b1-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d94b1-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="d94b1-122">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="d94b1-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d94b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94b1-123">CommonParameters</span></span>
<span data-ttu-id="d94b1-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d94b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94b1-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d94b1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94b1-126">입력</span><span class="sxs-lookup"><span data-stu-id="d94b1-126">INPUTS</span></span>

### <span data-ttu-id="d94b1-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d94b1-127">System.String</span></span>

## <span data-ttu-id="d94b1-128">출력</span><span class="sxs-lookup"><span data-stu-id="d94b1-128">OUTPUTS</span></span>

### <span data-ttu-id="d94b1-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="d94b1-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="d94b1-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d94b1-130">NOTES</span></span>

## <span data-ttu-id="d94b1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d94b1-131">RELATED LINKS</span></span>
