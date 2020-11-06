---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4bfbb25fa8b1e372175f741fd298384caa8050ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532046"
---
# <span data-ttu-id="63609-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63609-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="63609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63609-102">SYNOPSIS</span></span>
<span data-ttu-id="63609-103">Data Lake Analytics 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63609-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63609-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63609-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63609-105">DESCRIPTION</span></span>
<span data-ttu-id="63609-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="63609-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63609-107">EXAMPLES</span></span>

### <span data-ttu-id="63609-108">예제 1: 계정의 데이터 원본 수정</span><span class="sxs-lookup"><span data-stu-id="63609-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="63609-109">이 명령은 기본 데이터 원본 및 계정의 Tags 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="63609-110">변수</span><span class="sxs-lookup"><span data-stu-id="63609-110">PARAMETERS</span></span>

### <span data-ttu-id="63609-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="63609-111">-AllowAzureIpState</span></span>
<span data-ttu-id="63609-112">방화벽을 통해 Azure 시작 Ip를 선택적으로 허용/차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63609-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63609-113">-DefaultProfile</span></span>
<span data-ttu-id="63609-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="63609-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63609-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="63609-115">-FirewallState</span></span>
<span data-ttu-id="63609-116">필요에 따라 기존 방화벽 규칙을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63609-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="63609-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="63609-118">계정 업데이트를 위해 지원 되는 최대 분석 단위 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="63609-118">The optional maximum supported analytics units to update the account with.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63609-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="63609-119">-MaxJobCount</span></span>
<span data-ttu-id="63609-120">계정에서 설정에 대해 동시에 실행 되는 선택적 최대 지원 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="63609-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="63609-121">-이름</span><span class="sxs-lookup"><span data-stu-id="63609-121">-Name</span></span>
<span data-ttu-id="63609-122">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-122">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63609-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="63609-123">-QueryStoreRetention</span></span>
<span data-ttu-id="63609-124">계정에 설정 된 대로 작업 메타 데이터가 유지 되는 선택적 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="63609-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="63609-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63609-125">-ResourceGroupName</span></span>
<span data-ttu-id="63609-126">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63609-127">태그</span><span class="sxs-lookup"><span data-stu-id="63609-127">-Tag</span></span>
<span data-ttu-id="63609-128">현재 태그 집합을 대체 해야 하는이 계정과 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="63609-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63609-129">-티어</span><span class="sxs-lookup"><span data-stu-id="63609-129">-Tier</span></span>
<span data-ttu-id="63609-130">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="63609-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63609-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63609-131">CommonParameters</span></span>
<span data-ttu-id="63609-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63609-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63609-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63609-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63609-134">입력</span><span class="sxs-lookup"><span data-stu-id="63609-134">INPUTS</span></span>

### <span data-ttu-id="63609-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63609-135">System.String</span></span>

### <span data-ttu-id="63609-136">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="63609-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="63609-137">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="63609-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="63609-138">시스템 Null 허용 ' 1 [[DataLake]. TierType, [Microsoft Azure. DataLake. 31bf3856ad364e35, Version = 3.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="63609-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="63609-139">시스템 Null 허용 ' 1 [[DataLake]. FirewallState, [Microsoft Azure. DataLake. 31bf3856ad364e35, Version = 3.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="63609-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="63609-140">시스템 Null 허용 ' 1 [[DataLake]. FirewallAllowAzureIpsState, [Microsoft Azure. DataLake. 31bf3856ad364e35, Version = 3.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="63609-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="63609-141">출력</span><span class="sxs-lookup"><span data-stu-id="63609-141">OUTPUTS</span></span>

### <span data-ttu-id="63609-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63609-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="63609-143">상속자</span><span class="sxs-lookup"><span data-stu-id="63609-143">NOTES</span></span>

## <span data-ttu-id="63609-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63609-144">RELATED LINKS</span></span>

[<span data-ttu-id="63609-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63609-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="63609-146">새로운 AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63609-146">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="63609-147">제거-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63609-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="63609-148">테스트-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="63609-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


