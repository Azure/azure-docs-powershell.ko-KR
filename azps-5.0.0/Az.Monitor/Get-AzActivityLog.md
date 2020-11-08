---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218612"
---
# <span data-ttu-id="0abd3-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="0abd3-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="0abd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0abd3-102">SYNOPSIS</span></span>
<span data-ttu-id="0abd3-103">활동 로그 이벤트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="0abd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0abd3-104">SYNTAX</span></span>

### <span data-ttu-id="0abd3-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="0abd3-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0abd3-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0abd3-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0abd3-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0abd3-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0abd3-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0abd3-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0abd3-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="0abd3-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0abd3-110">설명은</span><span class="sxs-lookup"><span data-stu-id="0abd3-110">DESCRIPTION</span></span>
<span data-ttu-id="0abd3-111">Get-AzActivityLog cmdlet은 활동 로그 이벤트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="0abd3-112">이벤트는 현재 구독 ID, 상관 관계 ID, 리소스 그룹, 리소스 ID 또는 리소스 공급자와 연결 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="0abd3-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0abd3-113">EXAMPLES</span></span>

### <span data-ttu-id="0abd3-114">예제 1: 구독 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="0abd3-115">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 사용자의 구독 ID와 연결 된 최대 1000 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-116">예제 2: 최대 개수의 이벤트를 사용 하 여 구독 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="0abd3-117">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 사용자의 구독 ID와 연결 된 최대 100 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-118">예제 3: 시작 시간으로 구독 ID를 사용 하 여 이벤트 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="0abd3-119">이 명령은 2017 년 6 월에 발생 한 사용자의 구독 ID와 연결 된 최대 1000 이벤트를 나열 합니다. 해당 날짜/시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우 30 개의 현지 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-120">예제 4: 시작 시간 및 종료 시간을 사용 하 여 구독 ID를 기준으로 이벤트 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="0abd3-121">이 명령은 2017 년 4 월에 발생 한 사용자의 구독 ID와 연결 된 이벤트 (최대 1000, 현지 시간 30 개, 2017 년 4 월 1 일 이전)를 나열 합니다. 전체 날짜/시간 범위가 현재 날짜/시간 (예: 보존 기간)에서 90 일 보다 오래 된 경우에는 30 현지 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="0abd3-122">예제 5: 상관 관계 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="0abd3-123">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="0abd3-124">**참고** :이는 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="0abd3-125">예제 6: 최대 이벤트 수를 사용 하 여 상관 관계 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="0abd3-126">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 상관 관계 ID와 연결 된 최대 100 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="0abd3-127">**참고** :이는 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="0abd3-128">예제 7: 상관 관계 ID 및 시작 시간을 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="0abd3-129">이 명령은 2017 년에 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트를 나열 합니다. 시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우-05-22T04:30:00 현지 시간.</span><span class="sxs-lookup"><span data-stu-id="0abd3-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="0abd3-130">**참고** :이는 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="0abd3-131">예제 8: 시작 시간과 종료 시간을 사용 하 여 상관 관계 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="0abd3-132">이 명령은 2017 년 4 월에 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 현지 시간을 보존 기간 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="0abd3-133">예제 9: 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="0abd3-134">이 명령은 1000에서 현재 날짜/시간 으로부터 7 일 동안 지정 된 리소스 그룹과 연결 된 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-135">예제 10: 최대 이벤트 수를 사용 하 여 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="0abd3-136">이 명령은 현재 날짜/시간 으로부터 7 일 동안 지정 된 리소스 그룹과 연결 된 100 이벤트를 모두 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-137">예제 11: 시작 시간별로 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="0abd3-138">이 명령은 2017 년에 발생 한 특정 리소스 그룹과 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-139">예제 12: 시작 시간 및 종료 시간을 사용 하 여 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="0abd3-140">이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 그룹과 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 로컬 시간 (즉, 보존 기간)</span><span class="sxs-lookup"><span data-stu-id="0abd3-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="0abd3-141">예제 13: 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="0abd3-142">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 ID와 연결 된 최대 1000 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-143">예제 14: 최대 이벤트 수를 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="0abd3-144">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 ID와 연결 된 최대 100 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-145">예제 15: 시작 시간을 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="0abd3-146">이 명령은 2017 년에 발생 한 특정 리소스 ID와 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-147">예제 16: 시작 시간 및 종료 시간을 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="0abd3-148">이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 ID와 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일이 하 인 경우: 30 현지 시간을 보존 기간 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="0abd3-149">예제 17: 리소스 공급자를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="0abd3-150">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 공급자와 연결 된 1000 이벤트를 모두 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-151">예제 18: 최대 이벤트 수를 사용 하 여 리소스 공급자에 의해 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="0abd3-152">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 공급자와 연결 된 100 이벤트를 모두 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-153">예제 19: 시작 시간을 사용 하 여 리소스 공급자에의 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="0abd3-154">이 명령은 2017 년에 발생 한 특정 리소스 공급자와 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="0abd3-155">예제 20: 시작 시간 및 종료 시간을 사용 하 여 리소스 공급자에의 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="0abd3-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="0abd3-156">이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 공급자에 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하지만 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 현지 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="0abd3-157">변수</span><span class="sxs-lookup"><span data-stu-id="0abd3-157">PARAMETERS</span></span>

### <span data-ttu-id="0abd3-158">-발신자</span><span class="sxs-lookup"><span data-stu-id="0abd3-158">-Caller</span></span>
<span data-ttu-id="0abd3-159">가져올 이벤트의 호출자입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-159">The caller of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="0abd3-160">-CorrelationId</span></span>
<span data-ttu-id="0abd3-161">CorrelationId</span><span class="sxs-lookup"><span data-stu-id="0abd3-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abd3-162">-DefaultProfile</span></span>
<span data-ttu-id="0abd3-163">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0abd3-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="0abd3-164">-DetailedOutput</span></span>
<span data-ttu-id="0abd3-165">이벤트의 모든 세부 정보를 포함 하는 개체 반환 (기본값은 일부 특성만 반환 하는 것입니다 (예: 세부 정보 없음)</span><span class="sxs-lookup"><span data-stu-id="0abd3-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0abd3-166">-EndTime</span></span>
<span data-ttu-id="0abd3-167">쿼리 endTime</span><span class="sxs-lookup"><span data-stu-id="0abd3-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="0abd3-168">-MaxRecord</span></span>
<span data-ttu-id="0abd3-169">반입할 최대 레코드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="0abd3-170">별칭: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="0abd3-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abd3-171">-ResourceGroupName</span></span>
<span data-ttu-id="0abd3-172">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0abd3-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0abd3-173">-ResourceId</span></span>
<span data-ttu-id="0abd3-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0abd3-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0abd3-175">-ResourceProvider</span></span>
<span data-ttu-id="0abd3-176">ResourceProvider 이름</span><span class="sxs-lookup"><span data-stu-id="0abd3-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0abd3-177">-StartTime</span></span>
<span data-ttu-id="0abd3-178">쿼리의 correlationId</span><span class="sxs-lookup"><span data-stu-id="0abd3-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-179">-상태</span><span class="sxs-lookup"><span data-stu-id="0abd3-179">-Status</span></span>
<span data-ttu-id="0abd3-180">반입할 이벤트의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-180">The status of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd3-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abd3-181">CommonParameters</span></span>
<span data-ttu-id="0abd3-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abd3-183">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0abd3-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abd3-184">입력</span><span class="sxs-lookup"><span data-stu-id="0abd3-184">INPUTS</span></span>

### <span data-ttu-id="0abd3-185">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0abd3-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0abd3-186">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0abd3-186">System.String</span></span>

### <span data-ttu-id="0abd3-187">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0abd3-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0abd3-188">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="0abd3-188">System.Int32</span></span>

## <span data-ttu-id="0abd3-189">출력</span><span class="sxs-lookup"><span data-stu-id="0abd3-189">OUTPUTS</span></span>

### <span data-ttu-id="0abd3-190">PSEventData를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abd3-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="0abd3-191">상속자</span><span class="sxs-lookup"><span data-stu-id="0abd3-191">NOTES</span></span>

## <span data-ttu-id="0abd3-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0abd3-192">RELATED LINKS</span></span>
