---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 62b0a959e632c3e54b07e9238ae4ea9034a7408b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696726"
---
# <span data-ttu-id="1998d-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="1998d-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="1998d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1998d-102">SYNOPSIS</span></span>
<span data-ttu-id="1998d-103">공유 구독에서 동기화 실행에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1998d-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="1998d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1998d-104">SYNTAX</span></span>

### <span data-ttu-id="1998d-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1998d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1998d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1998d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1998d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1998d-107">DESCRIPTION</span></span>
<span data-ttu-id="1998d-108">**AzDataShareSubscriptionSynchronization** cmdlet은 소비자의 데이터 공유 계정에서 공유 구독의 모든 동기화 실행에 대 한 informaiton을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1998d-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="1998d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1998d-109">EXAMPLES</span></span>

### <span data-ttu-id="1998d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1998d-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="1998d-111">이 명령은 data share 계정 WikiAds에서 공유 구독 AdsShareSubscription에 대 한 모든 동기화 실행에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1998d-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="1998d-112">변수</span><span class="sxs-lookup"><span data-stu-id="1998d-112">PARAMETERS</span></span>

### <span data-ttu-id="1998d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1998d-113">-AccountName</span></span>
<span data-ttu-id="1998d-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="1998d-114">Azure data share account name</span></span>

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

### <span data-ttu-id="1998d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1998d-115">-DefaultProfile</span></span>
<span data-ttu-id="1998d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1998d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1998d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1998d-117">-ResourceGroupName</span></span>
<span data-ttu-id="1998d-118">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1998d-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1998d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1998d-119">-ResourceId</span></span>
<span data-ttu-id="1998d-120">Azure data share 구독 리소스 id</span><span class="sxs-lookup"><span data-stu-id="1998d-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="1998d-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1998d-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="1998d-122">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="1998d-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="1998d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1998d-123">CommonParameters</span></span>
<span data-ttu-id="1998d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1998d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1998d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1998d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1998d-126">입력</span><span class="sxs-lookup"><span data-stu-id="1998d-126">INPUTS</span></span>

### <span data-ttu-id="1998d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1998d-127">System.String</span></span>

## <span data-ttu-id="1998d-128">출력</span><span class="sxs-lookup"><span data-stu-id="1998d-128">OUTPUTS</span></span>

### <span data-ttu-id="1998d-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="1998d-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="1998d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1998d-130">NOTES</span></span>

## <span data-ttu-id="1998d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1998d-131">RELATED LINKS</span></span>
