---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194601"
---
# <span data-ttu-id="ec764-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="ec764-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="ec764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec764-102">SYNOPSIS</span></span>
<span data-ttu-id="ec764-103">공유 구독에 대한 동기화 세부 정보에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec764-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="ec764-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec764-104">SYNTAX</span></span>

### <span data-ttu-id="ec764-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec764-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec764-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec764-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec764-107">설명</span><span class="sxs-lookup"><span data-stu-id="ec764-107">DESCRIPTION</span></span>
<span data-ttu-id="ec764-108">**Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet은 공유 구독에 대해 시작된 동기화의 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ec764-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="ec764-109">예제</span><span class="sxs-lookup"><span data-stu-id="ec764-109">EXAMPLES</span></span>

### <span data-ttu-id="ec764-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec764-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="ec764-111">이 명령은 데이터 공유 계정 WikiAds에서 공유 구독 AdsShareSubscription에 대해 시작된 동기화에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ec764-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="ec764-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec764-112">PARAMETERS</span></span>

### <span data-ttu-id="ec764-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec764-113">-AccountName</span></span>
<span data-ttu-id="ec764-114">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="ec764-114">Azure data share account name</span></span>

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

### <span data-ttu-id="ec764-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec764-115">-DefaultProfile</span></span>
<span data-ttu-id="ec764-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec764-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec764-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec764-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec764-118">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ec764-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ec764-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec764-119">-ResourceId</span></span>
<span data-ttu-id="ec764-120">Azure 데이터 공유 구독 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ec764-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="ec764-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ec764-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="ec764-122">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="ec764-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ec764-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="ec764-123">-SynchronizationId</span></span>
<span data-ttu-id="ec764-124">공유 구독 동기화의 동기화 ID</span><span class="sxs-lookup"><span data-stu-id="ec764-124">Synchronization id of share subscription synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec764-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec764-125">CommonParameters</span></span>
<span data-ttu-id="ec764-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec764-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec764-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec764-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec764-128">입력</span><span class="sxs-lookup"><span data-stu-id="ec764-128">INPUTS</span></span>

### <span data-ttu-id="ec764-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ec764-129">System.String</span></span>

## <span data-ttu-id="ec764-130">출력</span><span class="sxs-lookup"><span data-stu-id="ec764-130">OUTPUTS</span></span>

### <span data-ttu-id="ec764-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="ec764-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="ec764-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec764-132">NOTES</span></span>

## <span data-ttu-id="ec764-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec764-133">RELATED LINKS</span></span>
