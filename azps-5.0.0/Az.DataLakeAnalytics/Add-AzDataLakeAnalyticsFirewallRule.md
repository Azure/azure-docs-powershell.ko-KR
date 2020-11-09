---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305891"
---
# <span data-ttu-id="dd313-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dd313-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="dd313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd313-102">SYNOPSIS</span></span>
<span data-ttu-id="dd313-103">Data Lake Analytics 계정에 방화벽 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="dd313-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd313-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd313-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dd313-105">DESCRIPTION</span></span>
<span data-ttu-id="dd313-106">**Add-AzDataLakeAnalyticsFirewallRule** Cmdlet은 Azure Data Lake Analytics 계정에 방화벽 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="dd313-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dd313-107">EXAMPLES</span></span>

### <span data-ttu-id="dd313-108">예제 1: 방화벽 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="dd313-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="dd313-109">이 명령은 "ContosoAdlAcct" 계정의 "my 방화벽 규칙" 이라는 방화벽 규칙을 IP 범위: 127.0.0.1-127.0.0.10에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="dd313-110">변수</span><span class="sxs-lookup"><span data-stu-id="dd313-110">PARAMETERS</span></span>

### <span data-ttu-id="dd313-111">-계정</span><span class="sxs-lookup"><span data-stu-id="dd313-111">-Account</span></span>
<span data-ttu-id="dd313-112">방화벽 규칙을 추가할 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="dd313-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="dd313-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd313-113">-DefaultProfile</span></span>
<span data-ttu-id="dd313-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dd313-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd313-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="dd313-115">-EndIpAddress</span></span>
<span data-ttu-id="dd313-116">방화벽 규칙에 대 한 유효한 ip 범위의 끝</span><span class="sxs-lookup"><span data-stu-id="dd313-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="dd313-117">-이름</span><span class="sxs-lookup"><span data-stu-id="dd313-117">-Name</span></span>
<span data-ttu-id="dd313-118">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="dd313-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd313-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd313-120">계정을 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="dd313-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="dd313-121">-StartIpAddress</span></span>
<span data-ttu-id="dd313-122">방화벽 규칙에 대 한 유효한 ip 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="dd313-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="dd313-123">-확인</span><span class="sxs-lookup"><span data-stu-id="dd313-123">-Confirm</span></span>
<span data-ttu-id="dd313-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd313-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd313-125">-WhatIf</span></span>
<span data-ttu-id="dd313-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd313-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd313-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd313-128">CommonParameters</span></span>
<span data-ttu-id="dd313-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd313-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd313-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd313-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd313-131">입력</span><span class="sxs-lookup"><span data-stu-id="dd313-131">INPUTS</span></span>

### <span data-ttu-id="dd313-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dd313-132">System.String</span></span>

## <span data-ttu-id="dd313-133">출력</span><span class="sxs-lookup"><span data-stu-id="dd313-133">OUTPUTS</span></span>

### <span data-ttu-id="dd313-134">DataLakeAnalytics. DataLakeAnalyticsFirewallRule/.</span><span class="sxs-lookup"><span data-stu-id="dd313-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="dd313-135">상속자</span><span class="sxs-lookup"><span data-stu-id="dd313-135">NOTES</span></span>

## <span data-ttu-id="dd313-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd313-136">RELATED LINKS</span></span>
