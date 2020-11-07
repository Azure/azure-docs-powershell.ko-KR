---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: 45a2adc34322d80d5b9d103a99e26c9e2638c9af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689313"
---
# <span data-ttu-id="961ce-101">Get-AzLog</span><span class="sxs-lookup"><span data-stu-id="961ce-101">Get-AzLog</span></span>

## <span data-ttu-id="961ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="961ce-102">SYNOPSIS</span></span>
<span data-ttu-id="961ce-103">이벤트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-103">Gets a log of events.</span></span>

## <span data-ttu-id="961ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="961ce-104">SYNTAX</span></span>

### <span data-ttu-id="961ce-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="961ce-105">GetByCorrelationId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="961ce-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="961ce-106">GetByResourceId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="961ce-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="961ce-107">GetByResourceGroup</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="961ce-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="961ce-108">GetByResourceProvider</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="961ce-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="961ce-109">GetBySubscription</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="961ce-110">설명은</span><span class="sxs-lookup"><span data-stu-id="961ce-110">DESCRIPTION</span></span>
<span data-ttu-id="961ce-111">**Get-AzLog** cmdlet은 이벤트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-111">The **Get-AzLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="961ce-112">이벤트는 현재 구독 ID, 상관 관계 ID, 리소스 그룹, 리소스 ID 또는 리소스 공급자와 연결 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="961ce-113">예제의</span><span class="sxs-lookup"><span data-stu-id="961ce-113">EXAMPLES</span></span>

### <span data-ttu-id="961ce-114">예제 1: 구독 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzLog
```

<span data-ttu-id="961ce-115">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 사용자의 구독 ID와 연결 된 최대 1000 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-116">예제 2: 최대 개수의 이벤트를 사용 하 여 구독 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -MaxRecord 100
```

<span data-ttu-id="961ce-117">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 사용자의 구독 ID와 연결 된 최대 100 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-118">예제 3: 시작 시간으로 구독 ID를 사용 하 여 이벤트 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="961ce-119">이 명령은 2017 년 6 월에 발생 한 사용자의 구독 ID와 연결 된 최대 1000 이벤트를 나열 합니다. 해당 날짜/시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우 30 개의 현지 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-120">예제 4: 시작 시간 및 종료 시간을 사용 하 여 구독 ID를 기준으로 이벤트 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="961ce-121">이 명령은 2017 년 4 월에 발생 한 사용자의 구독 ID와 연결 된 이벤트 (최대 1000, 현지 시간 30 개, 2017 년 4 월 1 일 이전)를 나열 합니다. 전체 날짜/시간 범위가 현재 날짜/시간 (예: 보존 기간)에서 90 일 보다 오래 된 경우에는 30 현지 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="961ce-122">예제 5: 상관 관계 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="961ce-123">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="961ce-124">**참고** :이는 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="961ce-125">예제 6: 최대 이벤트 수를 사용 하 여 상관 관계 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="961ce-126">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 상관 관계 ID와 연결 된 최대 100 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="961ce-127">**참고** :이는 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="961ce-128">예제 7: 상관 관계 ID 및 시작 시간을 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="961ce-129">이 명령은 2017 년에 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트를 나열 합니다. 시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우-05-22T04:30:00 현지 시간.</span><span class="sxs-lookup"><span data-stu-id="961ce-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="961ce-130">**참고** :이는 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="961ce-131">예제 8: 시작 시간과 종료 시간을 사용 하 여 상관 관계 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="961ce-132">이 명령은 2017 년 4 월에 발생 한 지정 된 상관 관계 ID와 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 현지 시간을 보존 기간 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="961ce-133">예제 9: 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="961ce-134">이 명령은 1000에서 현재 날짜/시간 으로부터 7 일 동안 지정 된 리소스 그룹과 연결 된 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-135">예제 10: 최대 이벤트 수를 사용 하 여 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="961ce-136">이 명령은 현재 날짜/시간 으로부터 7 일 동안 지정 된 리소스 그룹과 연결 된 100 이벤트를 모두 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-137">예제 11: 시작 시간별로 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="961ce-138">이 명령은 2017 년에 발생 한 특정 리소스 그룹과 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-139">예제 12: 시작 시간 및 종료 시간을 사용 하 여 리소스 그룹에 대 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="961ce-140">이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 그룹과 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 로컬 시간 (즉, 보존 기간)</span><span class="sxs-lookup"><span data-stu-id="961ce-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="961ce-141">예제 13: 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="961ce-142">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 ID와 연결 된 최대 1000 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-143">예제 14: 최대 이벤트 수를 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="961ce-144">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 ID와 연결 된 최대 100 이벤트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-145">예제 15: 시작 시간을 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="961ce-146">이 명령은 2017 년에 발생 한 특정 리소스 ID와 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-147">예제 16: 시작 시간 및 종료 시간을 사용 하 여 리소스 ID를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="961ce-148">이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 ID와 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하 고 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일이 하 인 경우: 30 현지 시간을 보존 기간 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="961ce-149">예제 17: 리소스 공급자를 기준으로 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="961ce-150">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 공급자와 연결 된 1000 이벤트를 모두 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-151">예제 18: 최대 이벤트 수를 사용 하 여 리소스 공급자에 의해 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="961ce-152">이 명령은 현재 날짜/시간에서 7 일 동안 발생 한 지정 된 리소스 공급자와 연결 된 100 이벤트를 모두 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-153">예제 19: 시작 시간을 사용 하 여 리소스 공급자에의 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="961ce-154">이 명령은 2017 년에 발생 한 특정 리소스 공급자와 연결 된 최대 1000 이벤트 (시작 시간이 현재 날짜/시간에서 90 일 보다 오래 된 경우)를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="961ce-155">예제 20: 시작 시간 및 종료 시간을 사용 하 여 리소스 공급자에의 한 이벤트 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="961ce-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="961ce-156">이 명령은 2017 년 4 월에 발생 한 지정 된 리소스 공급자에 연결 된 최대 1000 이벤트 (예: 30 현지 시간)를 나열 하지만 2017-04-25T12: 전체 날짜/시간 범위가 현재 날짜/시간에서 90 일 보다 오래 된 경우: 30 현지 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="961ce-157">변수</span><span class="sxs-lookup"><span data-stu-id="961ce-157">PARAMETERS</span></span>

### <span data-ttu-id="961ce-158">-발신자</span><span class="sxs-lookup"><span data-stu-id="961ce-158">-Caller</span></span>
<span data-ttu-id="961ce-159">발신자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="961ce-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="961ce-160">-CorrelationId</span></span>
<span data-ttu-id="961ce-161">상관 관계 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="961ce-162">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-162">This parameter is required.</span></span>

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

### <span data-ttu-id="961ce-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="961ce-163">-DefaultProfile</span></span>
<span data-ttu-id="961ce-164">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="961ce-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="961ce-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="961ce-165">-DetailedOutput</span></span>
<span data-ttu-id="961ce-166">이 cmdlet에 자세한 출력이 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="961ce-167">기본적으로 출력이 요약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961ce-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="961ce-168">-EndTime</span></span>
<span data-ttu-id="961ce-169">현지 시간으로 쿼리의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="961ce-170">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-170">The default value is the current time.</span></span>
<span data-ttu-id="961ce-171">값은 *StartTime* 보다 이후 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="961ce-172">Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961ce-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="961ce-173">-MaxRecord</span></span>
<span data-ttu-id="961ce-174">지정 된 필터에 대해 반입할 총 레코드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="961ce-175">기본값은 1000이 고 최대 허용 값은 10만입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="961ce-176">음수 값과 0은 무시 되 고 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961ce-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="961ce-177">-ResourceGroupName</span></span>
<span data-ttu-id="961ce-178">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="961ce-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="961ce-179">-ResourceId</span></span>
<span data-ttu-id="961ce-180">리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="961ce-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="961ce-181">-ResourceProvider</span></span>
<span data-ttu-id="961ce-182">리소스 공급자별 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="961ce-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="961ce-183">-StartTime</span></span>
<span data-ttu-id="961ce-184">현지 시간으로 쿼리의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="961ce-185">기본값은 *EndTime* 에서 7 일을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="961ce-186">Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961ce-187">-상태</span><span class="sxs-lookup"><span data-stu-id="961ce-187">-Status</span></span>
<span data-ttu-id="961ce-188">상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-188">Specifies the status.</span></span>

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

### <span data-ttu-id="961ce-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="961ce-189">CommonParameters</span></span>
<span data-ttu-id="961ce-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="961ce-191">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="961ce-191">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="961ce-192">입력</span><span class="sxs-lookup"><span data-stu-id="961ce-192">INPUTS</span></span>

### <span data-ttu-id="961ce-193">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="961ce-193">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="961ce-194">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="961ce-194">System.String</span></span>

### <span data-ttu-id="961ce-195">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="961ce-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="961ce-196">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="961ce-196">System.Int32</span></span>

## <span data-ttu-id="961ce-197">출력</span><span class="sxs-lookup"><span data-stu-id="961ce-197">OUTPUTS</span></span>

### <span data-ttu-id="961ce-198">PSEventData를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="961ce-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="961ce-199">상속자</span><span class="sxs-lookup"><span data-stu-id="961ce-199">NOTES</span></span>

## <span data-ttu-id="961ce-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="961ce-200">RELATED LINKS</span></span>