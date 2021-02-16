---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190457"
---
# <span data-ttu-id="86170-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="86170-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="86170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86170-102">SYNOPSIS</span></span>
<span data-ttu-id="86170-103">Azure 리소스 관리 엔드포인트에만 HTTP 요청을 생성하고 수행</span><span class="sxs-lookup"><span data-stu-id="86170-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="86170-104">구문</span><span class="sxs-lookup"><span data-stu-id="86170-104">SYNTAX</span></span>

### <span data-ttu-id="86170-105">ByPath(기본값)</span><span class="sxs-lookup"><span data-stu-id="86170-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86170-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="86170-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86170-107">설명</span><span class="sxs-lookup"><span data-stu-id="86170-107">DESCRIPTION</span></span>
<span data-ttu-id="86170-108">Azure 리소스 관리 엔드포인트에만 HTTP 요청을 생성하고 수행</span><span class="sxs-lookup"><span data-stu-id="86170-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="86170-109">예제</span><span class="sxs-lookup"><span data-stu-id="86170-109">EXAMPLES</span></span>

### <span data-ttu-id="86170-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="86170-110">Example 1</span></span>
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

<span data-ttu-id="86170-111">경로에 따라 로그 분석 작업 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="86170-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="86170-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86170-112">PARAMETERS</span></span>

### <span data-ttu-id="86170-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="86170-113">-ApiVersion</span></span>
<span data-ttu-id="86170-114">API 버전</span><span class="sxs-lookup"><span data-stu-id="86170-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86170-115">-AsJob</span></span>
<span data-ttu-id="86170-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="86170-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86170-117">-DefaultProfile</span></span>
<span data-ttu-id="86170-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86170-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-119">-Method</span><span class="sxs-lookup"><span data-stu-id="86170-119">-Method</span></span>
<span data-ttu-id="86170-120">Http 메서드</span><span class="sxs-lookup"><span data-stu-id="86170-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-121">-Name</span><span class="sxs-lookup"><span data-stu-id="86170-121">-Name</span></span>
<span data-ttu-id="86170-122">대상 리소스 이름 목록</span><span class="sxs-lookup"><span data-stu-id="86170-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-123">-Path</span><span class="sxs-lookup"><span data-stu-id="86170-123">-Path</span></span>
<span data-ttu-id="86170-124">대상 경로</span><span class="sxs-lookup"><span data-stu-id="86170-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-125">-Payload</span><span class="sxs-lookup"><span data-stu-id="86170-125">-Payload</span></span>
<span data-ttu-id="86170-126">JSON 형식 페이로드</span><span class="sxs-lookup"><span data-stu-id="86170-126">JSON format payload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86170-127">-ResourceGroupName</span></span>
<span data-ttu-id="86170-128">대상 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="86170-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="86170-129">-ResourceProviderName</span></span>
<span data-ttu-id="86170-130">대상 리소스 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="86170-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="86170-131">-ResourceType</span></span>
<span data-ttu-id="86170-132">대상 리소스 종류 목록</span><span class="sxs-lookup"><span data-stu-id="86170-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86170-133">-SubscriptionId</span></span>
<span data-ttu-id="86170-134">대상 구독 ID</span><span class="sxs-lookup"><span data-stu-id="86170-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86170-135">-Confirm</span></span>
<span data-ttu-id="86170-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="86170-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86170-137">-WhatIf</span></span>
<span data-ttu-id="86170-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="86170-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86170-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86170-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86170-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86170-140">CommonParameters</span></span>
<span data-ttu-id="86170-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86170-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86170-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86170-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86170-143">입력</span><span class="sxs-lookup"><span data-stu-id="86170-143">INPUTS</span></span>

### <span data-ttu-id="86170-144">System.string</span><span class="sxs-lookup"><span data-stu-id="86170-144">System.string</span></span>

## <span data-ttu-id="86170-145">출력</span><span class="sxs-lookup"><span data-stu-id="86170-145">OUTPUTS</span></span>

### <span data-ttu-id="86170-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="86170-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="86170-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86170-147">NOTES</span></span>

## <span data-ttu-id="86170-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86170-148">RELATED LINKS</span></span>
