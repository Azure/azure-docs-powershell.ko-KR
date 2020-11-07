---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703367"
---
# <span data-ttu-id="27bf4-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="27bf4-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="27bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="27bf4-103">리소스에 대 한 로그 및 메트릭 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27bf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27bf4-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27bf4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="27bf4-106">**AzureRmDiagnosticSetting** cmdlet은 특정 리소스에 대해 각 시간 세분화 및 로그 범주를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="27bf4-107">로그 및 메트릭은 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="27bf4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="27bf4-108">EXAMPLES</span></span>

### <span data-ttu-id="27bf4-109">예제 1: 리소스에 대 한 모든 메트릭 및 로그 사용</span><span class="sxs-lookup"><span data-stu-id="27bf4-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="27bf4-110">이 명령은 Resource01에 대해 사용 가능한 모든 메트릭과 로그를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="27bf4-111">예제 2: 모든 메트릭 및 로그 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="27bf4-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="27bf4-112">이 명령은 리소스 Resource01 사용할 수 있는 모든 메트릭 및 로그를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="27bf4-113">예제 3: 여러 범주 사용</span><span class="sxs-lookup"><span data-stu-id="27bf4-113">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
Timegrain : PT1H
Logs
Enabled  : True
Category : Category1
Enabled  : True
Category : Category2
Enabled  : True
Category : Category3
Enabled  : False
Category : Category4
```

<span data-ttu-id="27bf4-114">이 명령은 Category1 및 Category2를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="27bf4-115">모든 timegrains 및 다른 범주는 동일 하 게 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="27bf4-116">예제 4: 시간 세분화 및 여러 범주 사용</span><span class="sxs-lookup"><span data-stu-id="27bf4-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="27bf4-117">이 명령은 Category1, Category2 및 시간 세분화 PT1M만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="27bf4-118">다른 모든 시간 grains 및 범주는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="27bf4-119">변수</span><span class="sxs-lookup"><span data-stu-id="27bf4-119">PARAMETERS</span></span>

### <span data-ttu-id="27bf4-120">-범주</span><span class="sxs-lookup"><span data-stu-id="27bf4-120">-Categories</span></span>
<span data-ttu-id="27bf4-121">사용 *가능* 값에 따라 사용 하거나 사용 하지 않도록 설정할 로그 범주 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="27bf4-122">범주를 지정 하지 않으면이 명령은 모든 범주에 대해 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-122">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bf4-123">-사용</span><span class="sxs-lookup"><span data-stu-id="27bf4-123">-Enabled</span></span>
<span data-ttu-id="27bf4-124">진단을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="27bf4-125">진단 기능을 사용 하도록 $True를 지정 하거나 진단을 사용 하지 않도록 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bf4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27bf4-126">-ResourceId</span></span>
<span data-ttu-id="27bf4-127">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bf4-128">-보존 설정</span><span class="sxs-lookup"><span data-stu-id="27bf4-128">-RetentionEnabled</span></span>
<span data-ttu-id="27bf4-129">진단 정보의 보존을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bf4-130">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="27bf4-130">-RetentionInDays</span></span>
<span data-ttu-id="27bf4-131">보존 정책을 일 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bf4-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="27bf4-132">-ServiceBusRuleId</span></span>
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

### <span data-ttu-id="27bf4-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="27bf4-133">-StorageAccountId</span></span>
<span data-ttu-id="27bf4-134">데이터를 저장할 저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-134">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="27bf4-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="27bf4-135">-Timegrains</span></span>
<span data-ttu-id="27bf4-136">*사용* 값에 따라 메트릭을 사용 하거나 사용 하지 않도록 설정 하는 시간 grains 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="27bf4-137">시간 세분화를 지정 하지 않으면이 명령은 사용 가능한 모든 시간 grains에 대해 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bf4-138">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="27bf4-138">-WorkspaceId</span></span>
<span data-ttu-id="27bf4-139">작업 영역의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-139">The Id of the workspace</span></span>

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

### <span data-ttu-id="27bf4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27bf4-140">-DefaultProfile</span></span>
<span data-ttu-id="27bf4-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27bf4-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="27bf4-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="27bf4-143">이벤트 허브 규칙 id</span><span class="sxs-lookup"><span data-stu-id="27bf4-143">The event hub rule id</span></span>

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

### <span data-ttu-id="27bf4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27bf4-144">CommonParameters</span></span>
<span data-ttu-id="27bf4-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27bf4-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27bf4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27bf4-147">입력</span><span class="sxs-lookup"><span data-stu-id="27bf4-147">INPUTS</span></span>

## <span data-ttu-id="27bf4-148">출력</span><span class="sxs-lookup"><span data-stu-id="27bf4-148">OUTPUTS</span></span>

### <span data-ttu-id="27bf4-149">PSServiceDiagnosticSettings를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf4-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="27bf4-150">상속자</span><span class="sxs-lookup"><span data-stu-id="27bf4-150">NOTES</span></span>

## <span data-ttu-id="27bf4-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27bf4-151">RELATED LINKS</span></span>

[<span data-ttu-id="27bf4-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="27bf4-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


