---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: dfe0710be411f3739a888cd58d3c0a6ec5353cab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696724"
---
# <span data-ttu-id="e7e53-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="e7e53-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="e7e53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7e53-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e53-103">공유 구독에 대 한 동기화 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7e53-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="e7e53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7e53-104">SYNTAX</span></span>

### <span data-ttu-id="e7e53-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7e53-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7e53-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7e53-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e53-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e7e53-107">DESCRIPTION</span></span>
<span data-ttu-id="e7e53-108">**AzDataShareSubscriptionSynchronizationDetail** cmdlet은 공유 구독에 대해 시작 된 동기화에 대 한 세부 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e53-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="e7e53-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e7e53-109">EXAMPLES</span></span>

### <span data-ttu-id="e7e53-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7e53-110">Example 1</span></span>
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

<span data-ttu-id="e7e53-111">이 명령은 data 공유 계정 WikiAds에서 구독 공유 AdsShareSubscription 동기화 시작에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e53-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="e7e53-112">변수</span><span class="sxs-lookup"><span data-stu-id="e7e53-112">PARAMETERS</span></span>

### <span data-ttu-id="e7e53-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7e53-113">-AccountName</span></span>
<span data-ttu-id="e7e53-114">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="e7e53-114">Azure data share account name</span></span>

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

### <span data-ttu-id="e7e53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e53-115">-DefaultProfile</span></span>
<span data-ttu-id="e7e53-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7e53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7e53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e53-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7e53-118">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e7e53-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e7e53-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7e53-119">-ResourceId</span></span>
<span data-ttu-id="e7e53-120">Azure data share 구독 리소스 id</span><span class="sxs-lookup"><span data-stu-id="e7e53-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="e7e53-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e7e53-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="e7e53-122">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="e7e53-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="e7e53-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="e7e53-123">-SynchronizationId</span></span>
<span data-ttu-id="e7e53-124">공유 구독 동기화의 동기화 id</span><span class="sxs-lookup"><span data-stu-id="e7e53-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="e7e53-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e53-125">CommonParameters</span></span>
<span data-ttu-id="e7e53-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e53-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e53-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7e53-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e53-128">입력</span><span class="sxs-lookup"><span data-stu-id="e7e53-128">INPUTS</span></span>

### <span data-ttu-id="e7e53-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e7e53-129">System.String</span></span>

## <span data-ttu-id="e7e53-130">출력</span><span class="sxs-lookup"><span data-stu-id="e7e53-130">OUTPUTS</span></span>

### <span data-ttu-id="e7e53-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="e7e53-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="e7e53-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e7e53-132">NOTES</span></span>

## <span data-ttu-id="e7e53-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7e53-133">RELATED LINKS</span></span>
