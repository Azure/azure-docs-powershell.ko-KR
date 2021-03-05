---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980203"
---
# <span data-ttu-id="5a45f-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="5a45f-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="5a45f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a45f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a45f-103">활동 로그 이벤트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="5a45f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a45f-104">SYNTAX</span></span>

### <span data-ttu-id="5a45f-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="5a45f-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a45f-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a45f-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a45f-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a45f-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a45f-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5a45f-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a45f-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="5a45f-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a45f-110">설명</span><span class="sxs-lookup"><span data-stu-id="5a45f-110">DESCRIPTION</span></span>
<span data-ttu-id="5a45f-111">Get-AzActivityLog cmdlet은 활동 로그 이벤트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="5a45f-112">이벤트는 현재 구독 ID, 상관 관계 ID, 리소스 그룹, 리소스 ID 또는 리소스 공급자와 연결될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="5a45f-113">예제</span><span class="sxs-lookup"><span data-stu-id="5a45f-113">EXAMPLES</span></span>

### <span data-ttu-id="5a45f-114">예제 1: 구독 ID로 이벤트 로그를 하세요.</span><span class="sxs-lookup"><span data-stu-id="5a45f-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzActivityLog
```

<span data-ttu-id="5a45f-115">이 명령은 현재 날짜/시간으로부터 7일이 지난 사용자의 구독 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-116">예제 2: 최대 이벤트 수가 있는 구독 ID로 이벤트 로그를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="5a45f-117">이 명령은 현재 날짜/시간으로부터 7일 동안 진행된 사용자의 구독 ID와 연결된 대부분의 100개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-118">예제 3: 시작 시간을 사용하여 구독 ID로 이벤트 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="5a45f-119">이 명령은 해당 날짜/시간이 현재 날짜/시간보다 90일이 지난 경우 2017-06-01T10:30 로컬 시간 이후의 사용자 구독 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-120">예제 4: 시작 시간 및 종료 시간을 사용하여 구독 ID로 이벤트 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="5a45f-121">이 명령은 2017-04-01T10:30 로컬 시간 또는 2017-04-14T11:30 이전 날짜/시간 범위가 현재 날짜/시간의 90일보다 오래되지 않은 경우 사용자의 구독 ID와 연결된 이벤트의 대부분을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5a45f-122">예제 5: 상관 관계 ID로 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="5a45f-123">이 명령은 현재 날짜/시간에서 7일 동안 일어났습니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="5a45f-124">**참고**: 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="5a45f-125">예제 6: 최대 이벤트 수가 있는 상관 관계 ID로 이벤트 로그를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="5a45f-126">이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 상관 관계 ID와 연결된 100개 이벤트가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="5a45f-127">**참고**: 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="5a45f-128">예제 7: 상관 관계 ID로 이벤트 로그 및 시작 시간 확인</span><span class="sxs-lookup"><span data-stu-id="5a45f-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="5a45f-129">이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 상관 관계 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="5a45f-130">**참고**: 일반적으로 하나의 이벤트입니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="5a45f-131">예제 8: 시작 시간 및 종료 시간과 상관 관계 ID로 이벤트 로그를 얻</span><span class="sxs-lookup"><span data-stu-id="5a45f-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="5a45f-132">이 명령은 2017-04-15T04:30 로컬 시간 이전이나 2017-04-25T12:30 이전의 지정된 상관 관계 ID와 관련된 대부분의 1000개 이벤트를 나열합니다. 즉, 전체 날짜/시간 범위가 현재 날짜/시간에서 90일을 넘지 않는 경우 로컬 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5a45f-133">예제 9: 리소스 그룹에 대한 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="5a45f-134">이 명령은 현재 날짜/시간으로부터 7일 동안 일어났습니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-135">예제 10: 최대 이벤트 수가 있는 리소스 그룹에 대한 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="5a45f-136">이 명령은 현재 날짜/시간으로부터 7일 동안 일어났습니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-137">예제 11: 시작 시간으로 리소스 그룹에 대한 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="5a45f-138">이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 리소스 그룹과 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-139">예제 12: 시작 시간 및 종료 시간이 있는 리소스 그룹에 대한 이벤트 로그를 얻</span><span class="sxs-lookup"><span data-stu-id="5a45f-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5a45f-140">이 명령은 2017-04-15T04:30 로컬 시간 이전의 지정된 리소스 그룹과 연결된 대부분의 1000개 이벤트를 나열합니다. 전체 날짜/시간 범위가 현재 날짜/시간의 90일보다 오래되지 않은 경우 2017-04-25T12:30 로컬 시간 이전의 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5a45f-141">예제 13: 리소스 ID로 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="5a45f-142">이 명령은 현재 날짜/시간으로부터 7일 동안 일어났습니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-143">예제 14: 최대 이벤트 수가 있는 리소스 ID로 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="5a45f-144">이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 리소스 ID와 연결된 대부분의 100개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-145">예제 15: 시작 시간을 사용하여 리소스 ID로 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="5a45f-146">이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 리소스 ID와 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-147">예제 16: 시작 시간 및 종료 시간을 사용하여 리소스 ID로 이벤트 로그를 얻</span><span class="sxs-lookup"><span data-stu-id="5a45f-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5a45f-148">이 명령은 2017-04-15T04:30 로컬 시간 이전이나 2017-04-25T12:30 이전의 지정된 리소스 ID와 연결된 대부분의 1000개 이벤트가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5a45f-149">예제 17: 리소스 공급자에 의해 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="5a45f-150">이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 리소스 공급자와 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-151">예제 18: 최대 이벤트 수를 사용하여 리소스 공급자에 의해 이벤트 로그를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="5a45f-152">이 명령은 현재 날짜/시간으로부터 7일이 지난 지정된 리소스 공급자와 연결된 대부분의 100개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-153">예제 19: 시작 시간을 사용하여 리소스 공급자에 의해 이벤트 로그를 얻다</span><span class="sxs-lookup"><span data-stu-id="5a45f-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="5a45f-154">이 명령은 시작 시간이 현재 날짜/시간에서 90일을 넘지 않는 경우 2017-05-22T04:30:00 로컬 시간 이후의 지정된 리소스 공급자와 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5a45f-155">예제 20: 시작 시간 및 종료 시간을 사용하여 리소스 공급자에 의해 이벤트 로그를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5a45f-156">이 명령은 2017-04-15T04:30 로컬 시간 이후에 일어났지만 전체 날짜/시간 범위가 현재 날짜/시간의 90일보다 오래되지 않은 경우 2017-04-25T12:30 로컬 시간 이전의 지정된 리소스 공급자와 연결된 대부분의 1000개 이벤트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="5a45f-157">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a45f-157">PARAMETERS</span></span>

### <span data-ttu-id="5a45f-158">-Caller</span><span class="sxs-lookup"><span data-stu-id="5a45f-158">-Caller</span></span>
<span data-ttu-id="5a45f-159">인치할 이벤트의 호출자</span><span class="sxs-lookup"><span data-stu-id="5a45f-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="5a45f-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="5a45f-160">-CorrelationId</span></span>
<span data-ttu-id="5a45f-161">The CorrelationId</span><span class="sxs-lookup"><span data-stu-id="5a45f-161">The CorrelationId</span></span>

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

### <span data-ttu-id="5a45f-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a45f-162">-DefaultProfile</span></span>
<span data-ttu-id="5a45f-163">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a45f-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5a45f-164">-DetailedOutput</span></span>
<span data-ttu-id="5a45f-165">이벤트의 모든 세부 정보가 있는 개체를 반환합니다(기본값은 일부 특성만 반환하는 것입니다. 예: 세부 정보 없음).</span><span class="sxs-lookup"><span data-stu-id="5a45f-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

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

### <span data-ttu-id="5a45f-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5a45f-166">-EndTime</span></span>
<span data-ttu-id="5a45f-167">쿼리의 endTime</span><span class="sxs-lookup"><span data-stu-id="5a45f-167">The endTime of the query</span></span>

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

### <span data-ttu-id="5a45f-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="5a45f-168">-MaxRecord</span></span>
<span data-ttu-id="5a45f-169">인출할 레코드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="5a45f-170">별칭: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="5a45f-170">Alias: MaxRecords, MaxEvents</span></span>

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

### <span data-ttu-id="5a45f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a45f-171">-ResourceGroupName</span></span>
<span data-ttu-id="5a45f-172">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5a45f-172">The resource group name</span></span>

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

### <span data-ttu-id="5a45f-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a45f-173">-ResourceId</span></span>
<span data-ttu-id="5a45f-174">The ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a45f-174">The ResourceId</span></span>

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

### <span data-ttu-id="5a45f-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5a45f-175">-ResourceProvider</span></span>
<span data-ttu-id="5a45f-176">ResourceProvider 이름</span><span class="sxs-lookup"><span data-stu-id="5a45f-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="5a45f-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5a45f-177">-StartTime</span></span>
<span data-ttu-id="5a45f-178">쿼리의 상관 관계Id</span><span class="sxs-lookup"><span data-stu-id="5a45f-178">The correlationId of the query</span></span>

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

### <span data-ttu-id="5a45f-179">-Status</span><span class="sxs-lookup"><span data-stu-id="5a45f-179">-Status</span></span>
<span data-ttu-id="5a45f-180">인치할 이벤트의 상태</span><span class="sxs-lookup"><span data-stu-id="5a45f-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="5a45f-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a45f-181">CommonParameters</span></span>
<span data-ttu-id="5a45f-182">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a45f-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a45f-183">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a45f-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a45f-184">입력</span><span class="sxs-lookup"><span data-stu-id="5a45f-184">INPUTS</span></span>

### <span data-ttu-id="5a45f-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5a45f-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5a45f-186">System.String</span><span class="sxs-lookup"><span data-stu-id="5a45f-186">System.String</span></span>

### <span data-ttu-id="5a45f-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a45f-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5a45f-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5a45f-188">System.Int32</span></span>

## <span data-ttu-id="5a45f-189">출력</span><span class="sxs-lookup"><span data-stu-id="5a45f-189">OUTPUTS</span></span>

### <span data-ttu-id="5a45f-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="5a45f-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="5a45f-191">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a45f-191">NOTES</span></span>

## <span data-ttu-id="5a45f-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a45f-192">RELATED LINKS</span></span>
