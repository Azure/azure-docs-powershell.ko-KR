---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215115"
---
# <span data-ttu-id="0f24b-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="0f24b-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="0f24b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f24b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f24b-103">Azure 리소스 관리 끝점에 대 한 HTTP 요청을 생성 하 고 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f24b-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="0f24b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f24b-104">SYNTAX</span></span>

### <span data-ttu-id="0f24b-105">ByPath (기본값)</span><span class="sxs-lookup"><span data-stu-id="0f24b-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f24b-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="0f24b-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f24b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0f24b-107">DESCRIPTION</span></span>
<span data-ttu-id="0f24b-108">Azure 리소스 관리 끝점에 대 한 HTTP 요청을 생성 하 고 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f24b-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="0f24b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0f24b-109">EXAMPLES</span></span>

### <span data-ttu-id="0f24b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f24b-110">Example 1</span></span>
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

<span data-ttu-id="0f24b-111">경로를 기준으로 로그 분석 작업 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="0f24b-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="0f24b-112">변수</span><span class="sxs-lookup"><span data-stu-id="0f24b-112">PARAMETERS</span></span>

### <span data-ttu-id="0f24b-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f24b-113">-ApiVersion</span></span>
<span data-ttu-id="0f24b-114">Api 버전</span><span class="sxs-lookup"><span data-stu-id="0f24b-114">Api Version</span></span>

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

### <span data-ttu-id="0f24b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f24b-115">-AsJob</span></span>
<span data-ttu-id="0f24b-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0f24b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f24b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f24b-117">-DefaultProfile</span></span>
<span data-ttu-id="0f24b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f24b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f24b-119">-메서드</span><span class="sxs-lookup"><span data-stu-id="0f24b-119">-Method</span></span>
<span data-ttu-id="0f24b-120">Http 메서드</span><span class="sxs-lookup"><span data-stu-id="0f24b-120">Http Method</span></span>

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

### <span data-ttu-id="0f24b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0f24b-121">-Name</span></span>
<span data-ttu-id="0f24b-122">대상 리소스 이름 목록</span><span class="sxs-lookup"><span data-stu-id="0f24b-122">list of Target Resource Name</span></span>

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

### <span data-ttu-id="0f24b-123">-Path</span><span class="sxs-lookup"><span data-stu-id="0f24b-123">-Path</span></span>
<span data-ttu-id="0f24b-124">대상 경로</span><span class="sxs-lookup"><span data-stu-id="0f24b-124">Target Path</span></span>

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

### <span data-ttu-id="0f24b-125">-페이로드</span><span class="sxs-lookup"><span data-stu-id="0f24b-125">-Payload</span></span>
<span data-ttu-id="0f24b-126">JSON 형식 페이로드</span><span class="sxs-lookup"><span data-stu-id="0f24b-126">JSON format payload</span></span>

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

### <span data-ttu-id="0f24b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f24b-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f24b-128">대상 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0f24b-128">Target Resource Group Name</span></span>

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

### <span data-ttu-id="0f24b-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="0f24b-129">-ResourceProviderName</span></span>
<span data-ttu-id="0f24b-130">대상 리소스 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="0f24b-130">Target Resource Provider Name</span></span>

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

### <span data-ttu-id="0f24b-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0f24b-131">-ResourceType</span></span>
<span data-ttu-id="0f24b-132">대상 리소스 종류 목록</span><span class="sxs-lookup"><span data-stu-id="0f24b-132">List of Target Resource Type</span></span>

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

### <span data-ttu-id="0f24b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f24b-133">-SubscriptionId</span></span>
<span data-ttu-id="0f24b-134">대상 구독 Id</span><span class="sxs-lookup"><span data-stu-id="0f24b-134">Target Subscription Id</span></span>

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

### <span data-ttu-id="0f24b-135">-확인</span><span class="sxs-lookup"><span data-stu-id="0f24b-135">-Confirm</span></span>
<span data-ttu-id="0f24b-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f24b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f24b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f24b-137">-WhatIf</span></span>
<span data-ttu-id="0f24b-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f24b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f24b-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f24b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f24b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f24b-140">CommonParameters</span></span>
<span data-ttu-id="0f24b-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f24b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f24b-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f24b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f24b-143">입력</span><span class="sxs-lookup"><span data-stu-id="0f24b-143">INPUTS</span></span>

### <span data-ttu-id="0f24b-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0f24b-144">System.string</span></span>

## <span data-ttu-id="0f24b-145">출력</span><span class="sxs-lookup"><span data-stu-id="0f24b-145">OUTPUTS</span></span>

### <span data-ttu-id="0f24b-146">PSHttpResponse (. \*)</span><span class="sxs-lookup"><span data-stu-id="0f24b-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="0f24b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0f24b-147">NOTES</span></span>

## <span data-ttu-id="0f24b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f24b-148">RELATED LINKS</span></span>
