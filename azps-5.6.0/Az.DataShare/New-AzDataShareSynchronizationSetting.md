---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 5632aed8c1b3dde653be65fd587be5f1adf9cbbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996697"
---
# <span data-ttu-id="a2134-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="a2134-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="a2134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2134-102">SYNOPSIS</span></span>
<span data-ttu-id="a2134-103">공유에 대한 동기화 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="a2134-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2134-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2134-105">설명</span><span class="sxs-lookup"><span data-stu-id="a2134-105">DESCRIPTION</span></span>
<span data-ttu-id="a2134-106">**New-AzDataShareSynchronizationSetting은** 특정 시간의 반복 간격에 대해 공유 계정에서 공유에 대한 동기화 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="a2134-107">예제</span><span class="sxs-lookup"><span data-stu-id="a2134-107">EXAMPLES</span></span>

### <span data-ttu-id="a2134-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2134-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="a2134-109">이 명령은 데이터 공유 계정 WikiAds에서 Share AdsShare를 위해 매일 오전 9:00에 매일 반복 간격에 동기화 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="a2134-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2134-110">PARAMETERS</span></span>

### <span data-ttu-id="a2134-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2134-111">-AccountName</span></span>
<span data-ttu-id="a2134-112">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="a2134-112">Azure data share account name</span></span>

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

### <span data-ttu-id="a2134-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2134-113">-DefaultProfile</span></span>
<span data-ttu-id="a2134-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2134-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a2134-115">-Name</span></span>
<span data-ttu-id="a2134-116">동기화 설정 이름</span><span class="sxs-lookup"><span data-stu-id="a2134-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="a2134-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="a2134-117">-RecurrenceInterval</span></span>
<span data-ttu-id="a2134-118">동기화 설정의 반복 간격(일 또는 시간)</span><span class="sxs-lookup"><span data-stu-id="a2134-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="a2134-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2134-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2134-120">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a2134-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="a2134-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a2134-121">-ShareName</span></span>
<span data-ttu-id="a2134-122">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="a2134-122">Azure data share name</span></span>

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

### <span data-ttu-id="a2134-123">-동기화타임</span><span class="sxs-lookup"><span data-stu-id="a2134-123">-SynchronizationTime</span></span>
<span data-ttu-id="a2134-124">예약된 동기화 설정의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="a2134-124">The start time of the scheduled synchronization setting</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2134-125">-확인</span><span class="sxs-lookup"><span data-stu-id="a2134-125">-Confirm</span></span>
<span data-ttu-id="a2134-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2134-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2134-127">-WhatIf</span></span>
<span data-ttu-id="a2134-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2134-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2134-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2134-130">CommonParameters</span></span>
<span data-ttu-id="a2134-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2134-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2134-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2134-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2134-133">입력</span><span class="sxs-lookup"><span data-stu-id="a2134-133">INPUTS</span></span>

### <span data-ttu-id="a2134-134">없음</span><span class="sxs-lookup"><span data-stu-id="a2134-134">None</span></span>

## <span data-ttu-id="a2134-135">출력</span><span class="sxs-lookup"><span data-stu-id="a2134-135">OUTPUTS</span></span>

### <span data-ttu-id="a2134-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="a2134-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="a2134-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2134-137">NOTES</span></span>

## <span data-ttu-id="a2134-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2134-138">RELATED LINKS</span></span>
