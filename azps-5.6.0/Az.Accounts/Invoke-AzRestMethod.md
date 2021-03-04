---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: 355de1e4eb4518b8ec3d7291b20f76bda5fb1a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955019"
---
# <span data-ttu-id="a9298-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="a9298-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="a9298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9298-102">SYNOPSIS</span></span>
<span data-ttu-id="a9298-103">Azure 리소스 관리 엔드포인트에 대한 HTTP 요청 생성 및 수행</span><span class="sxs-lookup"><span data-stu-id="a9298-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="a9298-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9298-104">SYNTAX</span></span>

### <span data-ttu-id="a9298-105">ByPath(기본값)</span><span class="sxs-lookup"><span data-stu-id="a9298-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9298-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="a9298-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9298-107">설명</span><span class="sxs-lookup"><span data-stu-id="a9298-107">DESCRIPTION</span></span>
<span data-ttu-id="a9298-108">Azure 리소스 관리 엔드포인트에 대한 HTTP 요청 생성 및 수행</span><span class="sxs-lookup"><span data-stu-id="a9298-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="a9298-109">예제</span><span class="sxs-lookup"><span data-stu-id="a9298-109">EXAMPLES</span></span>

### <span data-ttu-id="a9298-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a9298-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="a9298-111">경로에 따라 로그 분석 작업 영역 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9298-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="a9298-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9298-112">PARAMETERS</span></span>

### <span data-ttu-id="a9298-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a9298-113">-ApiVersion</span></span>
<span data-ttu-id="a9298-114">Api 버전</span><span class="sxs-lookup"><span data-stu-id="a9298-114">Api Version</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9298-115">-AsJob</span></span>
<span data-ttu-id="a9298-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a9298-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9298-117">-DefaultProfile</span></span>
<span data-ttu-id="a9298-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9298-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9298-119">-Method</span><span class="sxs-lookup"><span data-stu-id="a9298-119">-Method</span></span>
<span data-ttu-id="a9298-120">Http 메서드</span><span class="sxs-lookup"><span data-stu-id="a9298-120">Http Method</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a9298-121">-Name</span></span>
<span data-ttu-id="a9298-122">대상 리소스 이름 목록</span><span class="sxs-lookup"><span data-stu-id="a9298-122">list of Target Resource Name</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-123">-Path</span><span class="sxs-lookup"><span data-stu-id="a9298-123">-Path</span></span>
<span data-ttu-id="a9298-124">대상 경로</span><span class="sxs-lookup"><span data-stu-id="a9298-124">Target Path</span></span>

```yaml
Type: System.String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-125">-페이로드</span><span class="sxs-lookup"><span data-stu-id="a9298-125">-Payload</span></span>
<span data-ttu-id="a9298-126">JSON 형식 페이로드</span><span class="sxs-lookup"><span data-stu-id="a9298-126">JSON format payload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9298-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9298-128">대상 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a9298-128">Target Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="a9298-129">-ResourceProviderName</span></span>
<span data-ttu-id="a9298-130">대상 리소스 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="a9298-130">Target Resource Provider Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a9298-131">-ResourceType</span></span>
<span data-ttu-id="a9298-132">대상 리소스 유형 목록</span><span class="sxs-lookup"><span data-stu-id="a9298-132">List of Target Resource Type</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9298-133">-SubscriptionId</span></span>
<span data-ttu-id="a9298-134">대상 구독 ID</span><span class="sxs-lookup"><span data-stu-id="a9298-134">Target Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9298-135">-확인</span><span class="sxs-lookup"><span data-stu-id="a9298-135">-Confirm</span></span>
<span data-ttu-id="a9298-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9298-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9298-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9298-137">-WhatIf</span></span>
<span data-ttu-id="a9298-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9298-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9298-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9298-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9298-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9298-140">CommonParameters</span></span>
<span data-ttu-id="a9298-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9298-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9298-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9298-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9298-143">입력</span><span class="sxs-lookup"><span data-stu-id="a9298-143">INPUTS</span></span>

### <span data-ttu-id="a9298-144">System.string</span><span class="sxs-lookup"><span data-stu-id="a9298-144">System.string</span></span>

## <span data-ttu-id="a9298-145">출력</span><span class="sxs-lookup"><span data-stu-id="a9298-145">OUTPUTS</span></span>

### <span data-ttu-id="a9298-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="a9298-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="a9298-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9298-147">NOTES</span></span>

## <span data-ttu-id="a9298-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9298-148">RELATED LINKS</span></span>
