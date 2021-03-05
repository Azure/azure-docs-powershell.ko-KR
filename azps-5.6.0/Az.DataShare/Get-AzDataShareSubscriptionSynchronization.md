---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 8a80277508f9cd2998668185af6a8c0b5bbec128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962283"
---
# <span data-ttu-id="38bd3-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="38bd3-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="38bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="38bd3-103">공유 구독에서 동기화 실행에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="38bd3-104">구문</span><span class="sxs-lookup"><span data-stu-id="38bd3-104">SYNTAX</span></span>

### <span data-ttu-id="38bd3-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="38bd3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38bd3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bd3-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38bd3-107">설명</span><span class="sxs-lookup"><span data-stu-id="38bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="38bd3-108">**Get-AzDataShareSubscriptionSynchronization** cmdlet은 소비자의 데이터 공유 계정에서 공유 구독에서 실행되는 모든 동기화에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="38bd3-109">예제</span><span class="sxs-lookup"><span data-stu-id="38bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="38bd3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="38bd3-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="38bd3-111">이 명령은 데이터 공유 계정 WikiAds에서 공유 구독 AdsShareSubscription에 대한 모든 동기화 실행에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="38bd3-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="38bd3-112">PARAMETERS</span></span>

### <span data-ttu-id="38bd3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="38bd3-113">-AccountName</span></span>
<span data-ttu-id="38bd3-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="38bd3-114">Azure data share account name</span></span>

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

### <span data-ttu-id="38bd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bd3-115">-DefaultProfile</span></span>
<span data-ttu-id="38bd3-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bd3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bd3-117">-ResourceGroupName</span></span>
<span data-ttu-id="38bd3-118">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="38bd3-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="38bd3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38bd3-119">-ResourceId</span></span>
<span data-ttu-id="38bd3-120">Azure 데이터 공유 구독 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="38bd3-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="38bd3-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="38bd3-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="38bd3-122">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="38bd3-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="38bd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bd3-123">CommonParameters</span></span>
<span data-ttu-id="38bd3-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bd3-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38bd3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bd3-126">입력</span><span class="sxs-lookup"><span data-stu-id="38bd3-126">INPUTS</span></span>

### <span data-ttu-id="38bd3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="38bd3-127">System.String</span></span>

## <span data-ttu-id="38bd3-128">출력</span><span class="sxs-lookup"><span data-stu-id="38bd3-128">OUTPUTS</span></span>

### <span data-ttu-id="38bd3-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="38bd3-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="38bd3-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38bd3-130">NOTES</span></span>

## <span data-ttu-id="38bd3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38bd3-131">RELATED LINKS</span></span>
