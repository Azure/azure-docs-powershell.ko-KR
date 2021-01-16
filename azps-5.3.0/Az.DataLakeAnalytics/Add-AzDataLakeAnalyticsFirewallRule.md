---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493490"
---
# <span data-ttu-id="fed50-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fed50-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="fed50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed50-102">SYNOPSIS</span></span>
<span data-ttu-id="fed50-103">Data Lake Analytics 계정에 방화벽 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="fed50-104">구문</span><span class="sxs-lookup"><span data-stu-id="fed50-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fed50-105">설명</span><span class="sxs-lookup"><span data-stu-id="fed50-105">DESCRIPTION</span></span>
<span data-ttu-id="fed50-106">**Add-AzDataLakeAnalyticsFirewallRule** cmdlet은 Azure Data Lake Analytics 계정에 방화벽 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="fed50-107">예제</span><span class="sxs-lookup"><span data-stu-id="fed50-107">EXAMPLES</span></span>

### <span data-ttu-id="fed50-108">예제 1: 방화벽 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="fed50-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="fed50-109">이 명령은 IP 범위가 127.0.0.1 - 127.0.0.10인 계정 "ContosoAdlAcct"에서 "내 방화벽 규칙"이라는 방화벽 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="fed50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fed50-110">PARAMETERS</span></span>

### <span data-ttu-id="fed50-111">-Account</span><span class="sxs-lookup"><span data-stu-id="fed50-111">-Account</span></span>
<span data-ttu-id="fed50-112">방화벽 규칙을 추가할 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="fed50-112">The Data Lake Analytics account to add the firewall rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed50-113">-DefaultProfile</span></span>
<span data-ttu-id="fed50-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fed50-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fed50-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="fed50-115">-EndIpAddress</span></span>
<span data-ttu-id="fed50-116">방화벽 규칙에 대한 유효한 IP 범위의 끝</span><span class="sxs-lookup"><span data-stu-id="fed50-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed50-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fed50-117">-Name</span></span>
<span data-ttu-id="fed50-118">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed50-119">-ResourceGroupName</span></span>
<span data-ttu-id="fed50-120">계정을 검색하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="fed50-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="fed50-121">-StartIpAddress</span></span>
<span data-ttu-id="fed50-122">방화벽 규칙에 대한 유효한 IP 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="fed50-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed50-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fed50-123">-Confirm</span></span>
<span data-ttu-id="fed50-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed50-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fed50-125">-WhatIf</span></span>
<span data-ttu-id="fed50-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fed50-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fed50-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fed50-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed50-128">CommonParameters</span></span>
<span data-ttu-id="fed50-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fed50-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed50-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fed50-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed50-131">입력</span><span class="sxs-lookup"><span data-stu-id="fed50-131">INPUTS</span></span>

### <span data-ttu-id="fed50-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fed50-132">System.String</span></span>

## <span data-ttu-id="fed50-133">출력</span><span class="sxs-lookup"><span data-stu-id="fed50-133">OUTPUTS</span></span>

### <span data-ttu-id="fed50-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fed50-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="fed50-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fed50-135">NOTES</span></span>

## <span data-ttu-id="fed50-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fed50-136">RELATED LINKS</span></span>
