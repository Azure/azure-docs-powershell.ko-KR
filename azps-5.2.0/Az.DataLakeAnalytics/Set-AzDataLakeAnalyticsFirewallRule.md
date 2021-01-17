---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345350"
---
# <span data-ttu-id="7ec6b-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ec6b-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7ec6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ec6b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec6b-103">Data Lake Analytics 계정에서 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7ec6b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ec6b-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ec6b-105">설명</span><span class="sxs-lookup"><span data-stu-id="7ec6b-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec6b-106">**Set-AzDataLakeAnalyticsFirewallRule** cmdlet은 Azure Data Lake Analytics 계정에서 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7ec6b-107">예제</span><span class="sxs-lookup"><span data-stu-id="7ec6b-107">EXAMPLES</span></span>

### <span data-ttu-id="7ec6b-108">예제 1: 방화벽 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="7ec6b-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="7ec6b-109">이 명령은 "ContosoAdlAcct" 계정에서 "내 방화벽 규칙"이라는 방화벽 규칙을 업데이트하여 새 IP 범위인 127.0.0.1 - 127.0.0.10을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="7ec6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ec6b-110">PARAMETERS</span></span>

### <span data-ttu-id="7ec6b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="7ec6b-111">-Account</span></span>
<span data-ttu-id="7ec6b-112">방화벽 규칙을 업데이트할 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="7ec6b-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="7ec6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec6b-113">-DefaultProfile</span></span>
<span data-ttu-id="7ec6b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7ec6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ec6b-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ec6b-115">-EndIpAddress</span></span>
<span data-ttu-id="7ec6b-116">방화벽 규칙에 대한 유효한 IP 범위의 끝</span><span class="sxs-lookup"><span data-stu-id="7ec6b-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec6b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7ec6b-117">-Name</span></span>
<span data-ttu-id="7ec6b-118">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="7ec6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ec6b-120">계정을 검색하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="7ec6b-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ec6b-121">-StartIpAddress</span></span>
<span data-ttu-id="7ec6b-122">방화벽 규칙에 대한 유효한 IP 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="7ec6b-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="7ec6b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ec6b-123">-Confirm</span></span>
<span data-ttu-id="7ec6b-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec6b-125">-WhatIf</span></span>
<span data-ttu-id="7ec6b-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7ec6b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ec6b-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec6b-128">CommonParameters</span></span>
<span data-ttu-id="7ec6b-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec6b-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ec6b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec6b-131">입력</span><span class="sxs-lookup"><span data-stu-id="7ec6b-131">INPUTS</span></span>

### <span data-ttu-id="7ec6b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7ec6b-132">System.String</span></span>

## <span data-ttu-id="7ec6b-133">출력</span><span class="sxs-lookup"><span data-stu-id="7ec6b-133">OUTPUTS</span></span>

### <span data-ttu-id="7ec6b-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7ec6b-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7ec6b-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ec6b-135">NOTES</span></span>

## <span data-ttu-id="7ec6b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ec6b-136">RELATED LINKS</span></span>
