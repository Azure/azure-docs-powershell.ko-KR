---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186180"
---
# <span data-ttu-id="bff27-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bff27-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="bff27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff27-102">SYNOPSIS</span></span>
<span data-ttu-id="bff27-103">Data Lake Analytics 계정에서 방화벽 규칙 또는 방화벽 규칙 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="bff27-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="bff27-104">구문</span><span class="sxs-lookup"><span data-stu-id="bff27-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bff27-105">설명</span><span class="sxs-lookup"><span data-stu-id="bff27-105">DESCRIPTION</span></span>
<span data-ttu-id="bff27-106">**Get-AzDataLakeAnalyticsFirewallRule** cmdlet은 Azure Data Lake Analytics 계정에서 방화벽 규칙 또는 방화벽 규칙 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="bff27-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bff27-107">예제</span><span class="sxs-lookup"><span data-stu-id="bff27-107">EXAMPLES</span></span>

### <span data-ttu-id="bff27-108">예제 1: 방화벽 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="bff27-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="bff27-109">이 명령은 계정 "ContosoAdlAcct"에서 "내 방화벽 규칙"이라는 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bff27-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="bff27-110">예제 2: 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="bff27-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="bff27-111">이 명령은 계정 "ContosoAdlAcct"에서 모든 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bff27-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="bff27-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bff27-112">PARAMETERS</span></span>

### <span data-ttu-id="bff27-113">-Account</span><span class="sxs-lookup"><span data-stu-id="bff27-113">-Account</span></span>
<span data-ttu-id="bff27-114">방화벽 규칙을 얻을 Data Lake Analytics 계정</span><span class="sxs-lookup"><span data-stu-id="bff27-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="bff27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff27-115">-DefaultProfile</span></span>
<span data-ttu-id="bff27-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bff27-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bff27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bff27-117">-Name</span></span>
<span data-ttu-id="bff27-118">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bff27-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff27-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff27-119">-ResourceGroupName</span></span>
<span data-ttu-id="bff27-120">계정을 검색하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bff27-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="bff27-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff27-121">CommonParameters</span></span>
<span data-ttu-id="bff27-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bff27-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff27-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bff27-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff27-124">입력</span><span class="sxs-lookup"><span data-stu-id="bff27-124">INPUTS</span></span>

### <span data-ttu-id="bff27-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bff27-125">System.String</span></span>

## <span data-ttu-id="bff27-126">출력</span><span class="sxs-lookup"><span data-stu-id="bff27-126">OUTPUTS</span></span>

### <span data-ttu-id="bff27-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bff27-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="bff27-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bff27-128">NOTES</span></span>

## <span data-ttu-id="bff27-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bff27-129">RELATED LINKS</span></span>
