---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: d7f6429ebc3e8a3ebf1f8dd2749e6b7f66005ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041830"
---
# <span data-ttu-id="9de84-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="9de84-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="9de84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de84-102">SYNOPSIS</span></span>
<span data-ttu-id="9de84-103">공유에 대 한 동기화 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="9de84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9de84-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de84-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9de84-105">DESCRIPTION</span></span>
<span data-ttu-id="9de84-106">**AzDataShareSynchronizationSetting** 는 특정 시간에 매일 또는 매시간 되풀이 간격으로 공유 계정에서 공유에 대 한 동기화 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="9de84-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9de84-107">EXAMPLES</span></span>

### <span data-ttu-id="9de84-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9de84-108">Example 1</span></span>
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

<span data-ttu-id="9de84-109">이 명령은 9:00 오전 데이터 공유 계정 WikiAds에서 공유에 대 한 매일 되풀이 간격에 대 한 동기화 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="9de84-110">변수</span><span class="sxs-lookup"><span data-stu-id="9de84-110">PARAMETERS</span></span>

### <span data-ttu-id="9de84-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9de84-111">-AccountName</span></span>
<span data-ttu-id="9de84-112">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="9de84-112">Azure data share account name</span></span>

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

### <span data-ttu-id="9de84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de84-113">-DefaultProfile</span></span>
<span data-ttu-id="9de84-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de84-115">-이름</span><span class="sxs-lookup"><span data-stu-id="9de84-115">-Name</span></span>
<span data-ttu-id="9de84-116">동기화 설정 이름</span><span class="sxs-lookup"><span data-stu-id="9de84-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="9de84-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="9de84-117">-RecurrenceInterval</span></span>
<span data-ttu-id="9de84-118">동기화 설정의 되풀이 간격 (일 또는 시간)</span><span class="sxs-lookup"><span data-stu-id="9de84-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="9de84-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de84-119">-ResourceGroupName</span></span>
<span data-ttu-id="9de84-120">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9de84-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="9de84-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9de84-121">-ShareName</span></span>
<span data-ttu-id="9de84-122">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="9de84-122">Azure data share name</span></span>

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

### <span data-ttu-id="9de84-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="9de84-123">-SynchronizationTime</span></span>
<span data-ttu-id="9de84-124">예약 된 동기화 설정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="9de84-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="9de84-125">-확인</span><span class="sxs-lookup"><span data-stu-id="9de84-125">-Confirm</span></span>
<span data-ttu-id="9de84-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de84-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de84-127">-WhatIf</span></span>
<span data-ttu-id="9de84-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9de84-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de84-130">CommonParameters</span></span>
<span data-ttu-id="9de84-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de84-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de84-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de84-133">입력</span><span class="sxs-lookup"><span data-stu-id="9de84-133">INPUTS</span></span>

### <span data-ttu-id="9de84-134">않아야</span><span class="sxs-lookup"><span data-stu-id="9de84-134">None</span></span>

## <span data-ttu-id="9de84-135">출력</span><span class="sxs-lookup"><span data-stu-id="9de84-135">OUTPUTS</span></span>

### <span data-ttu-id="9de84-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="9de84-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="9de84-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9de84-137">NOTES</span></span>

## <span data-ttu-id="9de84-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9de84-138">RELATED LINKS</span></span>
